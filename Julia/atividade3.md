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

A fonte segue quase que idealmente, porém fazendo a medição exatamente na crista e no vale, com Vmax=4.998245 e Vmin=-4.997561, e um offset de 1.75mV no máximo e 2.44mV no mínimo, dentro do especificado pelo datasheet, com valor típico de 1.60mV porém máximo de 5mV.

Abaixo temos um segundo gráfico, com a alimentação do AmpOp de modo especificado pelo datasheet, porém foi aplicado 6V na fonte utilizada na entrada não inversora. Assim podemos perceber como a saturação fica evidente.

![grafico2](https://github.com/Julialcomelli/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Julia/quest%C3%A3o%202%20-%20AD8040%20com%20satura%C3%A7%C3%A3o%20grafico.png)

### AD8539 

![circuito3](https://github.com/Julialcomelli/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Julia/quest%C3%A3o%202%20-%20AD8539%20circuito.png)

Usamos alimentação de ±2.5V e a fonte na entrada não inversora foi de 2.5V com frequência de 1kHz. A partir de 2.5V temos uma saturação. Abaixo temos um gráfico mostrando a tensão em Vout quando temos 2.6V no AD8539 (quando já está saturado).

![grafico3](https://github.com/Julialcomelli/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Julia/quest%C3%A3o%202%20-%20AD8539%20grafico.png)

Assim, notamos que o limite de funcionamento apresentado nos dois Amplificadores operacionais é sempre igual a soma das tensões de alimentação, caso seja duplamente alimentado, ou igual a alimentação simples do AmpOp. Acima desses valores sempre ocorrerá a saturação do componente.

## 3. Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual -100V/V.

Ao aplicar 0V no circuito com o AD 8040, obtemos Vout=-169,90mV. Como o valor do offset é 100 vezes menor do que o valor de Vout, fica 1,7mV, o que condiz com o offset apresentado pelo datasheet. Aplicando 0V no circuito com o AD 8539, obtemos Vout=1,38mV. Como o valor medido em Vout é 100 vezes o offset,assim fica 13uV.

Aplicando um sinal senoidal de 10mVpp@1kHz temos o seguinte resultado:

### AD8040

![circuito4](https://github.com/Julialcomelli/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Julia/quest%C3%A3o%203%20-%20AD8040%20circuito.png)

Ao colocar uma onda senoidal de 10mVpp, deveríamos obter no seu vale -500mV e em sua crista 500mV. Porém, obtemos o seguinte gráfico ao simular o circuito:

![grafico4](https://github.com/Julialcomelli/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Julia/quest%C3%A3o%203%20-%20AD8040%20grafico.png)

Com um offset de 1.60mV em um ganho de -100V/V, obtemos cerca de -160mV no gráfico de análise do circuito. No gráfico do SPICE, encontramos o valor de Vmin = -668,26mV e Vmax = 327,68mV, o que nos dá aproximadamente o offset amplificado

### AD8539

![circuito5](https://github.com/Julialcomelli/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Julia/quest%C3%A3o%203%20-%20AD8539%20circuito.png)

Neste circuito, novamente teríamos um circuito ideal em -500mV de valor mínimo e 500mV de valor máximo. O gráfico analisado é o seguinte:

![grafico5](https://github.com/Julialcomelli/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Julia/quest%C3%A3o%203%20-%20AD8539%20grafico.png)

Haviamos obtido um offset de 1,38mV. Obtendo o relatório do SPICE, chegamos ao valor máximo de Vmax = 493,57mV e Vmin = -492,04mV. Isso nos dá um offset maior do que o previsto em simulação. 

## 4. Simule um circuito amplificador não inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual 10V/V.

![circuito6](https://github.com/Julialcomelli/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Julia/questao%204%20AD8040.jpeg)
Utilizamos um resistor de 9k Ohm na realimentação e um de 1k Ohm na entrada inversora indo ao terra. Aplicando 0V na entrada, temos o valor de aproximadamente -15,3mV na saída Vout. O offset foi negativo, e está dentro do especificado pelo datasheet.

Aplicando sinais contínuos, obtemos:

+ 5mV - Vout = 34,7mV
+ 50mV - Vout = 484,6mV
+ 200mV - Vout = 1,98V
+ 500mV - Vout = 4,97V

Os erros em relação ao ganho é:

+ 5mv - 30,6%
+ 50mV - 3,08%
+ 200mV - 1%
+ 500mV - 0,6%
