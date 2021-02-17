# Atividade 3

## Simulação de circuitos com Amplificadores operacionais AD8040 e AD8539.
### Questão 1: Verifique no datasheet dos Ampops indicados os valores dos itens abaixo:

#### AD8040

##### ◦ Máxima e mínima tensão de alimentação:
  – 2,7 _ 12 V
##### ◦ Tensão de modo comum:
  -5,2 _ +5,2V
##### ◦ CMRR
  - 4,5 _ 3 V
##### ◦ Máxima e mínima tensão de entrada
  Faixa de ±200 mV
##### ◦ Tensão de offset
  Máximo 6 mV
##### ◦ Corrente de polarização
  0,7 _ 1,3 uA
##### ◦ Consumo de corrente
  1,3 mA
##### ◦ Ganho em malha aberta
  -4,0 _ +4,0 V
##### ◦ Impedância de entrada
  6 MΩ e 2 pF
  
#### AD8539

##### ◦ Máxima e mínima tensão de alimentação:
  – 2,7 _ +5,5 V
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
 
### Questão 2: Simule um circuito seguidor de tensão com cada um dos ampops indicados e verifique os
efeitos decorrentes da máxima e mínima tensão de entrada.
1. Dica utilize um sinal senoidal de 1kHz para auxiliar na visualização.

2. Responda quais os valores das tensões de saturação?

### Questão 3: Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule os
resistores para ter um ganho igual -100V/V.
1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.
2. Aplique um sinal senoidal de 10mVpp@1kHz na entrada e verifique o sinal de saída.
Explique o resultado.

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
