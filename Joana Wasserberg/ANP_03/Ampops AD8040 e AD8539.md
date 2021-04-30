
# **Simulação de circuitos com Amplificadores operacionais AD8040 e AD8539**
----------------------------------
----------------------------------------
## Informações do Datasheet

### **AD8040**

◦ Máxima e mínima tensão de alimentação 2.7V a 12V


|  Alimentação Simétrica | +/- 5v        |          5V    |     3V         |
|-------:|:-------------:|:--------------:|:--------------:|
Tensão de modo comum| –5.2 a +5.2  | –0.2 a +5.2 V | –0.2 a +3.2 V |
CMRR | 80 a 90dB   | 80 a 90 dB     | 78 a 88 dB     | 
Máx e mín tensão de entrada| +/-Vs +/- 0,5 |  +/-Vs +/- 0,5 |  +/-Vs +/- 0,5 |
Tensão de offset| 1.6 a 5 mV    | 1.4 a 5 mV    | 1.1 a 5 mV        | 
Corrente de polarização| 0.7 a 1.3 μA  | 0.8 a 1.2 µA| 0.7 a 1.2 µA        |
Consumo de corrente| 1.4 a 1.5mA  |  1.3 a 1.5mA |      1.3 a 1.4mA |
Ganho em malha aberta      | 65 a 74 dB    |65 a 74  dB    |64 a 73 dB           |
Impedância                 | 6 MΩ          | 6 MΩ        |6 MΩ               |

### **AD8539**

◦ Máxima e mínima tensão de alimentação 0 a 5,5V


   Alimentação Simétrica   |       5V       |     2.7V   |
--------------------------:|:--------------:|:----------:|
Tensão de modo comum       |    2,5V        | 1,35V      |
CMRR                       | 115 a 135 dB   | 110 a 130dB|
Máx e mín tensão de entrada| 0V e +5V       | 0.2V a 2.5V|
Tensão de offset           | 5 a 15 µV      | 5 a 16µV   |
Corrente de polarização    | 15 a 60 pA     |15 a 25pA   |
Consumo de corrente        |    210 uA      |      210uA |    
Ganho em malha aberta      |110 a 130 dB    |110 a 130dB |
Impedância                 |     ---        |   ---      |

---
---



## Realizando simulações no LTspice AD8539 e AD8040.



1. Simule um circuito seguidor de tensão com cada um dos ampops indicados e verifique os efeitos decorrentes da máxima e mínima tensão de entrada. 
**Responda quais os valores das tensões de saturação?**

Para o AmpOp ad8539, a tensão de saída ficou proxíma de 4.8V. Por conta da tensão de entrada ser 8V, o AmpOp saturou para o lado do VCC de +5V.
 
![Seguidor de tensão ad8539](https://github.com/joananana/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Joana%20Wasserberg/ANP_03/Imagens/Seguidor%20de%20tens%C3%A3o%20ad8539.PNG )



![Seguidor de tensão ad8040]( https://github.com/joananana/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Joana%20Wasserberg/ANP_03/Imagens/Seguidor%20de%20tens%C3%A3o%20ad8040.PNG)

![Seguidor de tensão gráfico](https://github.com/joananana/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Joana%20Wasserberg/ANP_03/Imagens/Seguidor%20de%20tens%C3%A3o%20gr%C3%A1fico.PNG )



2. Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual -100V/V.

+ Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.



Com a tensão de entrada em 0V, a saída do AmpOp ficou proxíma de 1.94mv (AD8539). Isso é por efeito da tensão de offset, que nesse ampop, com o ganho de 100V/V fica proxímo de 0,5mV variando a 1,5mV.

Para o AmpOp AD8040, a tensão ficou em 0.18V, que está de acordo com a tensão de offset esperada para um ganho de 100V/V.

+ Aplique um sinal senoidal de 10mVpp@1kHz na entrada e verifique o sinal de saída. Explique o resultado.

![inversor ad8539](https://github.com/joananana/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Joana%20Wasserberg/ANP_03/Imagens/Inversor%20ad8539.PNG)

Com o sinal de 5mV de amplitude e o ganho em 100V/V a tensão de saída fica 500mV seguido 50mV (AD8439)


![inversor ad8040](https://github.com/joananana/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Joana%20Wasserberg/ANP_03/Imagens/Inversor%20ad8040.PNG)


Apesar de ambos possuirem ganhos na tensão de acordo com a topologia aplicada, o AD8539 foi muito mais preciso.


3. Simule um circuito amplificador não inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual 10V/V.


![não inversor ad8539](https://github.com/joananana/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Joana%20Wasserberg/ANP_03/Imagens/n%C3%A3o%20inversor%20ad8539.PNG)

![não inversor ad8040](https://github.com/joananana/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Joana%20Wasserberg/ANP_03/Imagens/n%C3%A3o%20inversor%20ad8040.PNG)

+ Aplique 0V na entrada e verifique o valor da tensão na saída. Explique o resultado.


Com a tensão de entrada em 0V, a saída do AmpOp ficou proxíma de 216uV (AD8539). Isso é por efeito da tensão de offset, que nesse ampop, com o ganho de 10V/V fica proxímo de 50uV variando a 150uV.

Para o AmpOp AD8040, a tensão de saída ficou 74mV. Isso é por efeito da tensão de offset, que nesse ampop, com o ganho de 10V/V fica proxímo de 50mV variando até 16V.

+ Aplique um sinal continuo de 5mV, 50mV, 200mV e 500mV na entrada e verifique o sinal de saída. Qual o erro com relação ao ganho calculado? Explique o resultado.

AD8539|  |   |
----------:|:--------------:|:--------
|Entrada | Saída | Erro em relação ao ganho
|5mV     | 50.1mV| 0.2%
|50mV    |500.2mV| 0.04%
|200mV   | 2V    |0%
|500mV   | 4.95V |1%

Devida a saturação para o VCC, o ganho esperado em 500mV foi menor.


AD8040|  |   |
----------:|:--------------:|:--------
|Entrada | Saída | Erro em relação ao ganho
|5mV     | 124mV| 148%
|50mV    | 573mV| 14,6%
|200mV   | 2V    |0%
|500mV   | 4.95V |1%


## Caso deseja-se projetar um amplificador subtrator com ganho de 100V/V, para sinais muito pequenos com variação de +/-10uV até +/-30mV de muito baixa frequência, qual desses ampops você utilizaria? Justifique a sua resposta.

Utilizaria o ampop AD8539 por sua precisão ser muito melhor que o ampop AD8040 para sinais pequenos como o proposto.