# Simulação de circuitos com Amplificadores operacionais AD8040 e AD8539.
## 1. Verifique no datasheet dos Ampops indicados os valores dos itens abaixo:
### AD8040
- Máxima e mínima tensão de alimentação: 2,7 a 12,0 V
- Tensão de modo comum: -5,2 a 5,2 V
- CMRR: Vcm = -4,5 a 3,0 V
- Máxima e mínima tensão de entrada: 200 mV acima ou abaixo
- Tensão de offset: Máximo de 6 mV
- Corrente de polarização: 0,7 a 1,3 uA
- Consumo de corrente: 1,3 mA
- Ganho em malha aberta: Vo = -4,0 a 4,0 V, 74 dB
- Resistência de entrada: 6M Ohm

### AD8539
- Máxima e mínima tensão de alimentação: 2.7V a 5.5V
- Tensão de modo comum: 2.5V
- CMRR: Vcm = 0 a 2,5 V
- Máxima e mínima tensão de entrada: 0 a 2,7 V
- Tensão de offset: Máximo de 13 uV
- Corrente de polarização: 15 a 25 pA
- Consumo de corrente: 180 uA
- Ganho em malha aberta: N/A
- Impedância de entrada: N/A

## 2. Simule um circuito seguidor de tensão com cada um dos ampops indicados e verifique os efeitos decorrentes da máxima e mínima tensão de entrada.
### 1. Dica utilize um sinal senoidal de 1kHz para auxiliar na visualização.
### 2. Responda: quais os valores das tensões de saturação?
### AD8040
Utilizando os valores extraídos do datasheet e apresentados na questão anterior, foi simulado o circuito seguidor de tensão da seguinte forma; Vin= 7v senoidal (para extrapolar o valor de saturação e o mesmo ficar bem visível no gráfico) com frequência de 1k hz, V+= 5vcc, V-= -5vcc e foi adotado um transiente de 1000u para a visualização completa de 1 ciclo. A seguir, observaremos o esquema de ligação do circuito:

![Seguidor de tensão circuito](https://github.com/mauriciots96/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Maur%C3%ADcio%20Teixeira/Atividade%203/q2%20circuito%20AD8040.jpg)

A partir deste circuito, rodamos a simulação para verificar o sinal de onda do Vout e avaliar os impactos da máxima e mínima tensão de entrada.

![Seguidor de tensão gráfico](https://github.com/mauriciots96/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Maur%C3%ADcio%20Teixeira/Atividade%203/q2%20gr%C3%A1fico%20AD8040.jpg)

Analisando o gráfico, podemos observar que o valor de saída é saturado quando chega na região de +/-5V durante aproximadamente 0.005ms e volta a entregar o sinal de onda senoidal até chegar no seu valor de pico de +/-7V.

### AD8539
Este segundo Ampop possui valores menores de máxima e mínima tensão de entrada, portanto, os valores utilizados na construção do circuito foram; Vin= 2.7v com frequência de 1000hz, +Vcc=2.5v, -Vcc= -2.5v e novamente um transiente de 1000u para poder avaliar um ciclo completo. 

![Circuito seguidor de tensão AD8539](https://github.com/mauriciots96/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Maur%C3%ADcio%20Teixeira/Atividade%203/q2%20Circuito%20AD8539.jpg)

Rodando a simulação do circuito, encontramos o seguiinte sinal de saída:

![Gráfico AD8539](https://github.com/mauriciots96/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Maur%C3%ADcio%20Teixeira/Atividade%203/q2%20Gr%C3%A1fico%20AD8539.jpg)

Assim como o Amplificador anterior, observamos uma região de saturação na faixa especificada pelo datasheet (+/-2.5v)

## 3. Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual -100V/V.
### 1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.
### 2. Aplique um sinal senoidal de 10mVpp@1kHz na entrada e verifique o sinal de saída. Explique o resultado.

Para determinar o valor das resistências, utilizamos a equação (G=-R2/R1), onde o resultado teria que ser -100, logo, qualque valores com essa grandeza de diferença nos traria o resultado esperado. Sendo assim, os valores escolhidos foram; R2=100 e R1=1 para ambos os Ampops, já que a única diferença nos circutios será na tensão máxima e mínima de entrada.
Aplicando 0V na entrada do AD8040, chegamos a um valor de -141.80µV na saída, representando um valor de tensão de offset de -1.418µV. Este valor, é o valor necessário de tensão entre os terminais de entrada para anular o de saída. O valor da tensão de offset encontrado nunca será maior do que o especificado em datasheet.

![Circuito AD8040](https://github.com/mauriciots96/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Maur%C3%ADcio%20Teixeira/Atividade%203/q3.%20AD8040%20Circuito.jpg)

Aplicando 0V na entrada do AD8539, chegamos a um valor de 1.38mV na saída, representando um valor de tensão de offset de 13.8µV. Este valor, é o valor necessário de tensão entre os terminais de entrada para anular o de saída. O valor da tensão de offset encontrado nunca será maior do que o especificado em datasheet.

![Circuito AD8539](https://github.com/mauriciots96/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Maur%C3%ADcio%20Teixeira/Atividade%203/q3%20Circuito%20AD8539.jpg)

Aplicando um sinal senoidal de 10mVpp@1kHz na entrada, obtivemos os seguintes resultados:

# AD8040

![Gráfico AD8040](https://github.com/mauriciots96/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Maur%C3%ADcio%20Teixeira/Atividade%203/q3%20AD8040%20Gr%C3%A1fico.jpg)

O offset calculado para esse circuito era de -1.418µV e devido aos valores de resistência e tensão de entrada escolhidos para a análise, não pudemos observar uma influência muito expressiva do offset no circuito

# AD8539

![Gráfico AD8539](https://github.com/mauriciots96/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Maur%C3%ADcio%20Teixeira/Atividade%203/q3%20AD8539%20Gr%C3%A1fico.jpg)

Novamente, assim como no caso anterior, não conseguimos visualizar um efeito muito expressivo no sinal de onda Vout. É interessante ressaltar que para alguns casos nos mesmos Ampops teriam um valor de offset diferente e poderiam impactar na analise do circuito.

## 4. Simule um circuito amplificador não inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual 10V/V.
### 1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.
### 2. Aplique um sinal continuo de 5mV, 50mV, 200mV e 500mV na entrada e verifique o sinal de saída. Qual o erro com relação ao ganho calculado? Explique o resultado.

Por meio da equação de ganho em Ampops não inversores (G=1+R2/R1), chegamos na relação desejada de ganho (10v/v) com os valores de R2=9000 e R1=1000. Os valores mais altos de resistência em comparação ao exercício anterior foram escolhidos para observar melhor o efeito da tensão de offset.

# AD8040

![Circuito AD8040](https://github.com/mauriciots96/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Maur%C3%ADcio%20Teixeira/Atividade%203/q4%20Circuito%20AD8040.jpg)

Aplicando 0V(zero) de tensão na entrada, foi verificado que o valor da tensão de offset do Ampop 8040 é de aproximadamente -15.29mV. Este valor, é o valor necessário de tensão entre os terminais de entrada para anular o de saída. O valor da tensão de offset encontrado nunca será maior do que o especificado em datasheet.
Para analisar a faixa de erro encontrada em vários níveis de tensão diferente, foram determinados pelo professor os seguintes valores de tensão contínua; 5mV, 50mV, 200mV e 500mV e a partir de simulações, foram encontrados os seguintes valores:

Vin= 5mV -> Vout= 34.70mV -> E%= 30,6%

Vin= 50mV -> Vout= 484.66mV -> E%= 3,07%

Vin= 200mV -> Vout= 1.98V -> E%= 1%

Vin= 500mV -> Vout= 4.97V -> E%= 0,6%

Após a análise dos dados obtidos empiricamente, é fácil observar que com tensões cada vez mais altas, o "erro" ou a distorção gerada pelo offset se torna cada vez mais insignificante em termos proposcionais.

# AD8539

![Circuito AD8539](https://github.com/mauriciots96/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Maur%C3%ADcio%20Teixeira/Atividade%203/q4%20Circuito%20AD8539.jpg)

Aplicando 0V(zero) de tensão na entrada, foi verificado que o valor da tensão de offset do Ampop 8539 é de aproximadamente 137.30µV. Este valor, é o valor necessário de tensão entre os terminais de entrada para anular o de saída. O valor da tensão de offset encontrado nunca será maior do que o especificado em datasheet.
Para analisar a faixa de erro encontrada em vários níveis de tensão diferente, foram determinados pelo professor os seguintes valores de tensão contínua; 5mV, 50mV, 200mV e 500mV e a partir de simulações, foram encontrados os seguintes valores:

Vin= 5mV -> Vout= 50.13mV -> E%= 0,26% 

Vin= 50mV -> Vout= 500.14mV -> E%= 0,028%

Vin= 200mV -> Vout= 2.00V -> E%= 0%

Vin= 500mV -> Vout= 2.47V -> E%= 50,6%

Neste caso podemos observar que o Ampop chegou no seu ponto de saturação na última simulação, uma vez que o mesmo estava sendo alimentado com 2.5V, impossibilitando que o circuito tivesse um ganho suficiente para entregar 5V na saída.
Concluímos então que para valores até 2.5V o Ampop AD8539 possui muito mais precisão comparado com o AD8040, que por sua vez possui alimentação de 5V, o que o tornaria mais útil em aplicações onde os valores de tensão ficassem entre 2.5 e 5V.

## Caso deseja-se projetar um amplificador subtrator com ganho de 100V/V, para sinais muito pequenos com variação de +/-10uV até +/-30mV de muito baixa frequência, qual desses ampops você utilizaria? Justifique a sua resposta.
Independentemente da frequência utilizada, ertamente o Amplificador escolhido seria o AD8539 devido a sua precisão ser maior nessa faixa de tensão.

## Escolha um terceiro ampop com características melhores que os ampops acima para uma aplicação como subtrator.
Para justificar a troca do Ampop AD8539, Escolhemos um Ampop trazendo valores máximos de offset muito baixos resultado em uma alta precisão.

![Ampop Escolhido](https://github.com/mauriciots96/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Maur%C3%ADcio%20Teixeira/Atividade%203/Ampop%20escolhido.jpg)
