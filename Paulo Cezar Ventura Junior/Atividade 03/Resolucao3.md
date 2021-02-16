# Atividade 3
Aluno:
* Paulo Cezar Ventura Junior - <paulo.cvj@aluno.ifsc.edu.br>

Professores:
* Daniel Lohmann

## O relatório consiste em um estudo com relação aos Amplificadores operacionais modelos AD8040 e AD8539.

### AD8040
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

### AD8539
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

### AD8040

![cir_1_ad8040](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2003/Exemplos/cir_1_ad8040.png)

A alimentação utilizada no AmpOp foi de -5V na entrada V- e 5V na entrada V+ (de acordo com as especificações do datasheet). Ao verificar as tensões da entrada não inversora, podemos observar que o AmpOp trabalha fora da saturação no máximo em ±5V. Acima disso, podemos observar essa tensão sendo ceifada no pico de no máximo 5V, justamente por ser a tensão limite de alimentação. No gráfico abaixo podemos perceber o funcionamento do AD8040 como um seguidor de tensão, para uma fonte de 5V com frequência de 1kHz (totalizando 10Vpp).

![ad8040_5v](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2003/Exemplos/ad8040_5v.png)

Como podemos observar, a fonte segue quase que idealmente, porém fazendo a medição exatamente na crista e no vale, obtemos um valor máximo de Vmax=4.998245 e um valor mínimo de Vmin=-4.997561, onde temos um offset de 1.75mV no máximo e 2.44mV no mínimo, nos indicando que está dentro do especificado pelo datasheet, onde mostra um valor típico de 1.60mV porém máximo de 5mV.

Abaixo temos um segundo gráfico, onde foi aplicado 6V na fonte utilizada na entrada não inversora, porém continuamos com a alimentação do AmpOp de modo especificado pelo datasheet.

![ad8040_6v](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2003/Exemplos/ad8040_6v.png)

Como podemos perceber, a saturação já é bem evidente.


### AD8539

![cir_1_ad8539](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2003/Exemplos/cir_1_ad8539.png)

No AD 8539 utilizamos alimentação de ±2.5V. A fonte na entrada não inversora foi de 2.5V com frequência de 1kHz. Dessa forma, temos uma saturação somente a partir de 2.5V, e não antes disso. Abaixo temos um gráfico mostrando a tensão em Vout quando temos 2.6V no AD8539 (quando já está saturado).

![ad8539_satura](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2003/Exemplos/ad8539_satura.png)

Portanto, dessa forma, notamos que o limite de funcionamento apresentado nos dois Amplificadores operacionais é sempre igual a soma das tensões de alimentação, caso seja duplamente alimentado, ou igual a alimentação simples do AmpOp. Acima desses valores sempre ocorrerá a saturação do componente.


## 3. Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual -100V/V.

O circuito simulado foi o circuito abaixo, tanto no caso do AD 8040 como no caso do AD 8539, as únicas diferenças sendo o AmpOp em questão e a alimentação do AmpOp (±5V para o AD8040 e ±2.5V para o AD8539).

![inversor_ad](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2003/Exemplos/inversor_ad.png)

Ao aplicar 0V no circuito com o AD 8040, obtemos Vout=-169,90mV. Vale lembrar que esse valor está sendo sempre multiplicado pelo ganho, ou seja, o valor do offset é 100 vezes menor do que o valor de Vout, o que nos dá aproximadamente 1,7mV, o que condiz com o offset apresentado pelo datasheet do AmpOp em questão. Aplicando 0V no circuito com o AD 8539, obtemos Vout=1,38mV. Como o valor medido em Vout é 100 vezes o offset, temos o offset também na faixa apresentada no datasheet, de cerca de 13uV.

Esse resultado pode ser explicado por conta do circuito inversor utilizado, já que possui ganho de -100V/V.


Aplicando um sinal senoidal de 10mVpp@1kHz temos o seguinte resultado:

### AD 8040

![ad8040_5mv](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2003/Exemplos/ad8040_5mv.png)

No circuito em questão, é notado que o ideal, em um circuito de ganho -100V/V (calculado pela relação entre R2 e R1), ao colocar uma onda senoidal de 10mVpp, deveríamos obter no seu vale -500mV e em sua crista 500mV. Porém, obtemos o seguinte gráfico ao simular o circuito:

![grafico_ad8040_5mv](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2003/Exemplos/grafico_ad8040_5mv.png)

Nota-se que o offset do AmpOp em questão é vital nessa análise, pois com um offset de 1.60mV em um ganho de -100V/V, obtemos cerca de -160mV no gráfico de análise do circuito. Portanto, verificando os valores máximos e mínimos do gráfico por meio do relatório obtido no SPICE, encontramos o valor de Vmin = -668,26mV e Vmax = 327,68mV, o que nos dá aproximadamente o offset amplificado, condizendo com o datasheet do componente.

### AD 8539

![ad8539_5mv](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2003/Exemplos/ad8539_5mv.png)

Neste circuito, novamente teríamos um circuito ideal em -500mV de valor mínimo e 500mV de valor máximo. O gráfico analisado é o seguinte:

![grafico_ad8539_5mv](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2003/Exemplos/grafico_ad8539_5mv.png)

De acordo com o valor analisado anteriormente neste relatório, havíamos obtido um offset de 1,38mV. Obtendo o relatório do SPICE, chegamos ao valor máximo de Vmax = 493,57mV e Vmin = -492,04mV. Isso nos dá um offset maior do que o previsto em simulação. Isso pode ocorrer por conta dos baixos valores utilizados para análise.


## 4. Simule um circuito amplificador não inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual 10V/V.

### AD 8040

![ad8040_naoinversor](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2003/Exemplos/ad8040_naoinversor.png)

No circuito com o AmpOp AD 8040 utilizamos um resistor de 9k Ohm na realimentação e um de 1k Ohm na entrada inversora indo ao terra. Isso nos fornece um ganho em malha fechada de 10V/V, tendo em vista que a fórmula para o ganho é G = 1 + R2/R1. Aplicando 0V na entrada, temos o valor de aproximadamente -15,3mV na saída Vout. Isso ocorre por conta do offset do ampop, podendo ele ser positivo ou negativo. Nesse caso, o offset foi negativo, e está dentro do especificado pelo datasheet.

Aplicando sinais contínuos especificados no documento da atividade, obtemos os seguintes valores:

```
5mV -> Vout = 34,7mV
50mV -> Vout = 484,6mV
200mV -> Vout = 1,98V
500mV -> Vout = 4,97V
```

Os valores esperados eram sempre 10 vezes maiores do que os valores de entrada, porém por conta do offset não foi possível obter os valores exatos. Os erros em relação ao ganho é:

```
5mv -> 30,6%
50mV -> 3,08%
200mV -> 1%
500mV -> 0,6%
```

Podemos observar que em valores mais baixos de tensão, temos um erro percentual muito maior ao comparar com valores de tensão mais elevados. Isso se dá pelo offset do AmpOp ser na faixa de mV, causando maior disparidade com valores muito baixos.


### AD 8539

![ad8539_naoinversor](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2003/Exemplos/ad8539_naoinversor.png)

Utilizamos o mesmo circuito do AD 8040 no AD 8539, sendo as únicas diferenças o valor da alimentação do Ampop. Aplicando 0V na entrada, obtemos o valor de 137uV na saída Vout. Isso está dentro do especificado pelo datasheet, pois com um offset médio de 13uV com ganho 10V/V, o valor fica dentro do normal.

Aplicando os sinais contínuos, obtemos:

```
5mV -> Vout = 50,14mV
50mV -> Vout = 500,14mV
200mV -> Vout = 2,0001V
500mV -> Vout = 2,47V (Saturou)
```

Os valores medidos chegaram dessa vez muito mais próximos aos valores esperados, porém na última medição obtemos a saturação do AmpOp justamente por ele trabalhar em uma faixa menor do que a esperada pelo ganho, ou seja, o AmpOp funcionando com alimentação de ± 2,5V não irá chegar em um valor Vout de 5V nunca.

O erro em relação ao ganho é:

```
5mv -> 0,28%
50mV -> 0,028%
200mV -> 0,005%
500mV -> Saturou
```

Ao contrário do AD 8040, o AD 8539 apresenta um uso muito mais otimizado em baixas tensões, porém quando se trata de um valor mais elevado, ele acaba por saturar, justamente por sua especificação de alimentação do AmpOp.


## Caso deseja-se projetar um amplificador subtrator com ganho de 100V/V, para sinais muito pequenos com variação de +/-10uV até +/-30mV de muito baixa frequência, qual desses ampops você utilizaria? Justifique a sua resposta.

Seria utilizado o AD 8539, por apresentar um offset muito menor do que o AD 8040, isso se falando em baixas tensões e frequências. Comparando os dois offsets, temos 13uV no AD 8539 e 1,6mV no AD 8040, o que é um offset mais de 100 vezes maior de um para o outro. Por essas razões, é mais adequado utilizar o AD 8539 nessa aplicação.

## Escolha um terceiro ampop com características melhores que os ampops acima para uma aplicação como subtrator.

Um terceiro Ampop a ser utilizado pode ser o modelo LTC 2064, pois ele sendo utilizado nessa faixa de tensão, com um ganho de 100V/V, não irá saturar em momento algum e terá um offset muito menor do que o AD 8539, tendo seu offset típico em 1uV e chegando ao máximo em 5uV.

Na imagem abaixo, retirada diretamente do seu datasheet (disponível no site analog.com) podemos verificar o seu offset, marcado em vermelho.

![datasheet_ltc2064](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2003/Exemplos/datasheet_ltc2064.png)
