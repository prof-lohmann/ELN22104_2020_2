# Atividade 3
Aluno: 
* Gabriel Wagner - <gabrielstd545@gmail.com>

Professores: 
* Daniel Lohmann

## Parte 1

Visualização das características dos ampops AD8040 e AD8539.

## Parte 2

Figura 1 - Buffer AD8040 com sinal 5Vpp senoidal de 1kHz.

<img src="ad8040buffersin.jpg" width="1000">

Figura 2 - Buffer AD8539 com sinal 5Vpp senoidal de 1kHz.

<img src="ad8539buffersin.jpg" width="1000">

Percebe-se que ambas as saturações apresentam os valores de alimentação, +-5V e +-2,5V respectivamente.

## Parte 3

Figura 3 - Inversor AD8040 com sinal 0V e ganho -100 V/V.

<img src="ad8040inversor.jpg" width="1000">

Mesmo fornecendo 0V na entrada inversora, temos +181,5 mV na saída. Isso ocorre devido a tensão de offset do amplificador, podemos verificar o efeito do offset em relação ao valor do datasheet da seguinte forma.

No datasheet o maior valor típico do offset do AD8040 é 1,6 mV. Como a tensão de offset está funcionando na configuração não inversora, mesmo no circuito inversor, temos:

Vout = Vin*(1 + R2/R1)
Vout = 1.6m * 101 = 161,6 mV

O valor calculado está de acordo com a simulação.

Figura 4 - Inversor AD8539 com sinal 0V e ganho -100 V/V.

<img src="ad8539inversor.jpg" width="1000">

O efeito do offset aparece novamente. Dessa vez com o valor máximo do datasheet. 

1,3u * 101 = 1,3 mV

Figura 5 - Inversor AD8040 com sinal senoidal de 10mVpp@1kHz e ganho -100 V/V.

<img src="ad8040inversorsenoidal.jpg" width="1000"

O valor está deslocado 200 mV do valor correto, tanto para o pico positivo quanto negativo. Esse efeito está descrito no datasheet.

Figura 6 - Inversor AD8539 com sinal senoidal de 10mVpp@1kHz e ganho -100 V/V.

<img src="ad8539inversorsenoidal.jpg" width="1000">

O valor da simulação está de acordo com o valor calculado.

## Parte 4

Figura 7 - Não Inversor AD8040 com sinal 0V e ganho 10 V/V.

<img src="ad8040ninversor.jpg" width="1000">

Figura 8 - Não Inversor AD8539 com sinal 0V e ganho 10 V/V.

<img src="ad8539ninversor.jpg" width="1000">

A tensão de offset aparece novamemte em ambas as simulações.

Figura 9 - Não Inversor AD8040 com sinais de 5mV, 50mV, 200mV e 500mV e ganho 10 V/V.

<img src="ad8040tensoes.jpg" width="1000">

Figura 10 - Não Inversor AD8539 com sinais de 5mV, 50mV, 200mV e 500mV e ganho 10 V/V.

<img src="ad8539tensoes.jpg" width="1000">






