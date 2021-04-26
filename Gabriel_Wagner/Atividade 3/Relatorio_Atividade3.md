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

<img src="ad8040inversorsenoidal.jpg" width="1000">

O valor está deslocado 200 mV do valor correto, tanto para o pico positivo quanto negativo. Esse efeito está descrito no datasheet.

Figura 6 - Inversor AD8539 com sinal senoidal de 10mVpp@1kHz e ganho -100 V/V.

<img src="ad8539inversorsenoidal.jpg" width="1000">

O valor da simulação está de acordo com o valor calculado.

## Parte 4

Figura 7 - Não Inversor AD8040 com sinal 0V e ganho 11 V/V.

<img src="ad8040ninversor.jpg" width="1000">

Figura 8 - Não Inversor AD8539 com sinal 0V e ganho 11 V/V.

<img src="ad8539ninversor.jpg" width="1000">

A tensão de offset aparece novamente em ambas as simulações. Sendo o efeito mais perceptível no AD8040.

Figura 9 - Não Inversor AD8040 com sinais de 5mV, 50mV, 200mV e 500mV e ganho 11 V/V.

<img src="ad8040tensoes.jpg" width="1000">

Tabela 1 - Erro da Tensão de saída calculada x simulação do ampop AD8040.

Vin(V) | Vout teórico(v) | Vout simulação(V) | Erro (%)
-- | ------------------ | ----------- | --------
5m | 50m | 74,4m | 48,8
50m | 500m | 568m | 13,6
200m | 2 | 2,214 | 10,7
500m | 5 | 5 | 0

Figura 10 - Não Inversor AD8539 com sinais de 5mV, 50mV, 200mV e 500mV e ganho 11 V/V.

<img src="ad8539tensoes.jpg" width="1000">

Tabela 2 - Erro da Tensão de saída calculada x simulação do ampop AD8539.

Vin(V) | Vout teórico(v) | Vout simulação(V) | Erro (%)
-- | ------------------ | ----------- | --------
5m | 50m | 55m | 10
50m | 500m | 550m | 10
200m | 2 | 2,2 | 10
500m | 5 | 2,478 | 50

Obs. O erro de 50% na última linha do AD8539 se deve a saturação do sinal, pois as tensões de alimentação desse ampop são de +-2,5 v.

Podemos perceber alguns detalhes, o erro do ampop AD8040 aumenta conforme diminuímos as tensões de entrada. Grande parte devido a tensão de offset, que têm uma grandeza de tensão na ordem de mV.

Outro detalhe é que o erro ao ampop AD8539 é mais equilibrado, apresentando valores constantes com regularidade.

## Parte 5

A escolha dos ampops se deram principalmente pois as tensões de entrada são baixas, na ordem de milivolt e microvolt, então tensões de modo comum e tensões de offset altas vão gerar erro na tensão da saída.

Figura 11 - Característica do ampop TLV2333

<img src="ampop_escolha.jpg" width="1000">

Referência Imagem: Texas Instruments; https://www.ti.com/amplifier-circuit/op-amps/products.html#p2max=0.0015;0.02&sort=p1130;desc
Produto: Texas Instruments; https://www.ti.com/product/TLV2333

Percebe-se que esse ampop apresenta tensão de offset de 15 uV e CMRR de 130 dB, com um valor de 0,607 dólares.

Verificando ampops da Analog Devices, temos o ampop utilizado neste relatório, o ampop AD8539, com tensão de offset de 15 uV e CMRR típico de 150 dB, custando 0,72 dólares.

Produto: Analog Devices; https://www.analog.com/en/products/ad8539.html







