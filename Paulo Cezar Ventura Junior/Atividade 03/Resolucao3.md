# Atividade 3
Aluno:
* Paulo Cezar Ventura Junior - <paulo.cvj@aluno.ifsc.edu.br>

Professores:
* Daniel Lohmann

### O relatório consiste em um estudo com relação aos Amplificadores operacionais modelos AD8040 e AD8539.

## AD8040
```
Máxima e mínima tensão de alimentação: 2,7 a 12,0 V
Tensão de modo comum: -5,2 a 5,2 V
CMRR: Vcm = -4,5 a 3,0 V
Máxima e mínima tensão de entrada: 200 mV acima ou abaixo
Tensão de offset: Máximo de 6 mV
Corrente de polarização: 0,7 a 1,3 uA
Consumo de corrente: 1,3 mA
Ganho em malha aberta: Vo = -4,0 a 4,0 V, 74 dB
Resistência de entrada: 6M Ohm
```

## AD8539
```
Máxima e mínima tensão de alimentação: 2,7 a 5,5 V
Tensão de modo comum: 0 a 2,7 V ---------- CORRIGIR
CMRR: Vcm = 0 a 2,5 V
Máxima e mínima tensão de entrada: 0 a 2,7 V
Tensão de offset: Máximo de 13 uV
Corrente de polarização: 15 a 25 pA
Consumo de corrente: 180 uA
Ganho em malha aberta: Não foi encontrado
Resistência de entrada: Não foram encontrados dados
```

## 2. Simule um circuito seguidor de tensão com cada um dos ampops indicados e verifique os efeitos decorrentes da máxima e mínima tensão de entrada.

## AD8040

![cir_1_ad8040](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2003/Exemplos/cir_1_ad8040.png)

A alimentação utilizada no AmpOp foi de -5V na entrada V- e 5V na entrada V+ (de acordo com as especificações do datasheet). Ao verificar as tensões da entrada não inversora, podemos observar que o AmpOp trabalha fora da saturação no máximo em ±5V. Acima disso, podemos observar essa tensão sendo ceifada no pico de no máximo 5V, justamente por ser a tensão limite de alimentação. No gráfico abaixo podemos perceber o funcionamento do AD8040 como um seguidor de tensão, para uma fonte de 5V com frequência de 1kHz (totalizando 10Vpp).

![ad8040_5v](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2003/Exemplos/ad8040_5v.png)

Como podemos observar, a fonte segue quase que idealmente, porém fazendo a medição exatamente na crista e no vale, obtemos um valor máximo de Vmax=4.998245 e um valor mínimo de Vmin=-4.997561, onde temos um offset de 1.75mV no máximo e 2.44mV no mínimo, nos indicando que está dentro do especificado pelo datasheet, onde mostra um valor típico de 1.60mV porém máximo de 5mV.

Abaixo temos um segundo gráfico, onde foi aplicado 6V na fonte utilizada na entrada não inversora, porém continuamos com a alimentação do AmpOp de modo especificado pelo datasheet.

![ad8040_6v](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2003/Exemplos/ad8040_6v.png)

Como podemos perceber, a saturação já é bem evidente.


## AD8539

![cir_1_ad8539](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2003/Exemplos/cir_1_ad8539.png)

No AD 8539 utilizamos alimentação de ±2.5V. A fonte na entrada não inversora foi de 2.5V com frequência de 1kHz. Dessa forma, temos uma saturação somente a partir de 2.5V, e não antes disso. Abaixo temos um gráfico mostrando a tensão em Vout quando temos 2.6V no AD8539 (quando já está saturado).

![ad8539_satura](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2003/Exemplos/ad8539_satura.png)

Portanto, dessa forma, notamos que o limite de funcionamento apresentado nos dois Amplificadores operacionais é sempre igual a soma das tensões de alimentação, caso seja duplamente alimentado, ou igual a alimentação simples do AmpOp. Acima desses valores sempre ocorrerá a saturação do componente.


## 3. Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual -100V/V.

O circuito simulado foi o circuito abaixo, tanto no caso do AD 8040 como no caso do AD 8539, as únicas diferenças sendo o AmpOp em questão e a alimentação do AmpOp (±5V para o AD8040 e ±2.5V para o AD8539).

![inversor_ad](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2003/Exemplos/inversor_ad.png)

Ao aplicar 0V no circuito com o AD 8040, obtemos Vout=-169,90mV. Vale lembrar que esse valor está sendo sempre multiplicado pelo ganho, ou seja, o valor do offset é 100 vezes menor do que o valor de Vout, o que nos dá aproximadamente 1,7mV, o que condiz com o offset apresentado pelo datasheet do AmpOp em questão. Aplicando 0V no circuito com o AD 8539, obtemos Vout=1,38mV. Como o valor medido em Vout é 100 vezes o offset, temos o offset também na faixa apresentada no datasheet, de cerca de 1,3uV.

Esse resultado pode ser explicado por conta do circuito inversor utilizado, já que possui ganho de -100V/V.


Aplicando um sinal senoidal de 10mVpp@1kHz temos o seguinte resultado:

## AD 8040

![ad8040_5mv](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2003/Exemplos/ad8040_5mv.png)

No circuito em questão, é notado que o ideal, em um circuito de ganho -100V/V (calculado pela relação entre R2 e R1), ao colocar uma onda senoidal de 10mVpp, deveríamos obter no seu vale -500mV e em sua crista 500mV. Porém, obtemos o seguinte gráfico ao simular o circuito:

![grafico_ad8040_5mv](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2003/Exemplos/grafico_ad8040_5mv.png)

Nota-se que o offset do AmpOp em questão é vital nessa análise, pois com um offset de 1.60mV em um ganho de -100V/V, obtemos cerca de -160mV no gráfico de análise do circuito. Portanto, verificando os valores máximos e mínimos do gráfico por meio do relatório obtido no SPICE, encontramos o valor de Vmin = -668,26mV e Vmax = 327,68mV, o que nos dá aproximadamente o offset amplificado, condizendo com o datasheet do componente.

## AD 8539

![ad8539_5mv](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2003/Exemplos/ad8539_5mv.png)

Neste circuito, novamente teríamos um circuito ideal em -500mV de valor mínimo e 500mV de valor máximo. O gráfico analisado é o seguinte:

![grafico_ad8539_5mv](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2003/Exemplos/grafico_ad8539_5mv.png)

De acordo com o valor analisado anteriormente neste relatório, havíamos obtido um offset de 1,38mV. Obtendo o relatório do SPICE, chegamos ao valor máximo de Vmax = 493,57mV e Vmin = -492,04mV. Isso nos dá um offset maior do que o previsto em simulação. Isso pode ocorrer por conta dos baixos valores utilizados para análise.
