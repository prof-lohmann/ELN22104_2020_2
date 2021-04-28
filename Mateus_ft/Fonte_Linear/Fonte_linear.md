# Parte 01: Entendendo um regulador linear

  - Qual relação entre a tensão de alimentação do ampop e a tensão de saída?

  Existe uma diferença de tensão entre a tensão de saída e a tensão de alimentação que deve ser respeitada, pois o ampop satura quando a tensão de saída se aproxima da tensão de   alimentação. Dessa forma é importante consultar o datasheet para consultar tais informações.


  - O que devemos considerar para esse circuito operar como um LDO?

  Uma baixa queda de tensão no mosfet. Tendo em vista que a potência dissipada no mosfet é diretamente proporcional a corrente que por ele passa e pela diferença de potencial. 

    P=V*I


  - Como obter as tensões de alimentação para o AmpOp (VCC e VEE)?


  Com um dobrador de tensão. Pois a tensão de alimentação do ampop precisa ser maior do que a tensão que o circuito original fornece.


  - Utilizando o circuito dobrador de tensão, qual valor de VCC você obtêm para um sinal Vin+ de 12Vrms?

  Vp= 12*(2/sqrt(2))
  Vp= 16,97 V

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/Fonte_Linear/imagens/dobrador%20de%20tensao.png)

  Vcc= 2*Vp - 2Vd

  Vcc= 2*16,97 - 2*0,7

  Vcc= 32,54 V

-  Quais problemas apresentam esse circuito?

  Tensão de ripple na realimentação do ampop. O que ocasiona ruído na saída

- Podemos melhorar?

  Sim. Adicionar um regulador linear. Assim eliminando os ruídos.



## Projeto do circuito de alimentação do ampop:

Ampop utilizado: LM324

Datasheet utilizado: https://www.ti.com/lit/ds/symlink/lm324.pdf?ts=1618824027289&ref_url=https%253A%252F%252Fwww.ti.com%252Fproduct%252FLM324

- Qual a Tensão VGS? Descreva como obter o valor.

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/Fonte_Linear/imagens/irf540vgs.png)

Conforme o datasheet a tensão Vgs para uma corrente de 1A é de 4,5V.


- Qual a corrente de alimentação do AmpOp?

  Como especificado no datasheet:

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/Fonte_Linear/imagens/icc_.png)

  Corrente de alimentação(Icc)= de 1mA até 3mA

- Qual a tensão de alimentação do AmpOP?


![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/Fonte_Linear/imagens/supplyvoltage.png)

Supply voltage(Vcc) = 32 V (máx)

Vee= 0V (gnd) no projeto


- Qual fator devo considerar para escolher o transistor Q1?

O beta precisa ser bastante elevado.
```
Beta= Ic/Ib
Beta^^^
Ic= Ie
```

- Qual valor da tensão do diodo zener D6?
  
  Considerando que a tensão de saída do ampop deve ser de 19,5V. Pois Vgs=4,5V
  
  Logo 15+4,5= 19,5V
  A tensão do diodo zener deve ser maior que 19,5V.
  
  
- Como escolher o diodo zener D6, maximizando a eficiência energética e
minimizando os ruídos no circuito?

Escolhendo um diodo zener que passe a menor corrente possível. Para isso precisa ser um zener com um resistor de zener pequeno

### Projeto no ltspice:

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/Fonte_Linear/imagens/alimentac_opamp_circ.png)


Observa-se que no circuito a associação de capacitores c2 e c3 com os diodos d3 e d4 formam um multiplicador de tensão retificado, sendo c3 o capacitor responsável por retificar o sinal. Que resulta na label Vcc1



![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/Fonte_Linear/imagens/vripple_aliment.png)

Entretando essa saída sofre com ruídos. Para resolver o problema foi adicionado um regulador de tensão com diodo zener e transistor tbj.

A tensão de ripple simulada é de 1,08V. Para resolver esse problema foi adicionado ao circuito um regulador de tensão com o regulador zener EDZV24B e o transistor tbj BC547C.

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/Fonte_Linear/imagens/vcc2_opamp.png)

Observa-se que a tensão de saída vcc2 ja regulada é estável em aproximadamente 23,75V.

Essa será a tensao de alimentação do ampop.





O diodo zener escolhido tem a tensão de funcionamento de 24V. Portanto atende ao resquisito de Vzener>19,5V

O transistor Q1 escolhido tem um beta de 520. Portanto corresponde ao requisito de projeto.

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/Fonte_Linear/imagens/bc547c_beta.png)



Portanto o projeto corresponde a todas as especificações.


- Considere que, por alterações futuras no circuito, o AmpOp poderá ter uma aumento de 10mA na corrente de alimentação, o circuito proposto continuará funcionando?

Sim, uma vez que a corrente de alimentação é maior que a mínima corrente de alimentação o ampop funcionará.


# Parte 02:  Calculando e dimensionando os componentes

## Para o primeiro bloco (D1, D2 e C1) considere vin+ = 12Vrms, vripple_pós_retificador = 1V e I_carga = 1,1A. Justifique a escolha dos componentes.

  D1 e D2 vão influenciar na tensão final. Pois terá queda de tensão de aproximadamente 0.7V para diodo de silício. Outro aspecto a ser observado é a tensão reversa que para esse diodo é de 53Vrms, segundo datasheet:

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/Fonte_Linear/imagens/reverse%20voltage.png)



     ```
     Vrp= Icarga/C*f
     1=1,1/120*C1
     C1=9,2mF
     Obs: Frequencia do retificador de onda completa é 2*F do sinal original. Portanto 2*60=120hz
      ```

## Circuito referência de tensão zener (R1 e D3):
 Quais fatores devo considerar para escolher o diodo zener para essa aplicação?
 
 Menor ruído na saída. Que influencia no Rzener do diodo.
 
 O diodo ptz12b atende a tais requisitos.
 
 ![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/Fonte_Linear/imagens/rzenerptz12b.png)
 
 Tensão regulada em 12v.
 
 

 
 - Qual o impacto da regulação linha / carga do circuito com o diodo zener na tensão de saída do regulador linear?
 
   A tensão de entrada é multiplicada pelo ganho do ampop. Portanto a regulaçao de linha de entrada será multiplicada pelo ganho na saída do ampop.

  Desta forma será projetado um circuito que tenha baixa variação de tensão de carga e linha. Para que a tensão de saída seja estável.

  O diodo zener estará regulando a tensão de entrada do ampop em 12volts, de tal forma que a variação Vout seja baixa, quase nula. Eliminando as variações de tensão do circuito.

  Regulação de linha = (delVout)/(delVin) = 0/delVin = 0 

  Da mesma forma para o regulador de carga:

  Regulação de carga = (delVout)/(delIout) = 0/delIout = 0 V/A


  - Podemos melhorar esse circuito?

  Sim. Eliminar um dos fatores da regulação de linha do circuito. Com uma fonte de corrente. A corrente será constante no zener portanto a tensão não varia no zener.
  
  - Calculo do R1:

Para calcular o resitor R1 foi calculado a diferença de potencial que ele está sujeito que é:

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/Fonte_Linear/imagens/VSRET_VZENER_VR1.png)

A corrente que passa por R1, que é a mesma corrente de zener pois o ampop consome uma corrente muito inferior na casa de nA o que não influência na conta

Corrente de zener simulada:

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/Fonte_Linear/imagens/IR1_IZENER.png)


Portanto R1:

```
(Vs_ret-vzener)/R1=Izener
R1= (Vs_ret-vzener)/Izener

R1=3,50/3,48*10^-3
R1= 1005,7 ohms

```


## Escolhendo transistor M1 e calculando R2 e R3:

- Qual a corrente contínua necessária?

  Para o transistor M1 é requisito de projeto que seja de 1A.
  
  ## Ao escolher o transistor obtenha:
 

- Quais os os parâmetros L, W, uo, Cox, VA e Vt?

L= 100uH;   

W= 100uW;

u0 (valor padrão) = 600 cm²/V/s;  

C0x = KP/u0 = 25,0081/600 = 41,68 mF/m²  

VA = 1/LAMBDA = 1/0.00291031 = 343,61 v 

Vt = 3.56362 V

Dados retirados do modelo spice do mosfet irf540. Disponivel em:  https://www.vishay.com/docs/90183/sihf540.lib

- Quais os limites de tensão para este circuito?

   Os limites de tensão para esse circuito será a própria tensão da fonte retificada, que estará em 17V. A saída do ampop Vout que é especificada pelo projeto para 15V. Importante ressaltar que a tensão sobre o mosfet Vgs será a tensão de saída do ampop subtraída da tensão Vout. 
 
 - Quais as tensões máxima desse componente?
 
   Segundo datasheet:
 
   ![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/Fonte_Linear/imagens/irf540%20vgs.png)
 
   Vds= 100V (máx)
   
   Vgs= +/- 20V (máx)
 
 
 - Justifique a escolha dos resistores R2 e R3.

  Vout= 15V --> requisito do projeto

  Vin= 12,5V --> Regulado pelo diodo zener

  Configuração do ampop é uma não inversora.

  Portanto:

```
Vout= (R2/R3+1)*Vin

Vou/Vin=R2/R3 +1
R2/R3= 15/12,5 -1
R2/R3=0,2

R3=2K
R2=0,2*2000
R2=400


```
 
 A escolha do R3 foi pensada na corrente que vai circular nele. Que será na casa de mA. Tendo o valor de R3 calculei o R2 na formula.
 
 
 # Circuito montado:
 
 ![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/Fonte_Linear/imagens/CIRCUITOCOMPLETO.png)
 
 

## Adicionando um circuito de proteção de sobre corrente ao regulador linear.

- Primeiramente reflita e pesquise sobre o que é sobrecorrente? 

 A sobrecorrente é circulação de excesso de corrente no circuito. Uma corrente que excede o valor nominal
 
- Quais os impactos neste circuito? 
 
 Se um curto circuito ou uma sobrecarga ocorrer pode danificar os componentes do circuito danificando todo o projeto e acabando com a sua eficácia.
 
- O que deve fazer um circuito de proteção de sobrecorrente? 

O circuito de proteção de sobrecorrente deve interromper a corrente que circula no circuito, automaticamente, sempre que a intensidade de corrente atingir valores que
podem causar danos aos demais dispositivos.

- O que é a proteção foldback?

Foldback é uma limitação de corrente. Quando a carga tenta provocar sobrecorrente da alimentação, a proteção foldback reduz a saída de tensão e corrente para bem abaixo dos limites normais de operação. Sob um curto-circuito , em que a tensão de saída é reduzida a zero, a corrente é tipicamente limitados a uma pequena fracção da corrente máxima.

- Pesquise as topologias disponíveis, caso deseja-se fazer um circuito LDO, o o que devemos levar em consideração para o regulador? 




 
 
 



