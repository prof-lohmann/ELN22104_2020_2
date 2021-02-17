# ATIVIDADE 3

## 1. Verifique no datasheet dos Ampops indicados os valores dos itens abaixo:

### AD8040

+ Máxima e mínima tensão de alimentação: 2,7 V a 12,0 V
+ Tensão de modo comum: -0,2 V a +5,2 V
+ CMRR: -4,5 V a 3,0 V
+ Máxima e mínima tensão de entrada: 200mV acima ou abaixo de Vc
+ Tensão de offset: 6mV
+ Corrente de polarização: 0,7 A a 1,5 µA
+ Consumo de corrente: 1,3 mA
+ Ganho em malha aberta: -4,0 V a 4,0 V
+ Impedância de entrada: 6 MΩ e 2 pF

### AD8539

+ Máxima e mínima tensão de alimentação: 2,7 V a 5,5 V
+ Tensão de modo comum: 0 V a 5 V
+ CMRR: 0 V a 5 V
+ Máxima e mínima tensão de entrada: 0 V a 5 V
+ Tensão de offset: 15 µV
+ Corrente de polarização: 25 A a 60 pA
+ Consumo de corrente: 180 µA
+ Ganho em malha aberta: 0,1 V a 7 V
+ Impedância de entrada: 10 kΩ e 300 pF

## 2. Simule um circuito seguidor de tensão com cada um dos ampops indicados e verifique os efeitos decorrentes da máxima e mínima tensão de entrada. 

### AD8040

![circuito1](https://github.com/Julialcomelli/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Julia/quest%C3%A3o%202%20-%20AD8040%20sem%20satura%C3%A7%C3%A3o%20circuito.png)

A alimentação utilizada no AmpOp foi de -5V na entrada V- e 5V na entrada V+ . O AmpOp trabalha fora da saturação no máximo em ±5V. Acima disso, vemos a tensão sendo ceifada no pico de no máximo 5V. No gráfico abaixo podemos perceber o funcionamento do AD8040 como um seguidor de tensão, para uma fon te de 5V com frequência de 1kHz (totalizando 10Vpp).

![grafico1](https://github.com/Julialcomelli/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Julia/quest%C3%A3o%202%20-%20AD8040%20sem%20satura%C3%A7%C3%A3o%20grafico.png)
