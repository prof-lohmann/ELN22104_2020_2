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

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/Fonte_Linear/imagens/vgs_idreno.png)

Conforme o datasheet a tensão Vgs para uma corrente de 1A é de 4V.


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
  
  Considerando que a tensão de saída do ampop deve ser de 21V. Pois Vgs=4V
  
  Logo 15+4= 19V
  A tensão do diodo zener deve ser maior que 19V.
  
  
- Como escolher o diodo zener D6, maximizando a eficiência energética e
minimizando os ruídos no circuito?

Escolhendo um diodo zener que passe a menor corrente possível. Para isso precisa ser um zener com um resistor de zener pequeno

**Projeto no ltspice:**

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/Fonte_Linear/imagens/alimentac_opamp_circ.png)


Observa-se que no circuito a associação de capacitores c2 e c3 com os diodos d3 e d4 formam um multiplicador de tensão retificado, sendo c3 o capacitor responsável por retificar o sinal. Que resulta na label Vcc1



![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/Fonte_Linear/imagens/vripple_aliment.png)

Entretando essa saída sofre com ruídos. Para resolver o problema foi adicionado um regulador de tensão com diodo zener e transistor tbj.

A tensão de ripple simulada é de 1,08V. Para resolver esse problema foi adicionado ao circuito um regulador de tensão com o regulador zener EDZV24B e o transistor tbj BC547C.

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/Fonte_Linear/imagens/vcc2_opamp.png)

Observa-se que a tensão de saída vcc2 ja regulada é estável em aproximadamente 23,75V.

Essa será a tensao de alimentação do ampop.





O diodo zener escolhido tem a tensão de funcionamento de 24V. Portanto atende ao resquisito de Vzener>19V

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


## Escolhendo transistor M1 e calculando R2 e R3:

- Qual a corrente contínua necessária?

  Para o transistor M1 é requisito de projeto que seja de 1A.

- Quais os limites de tensão para este circuito?

   A tensão será limitada pelo ganho da não inversora.
 
 - Quais as tensões máxima desse componente?
 
   Segundo datasheet:
 
   ![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/Fonte_Linear/imagens/irf540%20vgs.png)
 
   Vds= 100V (máx)
   
   Vgs= +/- 20V (máx)
 
 
 - Justifique a escolha dos resistores R2 e R3.

  Vou= 15V --> requisito do projeto

  Vin= 12,5V --> Regulado pelo diodo zener

  Configuração do ampop é uma não inversora.

  Portanto:

```
Vout= (R2/R3+1)*Vin

Vou/Vin=R2/R3 +1
R2/R3= 15/12,5 -1
R2/R3=0,2

R3=1K
R2=0,2*1000
R2=200


```
 
 A escolha do R3 foi pensada na corrente que vai circular nele. Que será na casa de mA. Tendo o valor de R3 calculei o R2 na formula.




 
 
 



