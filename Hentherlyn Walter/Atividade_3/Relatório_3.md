# Atividade 3

## Simulação de circuitos com Amplificadores operacionais AD8040 e AD8539.
### Questão 1: Verifique no datasheet dos Ampops indicados os valores dos itens abaixo:

#### AD8040

##### ◦ Máxima e mínima tensão de alimentação:
  2,7 _ +12 V
##### ◦ Tensão de modo comum:
  -5,2 _ +5,2V
##### ◦ CMRR
  -4,5 _ +3 V
##### ◦ Máxima e mínima tensão de entrada
  Faixa de ±200 mV
##### ◦ Tensão de offset
  Máximo 6 mV
##### ◦ Corrente de polarização
  0,7 _ +1,3 uA
##### ◦ Consumo de corrente
  1,3 mA
##### ◦ Ganho em malha aberta
  -4,0 _ +4,0 V
##### ◦ Impedância de entrada
  6 MΩ e 2 pF
  
#### AD8539

##### ◦ Máxima e mínima tensão de alimentação:
  –2,7 _ +5,5 V
##### ◦ Tensão de modo comum:
  0 _ +5,0 V
##### ◦ CMRR
  0 _ +5 V
##### ◦ Máxima e mínima tensão de entrada
  0 _ +5 V
##### ◦ Tensão de offset
  Máximo 13 uV
##### ◦ Corrente de polarização
  0,7 _ 1,3 uA
##### ◦ Consumo de corrente
  15 _ 25 pV
##### ◦ Ganho em malha aberta
  0,1 _ 4,9 V
##### ◦ Impedância de entrada
  10 KΩ e 300 pF
  
## Para todas simulações abaixo utilize a alimentação simétrica recomendada no datasheet
 
### Questão 2: Simule um circuito seguidor de tensão com cada um dos ampops indicados e verifique os efeitos decorrentes da máxima e mínima tensão de entrada.
1. Dica utilize um sinal senoidal de 1kHz para auxiliar na visualização.
2. Responda quais os valores das tensões de saturação?

#### AD8040

![Figura_1](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_3/Imagens/Quest%C3%A3o%201.1.JPG)

_Figura 1_

![Figura_2](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_3/Imagens/Quest%C3%A3o%201%20-%20AD8539%20com%204V%20-%20gr%C3%A1fico.JPG)

_Figura 2_

Nesta simulação, utilizou-se uma alimentação de 5V na entrada V+ e -5V na entrada V-, conforme descrito no datasheet. Analisando o gráfico acima, podemos perceber que o AmpOp trabalha fora de saturação, já que atinge no máximo 5 V e no mínimo -5V, conforme a alimentação. Além disso, é possível perceber que o circuito se trata de um seguidor de tensão, pois faz uma cópia quase perfeita da tensão de entrada na sua saída. Analisando os valore de pico máximo e mínimo obtemos respectivamente, 4,9979V e -4,9977V. Sendo assim, obtemos uma tensão de offset de 2,1 mV no pico máximo e 2,3 mV no vale, valores que se encaixam nas especificações encontradas no datasheet.

![Figura_3](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_3/Imagens/Gr%C3%A1fico%20Quest%C3%A3o%201.1.JPG)

_Figura 3_

No gráfico acima, foi aplicada uma tensão de 6V na fonte colocada na entrada inversora, conforme pode-se observar a saturação acontece e a tensão não uktrapassa os 5V da alimentação.

#### AD8539

![Figura_3](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_3/Imagens/Quest%C3%A3o%201%20-%20AD8539%20com%204V.JPG)

_Figura 3_

![Figura_4](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_3/Imagens/Quest%C3%A3o%201%20-%20AD8539%20com%204V%20-%20gr%C3%A1fico.JPG)

_Figura 4_

Explicação:

### Questão 3: Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule os
resistores para ter um ganho igual -100V/V.
1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.

#### AD8040

![Figura_5](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_3/Imagens/Quest%C3%A3o%202%20-%20AD8040%20com%200V.JPG)

_Figura 5_

![Figura_6](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_3/Imagens/Quest%C3%A3o%202%20-%20AD8040%20com%200V%20-%20grafico.JPG)

_Figura 6_

#### AD8539

![Figura_7](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_3/Imagens/Quest%C3%A3o%202%20-%20AD8539%20com%200V.JPG)

_Figura 7_

![Figura_8](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_3/Imagens/Quest%C3%A3o%202%20-%20AD8539%20com%200V%20-%20grafico.JPG)

_Figura 8_

2. Aplique um sinal senoidal de 10mVpp@1kHz na entrada e verifique o sinal de saída.
Explique o resultado.

#### AD8040

#### AD8539



### Questão 4: Simule um circuito amplificador não inversor com cada um dos ampops indicados e calcule
os resistores para ter um ganho igual 10V/V.
1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.
2. Aplique um sinal continuo de 5mV, 50mV, 200mV e 500mV na entrada e verifique o sinal
de saída. Qual o erro com relação ao ganho calculado? Explique o resultado.

### Caso deseja-se projetar um amplificador subtrator com ganho de 100V/V, para sinais muito
pequenos com variação de +/-10uV até +/-30mV de muito baixa frequência, qual desses ampops
você utilizaria? Justifique a sua resposta.
Escolha um terceiro ampop com características melhores que os ampops acima para uma aplicação
como subtrator.
