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

TEXTO TEXTO TEXTO

![Ex3B](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex3AD8040B.png)

![Ex3C](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex3AD8040Sim2.png)

AAAAA

**AD8539**

![Ex3D](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex3AD8539.png)

![Ex3E](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex3AD8539Sim.png)

aaaa

### 4) Simule um circuito amplificador não inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual 10V/V.

**AD8040**

![Ex4](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex4AD8040.png)

AAAAA

TABELA

![Ex4A](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex4AD8040Sim.png)

![Ex4B](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex4AD8040Sim2.png)

![Ex4C](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex4AD8040Sim3.png)

![Ex4D](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex4AD8040Sim4.png)

**AD8539**

![Ex4E](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex4AD8539.png)

AAAAAA

TABELA

![Ex4A](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex4AD8539Sim.png)

![Ex4A](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex4AD8539Sim2.png)

![Ex4A](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex4AD8539Sim3.png)

![Ex4A](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%203%20-%20Ex4AD8539Sim4.png)



