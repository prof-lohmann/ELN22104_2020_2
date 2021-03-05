# Atividade 03

## 1) Verifique no datasheet dos ampops indicados os valores dos itens abaixo:

### AD8040
* Máxima e mínima tensão de alimentação: de +2,7V a +12V
* Tensão de modo comum: de -0,2V a +5,2V
* CMRR Vcm: de -4,5V a +3V
* Máxima e mínima tensão de entrada: 200mV acima ou abaixo de Vc
* Tensão de offset: 6mV
* Corrente de polarização: de +0,7uA a -1,5uA
* Consumo de corrente: 1,3mA
* Ganho de malha aberta: de -4V a +4V
* Impedância de entrada: 6Mohm e 2pF

### AD8539
* Máxima e mínima tensão de alimentação: 2,7V a 5,5V
* Tensão de modo comum: de 0 a a +5V
* CMRR Vcm: de 0 a +5V
* Máxima e mínima tensão de entrada: de 0 a 4,8V
* Tensão de offset: 15uV
* Corrente de polarização: de 25pA a 60pA
* Consumo de corrente: 180uA
* Ganho em malha aberta: de +0,1V a +7V
* Impedância de entrada: 10KOhm e 300pF

## 2) Simule um circuito seguidor de tensão com cada um dos ampops indicados e verifique os efeitos decorrentes da máxima e mínima tensão de entrada.

### AD8040

![122](https://user-images.githubusercontent.com/75050609/109874501-f59d8800-7c4d-11eb-8f86-47581a63e27b.PNG)

![123](https://user-images.githubusercontent.com/75050609/109874838-6a70c200-7c4e-11eb-8729-45cd3c04f78e.PNG)

Observando o gráfico acima, vemos que o ampop está fora da saturação, pois atingiu no máximo +5V e -5V.

### AD8539

![132](https://user-images.githubusercontent.com/75050609/109876108-1d8deb00-7c50-11eb-9874-b54f73ce04ad.PNG)

De acordo com o datasheet do ampop, temos uma alimentação de +2,5V e -2,5V e como a fonte de alimentação é 3V haverá saturação, dado que a alimentação do ampop é +2,5V.

![125](https://user-images.githubusercontent.com/75050609/109879137-f3d6c300-7c53-11eb-9f5b-27ad6471393e.PNG)

Podemos observar que há uma saturação quando a tensão de saída alcança os valores de +2,5V e -2,5V.

## 3) Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual a -100V/V.

###AD8040














