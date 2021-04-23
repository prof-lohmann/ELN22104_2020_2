# ELN22104 - Atividade 02

## Luiz Gustavo Erthal

## Resumo sobre Amplificadores Operacionais (AmpOps)

## 1. O que é o AmpOp?

Um amplificador operacional, ou AmpOp, é um amplificador diferencial de ganho muito alto com impedância de entrada muito alta e baixa impedância de saída. Utilizações típicas do AmpOp compreendem desde alterações em valores de tensões, osciladores, filtros e outras instrumentações.

## 2. Mostre os simbolos e as características do AmpOp IDEAL?

Um AmpOp ideal possui cinco terminais, sendo dois de entrada (inversora [-] e não inversora [+]), dois de alimentação [Vcc e -Vee] e um terminal de saída.

![Ex2](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%202%20-%20Ex2.png)

## 3. O que significa Malha Aberta e Malha Fechada?

- Malha Aberta

É uma configuração em que o amplificador operacional não possui realimentação, seja essa negativa ou positiva. Geralmente, os ganhos nessa configurações são muito altos.

-  Malha Fechada

Diferentemente da de malha aberta, esta é uma configuração em que o amplificador operacional possui realimentação, sendo essa geralmente negativa (entrada inversora). Nesse caso, os ganhos não são tão altos quanto os de malha fechada.

## 4. Exemplifique como resolver e calcular circuitos com AmpOps em Malha Fechada.

![Ex4](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%202%20-%20Ex4.png)

Assumindo que se trata de um AmpOp ideal, com ganho infinito, um curto-circuito virtual existe entre os dois terminais de entrada. 
Ou seja, (1) Vld = 0. Não há corrente na entrada inversora. O resistor R2 e resistor R1 compartilham da mesma corrente. Podemos então calcular o ganho a partir desses dois.

> V0 = V1 + (V1/R1)*R2

> V0 = V1*[1 + (R2/R2)]

## 5. Descreva as principais características das topologias:

​	a. **Seguidor de Tensão** _(Buffer)_

Um circuito _buffer_ fornece um meio de isolar um sinal de entrada de uma carga ao utilizar um estágio com ganho unitário de tensão, agindo como um circuito ideal. A tensão é dada por:

> V0 = V1

![Ex5a](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%202%20-%20Ex5a.png)

​	b. **Amplificador Inversor**

![Ex5b](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%2002%20-%20Ex5b.png)

Considerando que o ganho nessa configuração em malha fechada será G = V0/V1.
Em (1) sabemos que a impedância é muito alta, ou seja, não há corrente que vá para a entrada inversora. A corrente i1 é a mesma de i2. Logo:

> V0 = - (R2/R1)*V1


c. **Amplificador Não Inversor**

![Ex5c](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%202%20-%20Ex5c.png)

Desta vez, a entrada inversora está aterrada. Como a diferença de potencial em (1) continua sendo zero, a corrente fluí de V0 para o terra (3). As correntes são novamente as mesmas para as resistores.
> V0 = V1 [1 + (R2/R1)]

d. **Amplificador Somador Inversor**

![Ex5d](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%202%20-%20Ex5d.png)

Sua função é a de realizar a soma das tensões das entradas no terminal inversos do AmpOp. 

O seu ganho é dado por: A = -Rf/R1 e sua tensão de saída - Vout - é dada por:

Vout = -(Rf/R1) * V_ 

e. **Amplificador Somador Não Inversor**

![Ex5e](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%202%20-%20Ex5e.png)

Ao contrário do último amplificador explanado, o somador não inversor realiza a soma das tensões no terminal não-inversor. Seu ganho é dado por:

A = 1 + (Rf / R1), e sua tensão de saída - Vout - é dada por: 

Vout = A * V+

f. **Subtrator**

Este AmpOp tem como função subtrair os sinais de tensão das entradas inversoras e não-inversoras dos amplificadores operacionais.

g. **Amplificador de Instrumentação**

É uma versão precisa do amplificador operacional subtrator que não apresenta tantos defeitos ou erros. 

## 6 . Explique o efeito de ganho em **MALHA ABERTA FINITO** para as topologias Amplificador Inversor e Amplificador Não Inversor

O ganho em malha aberta finito é uma das consequências das não-idealidades dos AmpOp, mesmo que tratemos muitas vezes esses dispositivos eletrônicos como ideais, eles ainda são reais e apresentam falhas ou diferenças de performance. Considerando as duas topologias, podemos considerar algumas não idealidades - tensão de offset, tensão de modo comum ou correntes de polarização - para citar algumas. 

**Amplificador Inversor** *NÃO IDEAL* - ERROS:

|  Av  | \|-R2/R1\| | \|G\| | **∆**% |
| :--: | :--------: | :---: | :----: |
| 1000 |    1000    |  909  |  9,1%  |
| 100  |    1000    | 90,83 | 90,9%  |

**Amplificador Não Inversor ** *NÃO IDEAL* - ERROS:

|  Av  | 1 + (R2/R1) |  G   | **∆**% |
| :--: | :---------: | :--: | :----: |
| 1000 |    1000     | 909  |  9,1%  |
| 100  |    1000     | 90,9 | 90,9%  |

## 7. Explique o que é a tensão de modo comum (Vcm) e quais os efeitos desta tensão nas topologias estudadas:

É um dos principais problemas que o Amplificador Subtrator apresenta, são tensões idênticas (fase e módulo) nas entradas inversoras e não inversoras. Ela é calculada da seguinte forma: Vcm = [(Vin+ + Vin-) / 2]. A tensão de modo comum acaba surgindo nas saídas amplificadas por um ganho em modo comum, idealmente zero, como um acréscimo das tensões de entrada.

## 8. O que é **CMRR**?

Common Mode Rejection Ratio (Razão de Rejeição em Modo Comum) é uma característica importante dos AmpOp que define a razão do ganho em modo comum do amplificador em relação ao seu ganho em malha aberta, sendo o ganho de modo comum idealmente nulo.

## 10. Explique as limitações de tensão de entrada e saída de um AmpOp. 

Os AmpOp apresentam algumas limitações nas suas tensões de entrada e saída por causa de suas tensões de modo comum e as oscilações das tensões de saída. 

![Ex10](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%202%20-%20Ex.10.png)

### a. Defina o que é um **AmpOp Rail-to-Rail**

São AmpOps que apresentam alimentação dupla e simétrica, com +VCC no terminal de alimentação positivo e -VCC no terminal de alimentação negativa. 

## 11. O que é **Tensão de offset**? Como calcular o efeito resultante na tensão de saída de um amplificador inversor?

É uma tensão parasita no terminal de Vout do dispositivo que ocorre por descasamento de transistores nos terminais de entrada do AmpOp durante a fabricação. Podemos calcular o efeito resultante em um AmpOp inversor aterrando seu terminal de entrada e verificando seu offset que estará sendo multiplicado pelo seu ganho. Para calcular, basta utilizar o teorema da superposição, onde anulamos uma fonte de cada vez para verificar seu trabalho exercido no final separadamente.

## 12. Como minimizar o efeito da **tensão de offset**?

Em alguns AmpOp, há um potenciômetro que é capaz de ajustar a sua tensão de offset, porém,sua produção não é escalável. Podemos então colocar uma fonte de sinal contrário em sua entrada (CC) ou utilizar um capacitor para minimizar o efeito (CA).

## 13. O que é a variação da tensão de offset pela temperatura?

É importante voltar alguns conceitos. Amplificadores Operacionais são produzidos "a base" de transistores, que são componentes eletrônico desenvolvidos de Sílicio (Si), que é um supercondutor. Supercondutores são extremamente sensíveis a temperatura, e variam suas características elétricas com base nisso. Por causa disso, a variação de temperatura ocasiona o descasamento desses transistores, como explicado na questão anterior, que ocasiona as tensões de offset. Em geral, nos datasheets, é possível verificar gráficos das variações das tensão de offset por temperatura.

## 14. O que são **correntes de polarização** de AmpOp?

Idealmente, não há corrente nos terminais de entrada de um AmpOp. Porém, a realidade é outra, é há sim uma certa passagem de corrente muito pequenas por esses terminais, em algumas aplicações são desprezadas.