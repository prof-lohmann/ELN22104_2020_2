# Atividade 03

## Aluno: Luiz Gustavo Erthal

### Simulação de circuitos com Amplificadores operacionais AD8040 e AD8539.

### 1. Verifique no datasheet dos Ampops indicados os valores dos itens abaixo:

|            CARACTERÍSTICAS            |    AD8040     |    AD8539    |
| :-----------------------------------: | :-----------: | :----------: |
| Máxima e mínima tensão de alimentação |  2,7V a 12V   | 2,7V a 5,5V  |
|         Tensão em modo comum          | -0,2V a +5,2V |    0 a 5V    |
|                 CMRR                  | -4,5V a 3,0V  |    0 a 5V    |
|   Máxima e mínima tensão de entrada   | 200mV (ambos) |    0 a 5V    |
|           Tensão de offset            |      6mV      |     15µV     |
|        Corrente de polarização        | 0,7A a 1,5µA  |  25A a 60pA  |
|          Consumo de corrente          |     1,3mA     |    180µA     |
|         Ganho em malha aberta         | -4,0V a 4,0V  |  0,1V a 7v   |
|         Impedância de entrada         |   6MΩ e 2pF   | 10KΩ e 300pF |

2. ### Simule um circuito seguidor de tensão com cada um dos ampops indicados e verifique os efeitos decorrentes da máxima e mínima tensão de entrada.

   **AD8040**

   ![Ex2](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex2AD8040.png)

   ![Ex2A](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex2AD8040Sim.png)

   Utilizando-se +5V e -5V nos terminais de alimentação do AmpOp - como especificado no datasheet do fabricante. 

   |         Tensão Máxima         | **4,998V**  |
   | :---------------------------: | :---------: |
   |       **Tensão Mínima**       | **-4,997V** |
   | **Tensão de offset (Máximo)** | **1,75mV**  |
   | **Tensão de offset (Mínimo)** | **2,44mV**  |

   

**AD8539**

![Ex2B](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex2AD8539.png)

![Ex2C](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex2AD8539Sim.png)

Nesse caso, é bem evidente que o AmpOp já está trabalhando na área de saturação.

### 3. Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual -100V/V.

**AD8040**

![Ex3](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex3AD8040.png)

![Ex3A](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex3AD8040Sim.png)

Ao se aplicar 0V na entrada inversora do AmpOp, obtemos uma tensão de saída de aprox. -169,90mV. Ou seja, isto já com a diferença do offset aplicado que é 100 vezes menor que o valor da nossa tensão de saída.

![Ex3B](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex3AD8040B.png)

![Ex3C](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex3AD8040Sim2.png)

É importante notar a diferença dos valores de pico nos vales e cristas (máximos e mínimos). Em um circuito de ganho -100V/V - com uma fonte senoidal de 10mVpp - idealmente deveríamos obter 500mV (positivo ou negativo) em seus vales e cristas, porém, por causa do offset de 1.60mV com um ganho de -100V/V, obtemos um offset total de -160mV. **(0,0016 * - 100 = 160mV)**

É notado ao ver que o vale é aproximadamente -660mV e sua crista é aproximadamente 320mV, isto se dá pela adição da tensão de offset.

**AD8539**

Ao se aplicar 0V na entrada inversora do AmpOp, obtemos uma tensão de saída de aproximadamente 1,38mV. Ou seja, isto já com a diferença do offset aplicado que é 100 vezes menor que o valor da nossa tensão de saída.

![Ex3D](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex3AD8539.png)

![Ex3E](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex3AD8539Sim.png)

O mesmo ocorre no AD8539, porém, como sua tensão de offset é muito menor que o do AD8040, obtemos uma tensão de offset máxima de 1,38mV. O que justifica os valores sempre abaixo de 500mV (máximo e mínimo).

### 4) Simule um circuito amplificador não inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual 10V/V.

**AD8040**

![Ex4](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex4AD8040.png)

Utilizando a fórmula do amplificador não inversor para se chegar ao resultado dos resistores, ao aplicar 0V em seu terminal de entrada, encontramos aproximadamente -15,3mV na tensão de saída - por causa da sua tensão de offset - já que idealmente, o ganho deveria ser de 10V/V.

Abaixo, se encontra uma tabela e as simulações com os mais diversos valores de sinais aplicados.

| Tensão Aplicada | Tensão de saída | Erro % |
| :-------------: | :-------------: | :----: |
|       5mv       |     34,7mV      |  31%   |
|      50mV       |     484,7mV     |  3,1%  |
|      200mV      |     1,9846V     |   1%   |
|      500mV      |     4,9664V     |  0,6%  |

![Ex4A](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex4AD8040Sim.png)

![Ex4B](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex4AD8040Sim2.png)

![Ex4C](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex4AD8040Sim3.png)

![Ex4D](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex4AD8040Sim4.png)

**AD8539**

![Ex4E](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex4AD8539.png)

Igualmente ao circuito e simulação anterior, mas desta vez utilizando o AmpOp AD8539, ao aplicar 0V no terminal de entrada, obtemos uma tensão de saída igual a 137uV. 

Abaixo, há a tabela e as simulações com os mais diferentes níveis de tensões aplicadas no circuitos.

| Tensão Aplicada | Tensão de Saída |  Erro %  |
| :-------------: | :-------------: | :------: |
|       5mV       |     50,3mV      |  0,28%   |
|      50mV       |     500,3mV     |  0,028%  |
|      200mV      |     2,0002V     |  0,005%  |
|      500mV      |    Saturado     | Saturado |

![Ex4A](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex4AD8539Sim.png)

![Ex4A](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex4AD8539Sim2.png)

![Ex4A](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex4AD8539Sim3.png)

![Ex4A](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex4AD8539Sim4.png)



## Caso deseja-se projetar um amplificador subtrator com ganho de 100V/V, para sinais muito pequenos com variação de +/-10uV até +/-30mV de muito baixa frequência, qual desses ampops você utilizaria? Justifique a sua resposta. 

Com essas especificações - baixas tensões e de muito baixa frequência - o mais correto seria olhar qual possui a menor **tensão de offset** dos dois exemplares analisados. Pela tabela inicial, vemos que o AD8040 possuí uma tensão de offset de 6mV e o AD8539 de 15µV, logo, o escolhido seria o *AD8539* por possuir uma tensão de offset inúmeras vezes mais baixa.

## Escolha um terceiro ampop com características melhores que os ampops acima para uma aplicação como subtrator.

Indo pela mesma explicação do item anterior, o **LTC 2063** possuí uma tensão de offset de 1µV típica e um máximo de 5µV.

Referência:

https://www.analog.com/media/en/technical-documentation/data-sheets/ltc2063-2064-2065.pdf