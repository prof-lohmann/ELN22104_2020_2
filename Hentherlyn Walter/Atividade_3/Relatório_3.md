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

Nesta simulação, utilizou-se uma alimentação de 5V na entrada V+ e -5V na entrada V-, conforme descrito no datasheet, com uma frequência de 1 kHz. Analisando o gráfico acima, podemos perceber que o AmpOp trabalha fora de saturação, já que atinge no máximo 5 V e no mínimo -5V, conforme a alimentação. Além disso, é possível perceber que o circuito se trata de um seguidor de tensão, pois faz uma cópia quase perfeita da tensão de entrada na sua saída. Analisando os valores de pico máximo e mínimo obtemos respectivamente, 4,9979V e -4,9977V. Sendo assim, obtemos uma tensão de offset de 2,1 mV no pico máximo e 2,3 mV no vale, valores que se encaixam nas especificações encontradas no datasheet.

![Figura_3](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_3/Imagens/Gr%C3%A1fico%20Quest%C3%A3o%201.1.JPG)

_Figura 3_

No gráfico acima, foi aplicada uma tensão de 6V na fonte colocada na entrada não inversora, conforme pode-se observar a saturação acontece e a tensão não ultrapassa os 5V da alimentação simétrica.

#### AD8539

![Figura_4](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_3/Imagens/Quest%C3%A3o%201%20-%20AD8539%20com%204V.JPG)

_Figura 4_

![Figura_5](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_3/Imagens/Quest%C3%A3o%201%20-%20AD8539%20com%204V%20-%20gr%C3%A1fico.JPG)

_Figura 5_

Da mesma forma que a simulação anterior, utilizou-se uma alimentação de ± 5V, com uma frequência de 1 kHz. Aplicando uma tensão de 5V na entrada inversora observa-se que o AmpOp não satura e trabalha com 4,9978 V na crista e 4,9975 V no vale, o que nos resulta em uma tensão de offset de 2,2 mV e 2,5 mV, respectivamente, valores que também obedecem as especificações do datasheet.

![Figura_6](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_3/Imagens/Quest%C3%A3o%201%20-%20AD8539%20com%205.5V.JPG)

_Figura 6_

No gráfico acima apresentado, foi aplicada uma tensão de 5,5V na fonte colocada na entrada não inversora, conforme pode-se observar a saturação acontece e a tensão não ultrapassa os 5V da alimentação simétrica.

### Questão 3: Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual -100V/V.
1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.

#### AD8040

Simulando o circuito mostrado na figura abaixo com o AmpOp AD8040 e aplicando à sua entrada inversora 0V obtemos uma tensão de saída (Vo) de 16,96 mV. Sabendo que o valor da tensão de offset é igual a Vo dividido pelo ganho, temos que Voff é igual a 0,1696 mV  que se encaixa nas especificações presentes no datasheet.

![Figura_5](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_3/Imagens/Quest%C3%A3o%202%20-%20AD8040%20com%200V.JPG)

_Figura 5_

![Figura_6](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_3/Imagens/Quest%C3%A3o%202%20-%20AD8040%20com%200V%20-%20grafico.JPG)

_Figura 6_

#### AD8539

Da mesma forma que o item anterior, simulou-se o circuito mostrado na figura abaixo, porém com o AmpOp AD8539. Aplicando à sua entrada inversora 0V obtemos uma tensão de saída (Vo) de 2,286 mV. Sabendo que o valor da tensão de offset é igual a Vo dividido pelo ganho, temos que Voff é igual a 0,02286 mV ou 22,86 uV, valor que não se encaixa nas especificações presentes no datasheet.

![Figura_7](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_3/Imagens/Quest%C3%A3o%202%20-%20AD8539%20com%200V.JPG)

_Figura 7_

![Figura_8](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_3/Imagens/Quest%C3%A3o%202%20-%20AD8539%20com%200V%20-%20grafico.JPG)

_Figura 8_

2. Aplique um sinal senoidal de 10mVpp@1kHz na entrada e verifique o sinal de saída. Explique o resultado.

#### AD8040

Aplicou-se um sinal senoidal de 5 mV de amplitude com frequência de 1 kHz com o AmpOp AD8040 conforme o circuito abaixo.

![Figura_9](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_3/Imagens/Questao%203%20-%20AD8040%20-%20circuito.JPG)

_Figura 9_

![Figura_10](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_3/Imagens/Questao%203%20-%20AD8040%20-%20grafico.JPG)

_Figura 10_

Idealmente era esperado que os valores para a tensão de saída fossem 500 mV e -500 mV conforme foi imposto à entrada inversora, porém ao simular obtivemos os resultados apresentados no gráfico acima, 481,27 mV no pico e -515,38 mV no vale. Para o entendimento desta diferença é necessário lembrar da existência do offset. No caso do AmpOp AD8040 a tensão de offset foi 0,1696 mV, associando este valor ao ganho de -100V/V, ou seja, multiplcando Voff pelo ganho, temos cerca de -6,96 mV que é praticamente a diferença existente entre os valores ideais e simulados.

#### AD8539
Aplicando o mesmo circuito, porém agora com o AmpOp AD8539, obteve-se os seguintes resultados:

![Figura_11](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_3/Imagens/Questao%203%20-%20AD8539%20-%20circuito.JPG)

_Figura 11_

![Figura_12](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_3/Imagens/Questao%203%20-%20AD8539%20-%20grafico.JPG)

_Figura 12_

Conforme o gráfico acima, a tensão de crista foi 497,07 mV e a de vale foi -492,61 mV. No caso do AmpOp AD8539 a tensão de offset foi 0,02286 mV, associando ao ganho de -100V/V temos cerca de -2,286 mV que fazem com que a diferença entre o ideal e o simulado quase desapareçam.

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
