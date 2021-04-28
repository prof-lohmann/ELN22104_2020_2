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

### AD8040

![123](https://user-images.githubusercontent.com/75050609/110173688-bb62f080-7ddd-11eb-8fa1-d2e52d5990d0.PNG)

Ao aplicarmos 0V na entrada inversora, temos uma tensão de saida de 169,90mV. Sabendo que a tensão é o Vo dividido pelo ganho, o valor do offset será 100 vezes menor que a tensão de saída.

![147](https://user-images.githubusercontent.com/75050609/110175233-362d0b00-7de0-11eb-8ef3-779450d2cc6e.PNG)

![125](https://user-images.githubusercontent.com/75050609/110177220-64601a00-7de3-11eb-9d92-4756898f5077.jpeg)

Neste circuito podemos observar que tais valores de 500mV de máximo e -500mV de mínimo não foram alcançados devido ao valor do offset do aparelho.

### AD8539

![1212](https://user-images.githubusercontent.com/75050609/110176105-93758c00-7de1-11eb-9aca-784e00a39cf3.PNG)

Ao aplicarmos 0V na entrada inversora, temos uma tensão de saída de 1,38mV. Podemos dizer que o valor do offset condiz com o datasheet.

![125](https://user-images.githubusercontent.com/75050609/110176991-f9aede80-7de2-11eb-9ffc-240be49c116c.PNG)

![125](https://user-images.githubusercontent.com/75050609/110177790-42b36280-7de4-11eb-960c-87bbbed79080.jpeg)

Neste circuito podemos observar que chegamos mais proximos do 500mV de máximo e -500mV de mínimo, pois o valor do offset do aparelho é diferente em comparação ao primeiro circuito.

## 4) Simule um circuito amplificador não inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual a 10V/V.

### AD8040

![122](https://user-images.githubusercontent.com/75050609/110217619-d42ddd80-7e93-11eb-9f1d-dc91ae474f8c.jpeg)

![123](https://user-images.githubusercontent.com/75050609/110217621-d6903780-7e93-11eb-94b4-4a1e2c92bd08.jpeg)

Aplicando 0V na entrada, atingiu-se na saída o resultado de -15,289mV. Aplicando os valores solicitados, temos:

* 5mV: 35,5mV
* 50mV: 485,3mV
* 200mV: 1,986V
* 500mV: 4,931V

Calculando o erro percentual em relação ao ganho 10V/V, temos: 

* 5mV: 28,1%
* 50mV: 2,81%
* 200mV: 0,63%
* 500mV: 0,53$

### AD8539

![155](https://user-images.githubusercontent.com/75050609/110217957-c416fd80-7e95-11eb-8397-4ecd46cbf295.jpeg)

![143](https://user-images.githubusercontent.com/75050609/110217959-c6795780-7e95-11eb-8537-4c45064f2304.jpeg)

Aplicando 0V na entrada, atingiu-se na saída o resultado de 1,2mV. Aplicando os valores solicitados, temos:

* 5mV: 50,8mV
* 50mV: 500,8mV
* 200mV: 2,00V
* 500mV: 2,480V

Calculando o erro percentual em relação ao ganho 10V/V, temos: 

* 5mV: Saturou
* 50mV: Saturou
* 200mV: Saturou
* 500mV: 99% 

### Caso deseja-se projetar um amplificador subtrator com ganho de 100V/V, para sinais muito pequenos com variação de +/-10uV até +/-30mV de muito baixa frequência, qual desses ampops você utilizaria? Justifique sua resposta. 

Eu optaria pelo AD8539, pois esse ampop apresentou melhor comportamento nessas condições com um ganho de 100V/V.

### Escolha um terceiro ampop com características melhores que os ampops acima para uma aplicação como subtrator. 

Escolheria o ampop LTC2063 pois ele possui tensões de offset máximas menores que o do ampop AD8539.





















