# ELN22104 - Atividade 02

## Luiz Gustavo Erthal

## Resumo sobre Amplificadores Operacionais (AmpOps)

### 1. O que é o AmpOp?

Um amplificador operacional, ou ampop, é um amplificador diferencial de ganho muito alto com impedância de entrada muito alta e baixa impedância de saída. Utilizações típicas do AmpOp compreendem desde alterações em valores de tensões, osciladores, filtros e outras instrumentações.

### 2. Mostre os simbolos e as características do AmpOp IDEAL?

Um AmpOp ideal possui cinco terminais, sendo dois de entrada (inversora [-] e não inversora [+]), dois de alimentação [Vcc e -Vee] e um terminal de saída.

![Ex2](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%202%20-%20Ex2.png)

### 3. O que significa Malha Aberta e Malha Fechada?

- Malha Aberta

É uma configuração em que o amplificador operacional não possui realimentação, seja essa negativa ou positiva. Geralmente, os ganhos nessa configurações são muito altos.

-  Malha Fechada

Diferentemente da de malha aberta, esta é uma configuração em que o amplificador operacional possui realimentação, sendo essa geralmente negativa (entrada inversora). Nesse caso, os ganhos não são tão altos quanto os de malha fechada.

### 4. Exemplifique como resolver e calcular circuitos com AmpOps em Malha Fechada.

![Ex4](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%202%20-%20Ex4.png)

Assumindo que se trata de um AmpOp ideal, com ganho infinito, um curto-circuito virtual existe entre os dois terminais de entrada. 
Ou seja, (1) Vld = 0. Não há corrente na entrada inversora. O resistor R2 e resistor R1 compartilham da mesma corrente. Podemos então calcular o ganho a partir desses dois.

> V0 = V1 + (V1/R1)*R2

> V0 = V1*[1 + (R2/R2)]

### 5. Descreva as principais características das topologias:

​	a. **Seguidor de Tensão** _(Buffer)_

Um circuito _buffer_ fornece um meio de isolar um sinal de entrada de uma carga ao utilizar um estágio com ganho unitário de tensão, agindo como um circuito ideal. A tensão é dada por:

> V0 = V1

![Ex5a](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%202%20-%20Ex5a.png)

​	b. **Amplificador Inversor**




