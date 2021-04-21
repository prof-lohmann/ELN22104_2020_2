# Atividade 3

## 1) Verifique no datasheet dos Ampops indicados os valores dos itens abaixo:

#### AD8040:

Máxima e mínima tensão de alimentação: 2,7 V a 12,0 V

Tensão de modo comum: -0,2 V a +5,2 V

CMRR: -4,5 V a 3,0 V

Máxima e mínima tensão de entrada: 200mV acima ou abaixo de Vc

Tensão de offset: 6 mV

Corrente de polarização: 0,7 A a 1,5 µA

Consumo de corrente: 1,3 mA

Ganho em malha aberta: -4,0 V a 4,0 V

Impedância de entrada: 6 MΩ e 2 pF


#### AD8539

Máxima e mínima tensão de alimentação: 2,7 V a 5,5 V

Tensão de modo comum: 0 a 5 V

CMRR: 0 a 5 V

Máxima e mínima tensão de entrada: 0 a 5 V

Tensão de offset: 15 µV

Corrente de polarização: 25 a 60 pA

Consumo de corrente: 180 µA

Ganho em malha aberta: 0,1 a 7 V

Impedância de entrada: 10 kΩ e 300 pF

### 2) Simule um circuito seguidor de tensão com cada um dos ampops indicados e verifique os efeitos decorrentes da máxima e mínima tensão de entrada.
### 1. Dica utilize um sinal senoidal de 1kHz para auxiliar na visualização.
### 2. Responda quais os valores das tensões de saturação?

#### AD8040:

![Circuito AD8040](https://github.com/larissasander/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Simula%C3%A7%C3%A3o%20-%20Quest%C3%A3o%202%20-%20AD8040.png)

Para alimentação do AmpOp, foi utilizado -5V na entrada -V e 5V na entrada +V, seguindo as especificações encontradas no datasheet, observando as tensões da entrada não inversora, foi possível verificar que o AmpOp trabalha fora da saturação no máximo em ±5V. No gráfico abaixo, está o funcionamento do AD8040 como um seguidor de tensão. 

![Gráfico AD8040](https://github.com/larissasander/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Larissa%20Sander/Gr%C3%A1fico%20-%20Quest%C3%A3o%202%20-%20AD8040.png)

Temos  Vmáx = 4,9982 V, Vmin = -4,9975 V, offset de 1,75 mV no máximo e 2,44 mV no mínimo, de acordo com as especificações encontradas no datasheet. 

No gráfico abaixo foi aplicado 6 V na fonte na entrada não inversora, mantendo a alimentação do AmpOp especificada pelo datasheet, onde fica evidenciado a saturação.

![Gráfico saturação AD8040](https://github.com/larissasander/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Larissa%20Sander/Gr%C3%A1fico%20satura%C3%A7%C3%A3o%20-%20Quest%C3%A3o%202%20-%20AD8040.png)

#### AD8539:

![Circuito AD8539](https://github.com/larissasander/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Larissa%20Sander/Simula%C3%A7%C3%A3o%20-%20Quest%C3%A3o%202%20-%20AD8539.png)

Foi utilizado na alimentação -5 V na entrada -V e 5V na entrada +V, foi utilizado na fonte na entrada não inversora uma tensão de 2,5 V com frequência de 1 kHz. Temos então saturação a partir de 2,5 V. Abaixo se encontra um gráfico que mostra a tensão em Vout utilizando uma tensão de 2,6 V, ou seja, quando já está saturado.

![Gráfico AD8539](https://github.com/larissasander/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Larissa%20Sander/Gr%C3%A1fico%20-%20Quest%C3%A3o%202%20-%20AD8539.png)

### 3) Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual -100V/V.
### 1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.
### 2. Aplique um sinal senoidal de 10mVpp@1kHz na entrada e verifique o sinal de saída.
### Explique o resultado.

![Gráfico](https://github.com/larissasander/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Larissa%20Sander/Simula%C3%A7%C3%A3o%20%200V-%20Quest%C3%A3o%203%20-%20AD8040.png)

Aplicando 0 V no circuito com o AmpOp 8040 temos que Vout = -169,90 mV e aplicando Vout no circuito com o AmpOp 8538 temos Vout =  -1,38 mV, estes valores estão sendo sempre multiplicados pelo ganho, sendo assim, o valor de offset é 100 vezes menor do que o valor de Vout, obtemos assim 1,7 mV para o AD8040 e 1,3 uV para o AD8539, sendo correspodente ao que foi encontrado no datasheet de cada um. Obtemos estes resultados pois utilizamos um circuito inversor que possui ganho de -100V/V.

#### AD8040

![Circuito AD8040](https://github.com/larissasander/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Larissa%20Sander/Simula%C3%A7%C3%A3o%20-%20Quest%C3%A3o%203%20-%20AD8040.png)

No circuito com ganho de -100V/V ao aplicar uma onda senoidal de 10mVpp, seria ideal obter no seu vale -500 mV e em sua crista 500mv, mas ao simular o circuito obtemos o seguinte gráfico:

![Gráfico 8040](https://github.com/larissasander/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Larissa%20Sander/Gr%C3%A1fico%20-%20Quest%C3%A3o%203%20-%20AD8040.png)

#### AD8539

![Circuito AD8539](https://github.com/larissasander/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Larissa%20Sander/Simula%C3%A7%C3%A3o%20-%20Quest%C3%A3o%203%20-%20AD8539.png)

Neste circuito teríamos novamente no seu vale -500 mV e em sua crista 500mv. Podemos observar no gráfico abaixo: 

![Gráfico 8539](https://github.com/larissasander/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Larissa%20Sander/Gr%C3%A1fico%20-%20Quest%C3%A3o%203%20-%20AD8539.png)


### 4) Simule um circuito amplificador não inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual 10V/V.
### 1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.
### 2. Aplique um sinal continuo de 5mV, 50mV, 200mV e 500mV na entrada e verifique o sinal de saída. Qual o erro com relação ao ganho calculado? Explique o resultado.

#### AD8040
Como temos que o ganho é G = 1 + R2/R1, utilizando um resistor de 9kΩ na realimentação e um de 1kΩ a entrada inversora, obtendo então um ganho de 10/V. Aplicando 0V na entrada obtemos -15,3mV na saída Vout, devido o offset do AmpOp.

![Circuito 8040](https://github.com/larissasander/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Larissa%20Sander/Simula%C3%A7%C3%A3o%20-%20Quest%C3%A3o%204%20-%20AD8040.png)

Aplicando os sinais pedidos na questão, foi obtido os seguintes sinais de saída:

![Gráfico AD40](https://github.com/larissasander/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Larissa%20Sander/Gr%C3%A1fico%20-%20Quest%C3%A3o%204%20-%20AD8040.png)

No gráfico acima está um exemplo aplicando 5 mV.

5 mV - Vout = 34,7 mV

50 mV - Vout = 484,65 mV

200 mV - Vout = 1,9846 V

500 mV - Vout = 4,966 V

Temos que os erros em relação ao ganho são:

5mv - 30,6%

50mV - 3,08%

200mV - 1%

500mV - 0,6%

#### AD8539

![Circuito AD8539](https://github.com/larissasander/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Larissa%20Sander/Simula%C3%A7%C3%A3o%20-%20Quest%C3%A3o%204%20-%20AD8539.png)


5 mV -> Vout = 50,3 mV

50 mV -> Vout = 500,3 mV

200 mV -> Vout = 2,0002 V

500 mV -> Vout = 4,963 V (Saturou)


Temos que os erros em relação ao ganho são:

5mv - 0,28%

50mV - 0,028%

200mV - 0,005%

500mV - Saturou



### Caso deseja-se projetar um amplificador subtrator com ganho de 100V/V, para sinais muito pequenos com variação de +/-10uV até +/-30mV de muito baixa frequência, qual desses ampops você utilizaria? Justifique a sua resposta. Escolha um terceiro ampop com características melhores que os ampops acima para uma aplicação como subtrator.


Utilizaria o AD8539, pois apresenta um offset menor que o do AD8040.

Escolheria o modelo LTC 2063 da Analog, pois possui um offset típico em 1uV e chega ao máximo em 5uV, como podemos ver na especificação no seu datasheet. Utilizando ele nesta faixa de tensão com um ganhi de 100V/V, ele não iria saturar.

![Datasheet](https://github.com/larissasander/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Larissa%20Sander/Datasheet%20LTC2063.png)



