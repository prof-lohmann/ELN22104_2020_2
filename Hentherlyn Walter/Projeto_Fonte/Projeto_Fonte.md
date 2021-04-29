# Projeto Final

## Parte 1


### Circuito 1

![image](https://user-images.githubusercontent.com/74205954/116479443-076a6880-a856-11eb-97f0-9dab844fc8a4.png)

_Figura 1

#### Qual relação entre a tensão de alimentação do ampop e a tensão de saída?

   A tensão de saída depende da tensão de alimentação do AmpOp, pois o AmpOp tende a saturar quando a tensão de saída se tende à tensão de alimentação.

#### O que devemos considerar para esse circuito operar como um LDO?

   Para este circuito operar como um LDO devemos utilizar a equação ilustrada abaixo.
    
   Vin >= Vout + Vdo
    
   Onde:
   Vin - Tensão de entrada que é limitada pelo diodo Zenner escolhido.
   Vout - Tensão de saída que é limitada pelo AmpOp escolhido.
   Vdo - Tensão do Zenner

#### Como obter as tensões de alimentação para o AmpOp (VCC e VEE)?

   A tensão de alimentação do AmpOp deve ser no mínimo a soma da tensão de saída (Vout) com a tensão de polarização do mosfet (Vgs).

#### Utilizando o circuito dobrador de tensão, qual valor de VCC você obtêm para um sinal Vin+ de 12Vrms?

![image](https://user-images.githubusercontent.com/74205954/116479687-721ba400-a856-11eb-9fd8-a212af7cf0fe.png)

_Figura 2: Circuito de alimentação 1 - dobrador de tensão.

   Para o circuito dobrador de tensão devemos utilizar a equação descrita abaixo:
    
   Vcc = 2*Vin,pico*sqrt(2) - Vdiodo4 - Vdiodo5
   Vcc = 2*12*sqrt(2) - 0,7 - 0,7 = 32,54 V

####  Quais problemas apresentam esse circuito?

   Este circuito apresenta ruído na tensão de saída devido à tensão de ripple existente.

#### Podemos melhorar?

  Podemos melhorar o desempenho do circuito adicionando um regulador linear na saída do dobrador para limitar a tensão de alimentação do AmpOp.

### Circuito 2

#### Alimentação do AmpOp: Considere AmpOp LM324, MOSFET IRF540, VOUT = 15V, IOUT = 1A, vin+ = 12Vrms, vripple_pós_retificador = 1V, considere as quedas de tensão nos diodos de 0,7V

![image](https://user-images.githubusercontent.com/74205954/116482020-b3ae4e00-a85a-11eb-93af-5c4fd1941b02.png)

_Figura 3: Circuito de alimentação 2 proposto.

#### Qual a tensão VGS? Descreva como obter o valor.

   Sabendo que Iout deve ser 1 A, analisando o Datasheet do MOSFET podemos perceber que Vgs deve ser de aproximadamente 4 V.
   
   ![image](https://user-images.githubusercontent.com/74205954/116503853-70b99e00-a88d-11eb-9073-9a3ce0475efc.png)

   _Figura 4: Tensão Vgs - DataSheet Mosfet IRF540.

#### Qual a corrente de alimentação do AmpOp?

   Através do Datasheet do AmpOp LM324, podemos observar que a corrente de alimentação é de 3mA.
   
   ![image](https://user-images.githubusercontent.com/74205954/116504220-33094500-a88e-11eb-92db-0df6cdac7041.png)

   _Figura 5: Corrente de alimantação - DataSheet LM324.

#### Qual a tensão de alimentação do AmpOP?

   Analisando o Datasheet percebemos que a tensão máxima de operação do é AmpOp LM324 é de 32V.
   
   ![image](https://user-images.githubusercontent.com/74205954/116504153-1705a380-a88e-11eb-86b4-93bbe089956f.png)
   
   _Figura 6: Tensão de alimantação - DataSheet LM324.

#### Qual fator devo considerar para escolher o transistor Q1?

   É necessário utilizar um beta bastante elevado, para que a corrente de alimentação do Bjt seja muito menor que a do Zenner, por isso foi escolhido o transistor bipolar de junção 2SC4617.

   ![image](https://user-images.githubusercontent.com/74205954/116504731-65677200-a88f-11eb-9be1-9e96a35666ba.png)


#### Qual valor da tensão do diodo zener D6?
   
   Primeiramente devemos verificar qual deverá ser a tensão de saída do AmpOp. Analisando o circuito podemos perceber que a tensão de saída do AmpOp (Vop) se dá pela soma entre a tensão Vgs do MOSFET e a tensão de saída do circuito (Vout). 
   
   Vop = Vgs + Vout 
   Vop = 4 + 15 = 19
   
   Desta forma, o valor escolhido para a tensão de Zenner deve ser maior que 19V. Pois assim o AmpOp receberá tensão suficiente e conseguirá fornecer 19V na sua saída.
   
   ![image](https://user-images.githubusercontent.com/74205954/116505310-e83cfc80-a890-11eb-809c-98fcb52098a5.png)
   
#### Como escolher o diodo zener D6, maximizando a eficiência energética e minimizando os ruídos no circuito? 

   Para maximizarmos a eficiência energética e minimizarmos os ruídos do circuito devemos escolher um diodo Zenner com a menor resistência possível. Desta forma, mesmo que a corrente varie, a tensão de regulação do Zenner não irá variar tanto.

#### Considere que, por alterações futuras no circuito, o AmpOp poderá ter um aumento de 10mA na corrente de alimentação, o circuito proposto continuará funcionando?

   Como estamos trabalhando com a mínima corrente de alimentação, mesmo com este aumento de corrente o circuito continuará funcionando.

##### Circuito de alimentação montado no LtSpice

   Vp = Vin * sqrt(2) = 12 * sqrt(2) = 16,97 V
   VD = 2 * Vp = 2 * 16,97 = 33,94 V

   Por C2, C3, D4 e D5 se tratarem de um dobrador de tensão, Vripple deve ser uma valor em torno de 32V.

![image](https://user-images.githubusercontent.com/74205954/116502483-f9363f80-a889-11eb-8dca-1ca2b3f207fc.png)

![image](https://user-images.githubusercontent.com/74205954/116502337-9a70c600-a889-11eb-90e5-da417fbed93d.png)

![image](https://user-images.githubusercontent.com/74205954/116502905-26cfb880-a88b-11eb-959f-d1e6b4a22806.png)

## Parte 2


#### A) Para o primeiro bloco (D1, D2 e C1) considere vin+ = 12Vrms, vripple_pós_retificador = 1V e I_carga = 1,1A. Justifique a escolha dos componentes

   Os diodos precisam apresentar uma queda de tensão menor do que 1V, a fim de consumir a menor tensão possível do circuito. Para selecioná-lo devemos realizar alguns cálculos, como a tensão reversa (VD) e a corrente média (Imed).
   
   Vp = Vin * sqrt(2) = 12 * sqrt(2) = 16,97 V
   VD = 2 * Vp = 2 * 16,97 = 33,94 V
   Imed = Icarga * ( 1 + pi * sqrt( Vp/ (2 * Vripple) ) = 1 + pi * sqrt( 16,97 / (2 * 1) = 10,15 A
   
   Para D1 e D2 foi escolhido o diodo 1N4148, que possue uma tensáo reversa minima de 100V.
   
   ![image](https://user-images.githubusercontent.com/74205954/116559074-6d96d000-a8d6-11eb-9f35-463889fb1e35.png)
   
   O capacitor deve ser escolhido com base no retificador, sendo assim:
   
   C1 = Icarga / (2*f*Vripple) =  1,1 / (2*60*1) = 9,17mF
   
#### B) Circuito referência de tensão zener (R1 e D3):

   Calculando R1:
   
   Diodo 1N750 - VD = 5 V; Iz = 20 mA;
   Vdiodo = 0,7 V
   Vz = 4,7 V
   
   V = Vp - 2 * Vdiodo = 16,97 - 1,4 = 15,57 V
   
   R1 = (V - Vz) / Iz = (15,75 - 4,7) / 20m = 543,5 ohms

##### B.1) Quais fatores devo considerar para escolher o diodo zener para essa aplicação? 

   Para escolhermos o Zenner, devemos considerar que ele deve fornecer tensão suficiente para o AmpOp e, além disso, devemos considerar que sua resistência deve ser baixa, para uma melhor regulação e maximização de sua eficiência.

##### B.2) Qual a influência da regulação de linha e da regulação de carga para este circuito?

   A regulação de linha e de carga medem a eficiência do regulador, por isso projetamos o circuito para que ele apresente a menor variação detensão possível e assim a regulação de tensão e carga fique aproximadamente zero.

##### B.3) Qual o impacto da regulação linha / carga do circuito com o diodo zener na tensão de saída do regulador linear? 

   O diodo Zenner será responsável por limitar a tensão de saída a fim de que a variação da tensão de saída seja aproximadamente zero.

  Reg.linha = ΔVout / ΔVin = 0 / ΔVin = 0 V/v
  Reg.carga = ΔVout / ΔIout = 0 / ΔIout = 0 V/A
   
##### B.4) Podemos melhorar esse circuito? Quais problemas podemos identificar nesta topologia?

   O problema é a corrente que gera uma variação de tensçao no diodo Zenner. Poderia resolver casa fosse possível colocar algum componente que mantivesse a corrente constante.
 
### No qual o circuito com R1, R5, Q2 e Q3 é uma fonte de corrente constante para polarizar o diodo zener D3. Vamos projetar?

   ![image](https://user-images.githubusercontent.com/74205954/116562783-d895d600-a8d9-11eb-80d4-0c7c01679d8b.png)
 
#### C) Escolhendo o transistor M1 e calculando R2 e R3.

##### C.1) Qual a corrente contínua necessária?

   A mesma corrente do projeto, 1A.
   
##### C.2) Quais os limites de tensão para este circuito?

   O limite é dado pela tensão de entrada.
 
##### C.3) Quais os os parâmetros L, W, uo, Cox, VA e Vt?
  
   L = 100 uH
   Vt = 3.56 V
   VA = 1/LAMBDA= 1/0.00291031 = 343,6 v
   W = 100 uW
   u0 = Valor Padrão = 600 cm²/V/s
   C0x = KP/u0 = 41,68 mF/m²
  
## Parte 3

##### Primeiramente reflita e pesquise sobre o que é sobrecorrente? Quais os impactos neste circuito?

   A sobrecorrente nada mais é do que o excesso de corrente que ultrapassa as valores nominais. Isso implica em danificar o circuito, podendo ocasionar a queima de alguns componentes.
 
 #### O que deve fazer um circuito de proteção de sobrecorrente? O que é a proteção foldback? O que deve fazer um circuito de proteção de sobrecorrente? O que é a proteção foldback?
   
   O circuito de proteção de sobrecorrente deve ser capaz de proteger todo o circuito enquanto houver sobrecorrente.
   A proteção foldback tende a diminuir a corrente enquanto houver o efeito da sobrecorrente, assim os componentes não geram tanta perda em potência.
   
