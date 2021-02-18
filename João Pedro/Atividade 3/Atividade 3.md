# Atividade 3

## Questão 1

### AD8040

Máxima e Mínima Tensão de alimentação: de +2,7 a +12 V\
Tensão de modo comum: de -0,2 a +5,2 V\
CMRR Vcm: de -4,5 a +3 V\
Máxima e Mínima tensão de entrada: 200 mV acima ou abaixo de Vc\
Tensão de Offset: 6 mV\
Corrente de Polarização: de +0,7 a -1,5 uA\
Consumo de Corrente: 1,3 mA\
Ganho de malha aberta: de -4 a +4 V\
Impedância de entrada: 6 MOhm e 2 pF 

### AD8539

Máxima e Mínima Tensão de alimentação: de +2,7 a +5,5 V\
Tensão de modo comum: de 0 a +5 V\
CMRR Vcm: de 0 a +5 V\
Máxima e Mínima tensão de entrada: de 0 a +5 V\
Tensão de Offset: 15 uV\
Corrente de Polarização: de 25 a 60 pA\
Consumo de Corrente: 180 uA\
Ganho de malha aberta: de +0,1 a +7 V\
Impedância de entrada: 10 KOhm e 300 pF

## Questão 2
![Circuito 1](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%203/Figuras/Q2.PNG)
![](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%203/Figuras/G1.1-8040.PNG)\
Essa simulação utiliza-se uma alimentação de 5V e -5V nas entradas _V+_ e _V-_, de acordo com o datasheet. Analisando o gráfico acima, podemos perceber que o AmpOp trabalha fora de saturação, já que atinge no máximo +-5 V, conforme a alimentação. Além disso, é possível perceber que o circuito se trata de um seguidor de tensão, pois a tensão de entrada aparace relativamente igual a saída. Analisando os valores de pico máximo e mínimo obtemos respectivamente, 1,99V e -1,99V. Pode ser percebido que o Ampop trabalha dentro das especificações do datasheet encontradas.
![Circuito 1G](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%203/Figuras/G2.PNG)\
Ao trocarmos o valor da fonte de entrada para 6 V, observa-se o momento de saturação em 5 V e -5 V.

![Circuito 2](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%203/Figuras/Q2-85.PNG)\
Essa simulação utiliza-se uma alimentação de 2,5V e -2,5V nas entradas _V+_ e _V-_, de acordo com o datasheet. A fonte de alimentação esta com 3 V, sendo assim, já haverá a saturação, pois a alimentação do Ampop é de +-2,5 V. Pode ser percebido que também o Ampop trabalha dentro das especificações do datasheet encontradas.
![Circuito 2G](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%203/Figuras/G2-85.PNG)\
Os Valores apresentados de saturação são -2,5 V e 2,5 V.

## Questão 3
### Parte 1

### AD8040

![Circuito 3](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%203/Figuras/Q3.1-80.PNG)
![Circuito 3G](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%203/Figuras/G3.1-80.PNG)\
Na simulação, ao aplicarmos na entrada inversora 0V obtemos uma tensão de saída _Vo_ de 169,96 mV. Sabendo que o valor da tensão de offset é igual a _Vo_ dividido pelo ganho, temos que _Voff_ é igual a 1,6996 mV que se encaixa nas especificações presentes no datasheet.

### AD8539

![Circuito 4](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%203/Figuras/Q3.1-85.PNG)
![Circuito 4G](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%203/Figuras/G3.1-85.PNG)\
Na simulação, ao aplicarmos na entrada inversora 0V obtemos uma tensão de saída _Vo_ de 1,386 mV. Sabendo que o valor da tensão de offset é igual a _Vo_ dividido pelo ganho, temos que _Voff_ é igual a 13,86 uV que se encaixa nas especificações presentes no datasheet.

### Parte 2

### AD8040

![Circuito 5](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%203/Figuras/Q3.2-80.PNG)
![Circuito 5G](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%203/Figuras/G3.2-80.PNG)\
Idealmente era esperado que os valores para a tensão de saída fossem 500 mV e -500 mV conforme foi imposto à entrada inversora, porém ao simular obtivemos os resultados apresentados no gráfico acima, 329,5 mV no pico e -669,0 mV no vale. Para o entendimento desta diferença é necessário lembrar da existência da tensão de offset. No caso do AmpOp AD8040 a tensão de offset foi 1,6996 mV, associando este valor ao ganho de -100V/V, ou seja, multiplcando Voff pelo ganho, temos cerca de -169,96 mV que é praticamente a diferença existente entre os valores ideais e simulados.

### AD8539

![Circuito 6](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%203/Figuras/Q3.2-85.PNG)
![Circuito 6G](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%203/Figuras/G3.2-85.PNG)\
O mesmo era para ser nesse circuito, porém ao simular obtivemos os resultados apresentados no gráfico acima, 498,54 mV no pico e -498,20 mV no vale. O mesmo entendimento se aplica para essa tensão de offset. No caso do AmpOp AD8539 a tensão de offset foi 13,86 uV associando este valor ao ganho de -100V/V, ou seja, multiplcando Voff pelo ganho, temos cerca de -1,386 mV que é praticamente a diferença existente entre os valores ideais e simulados.

## Questão 4

De acordo com a equação do circuito, podemos observar que o ganho do amplificador não inversor é gual a G = 1 + R2/R1, será utilizado R2 = 100k ohms e R1 = 10k ohms.

### Parte 1

### AD8040

![Circuito 7](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%203/Figuras/Q4.1-8040.PNG)
![Circuito 7G](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%203/Figuras/G4.1-8040.PNG)

### AD8539

![Circuito 8](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%203/Figuras/Q4.1-85.PNG)
![Circuito 8G](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%203/Figuras/G4.1-85.PNG)

### Parte 2

### AD8040

![Circuito 9](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%203/Figuras/Q4.2-80.PNG)

### AD8539

![Circuito 10](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%203/Figuras/Q4.2-85.PNG)
