# Atividade 3

## 1 - Verifique no datasheet dos Ampops indicados os valores dos itens abaixo:

### AD8040

    Máxima e mínima tensão de alimentação: 2.7V a 12.0V
    Tensão de modo comum: -5.2V a +5.2V
    CMRR: Min= 80dB e Typ=90dB
    Máxima e mínima tensão de entrada: +/-200mV em relação ao Vcm
    Tensão de offset: 6mV
    Corrente de polarização: 0.7µA a 1.3µA
    Consumo de corrente: 1.3A
    Ganho em malha aberta: +-4.0V
    Impedância de entrada: 6MΩ

### AD8539

    Máxima e mínima tensão de alimentação: 2.7V a 5.5V
    Tensão de modo comum: 2.5V
    CMRR: Min= 115dB e Typ= 135dB
    Máxima e mínima tensão de entrada: 0V a 4.8V
    Tensão de offset: 15µV
    Corrente de polarização: 25pA
    Consumo de corrente: 180pA
    Ganho em malha aberta: 0,1 a 7 V
    Impedância de entrada: 10 kΩ e 300 pF
    
  ## 2 - Simule um circuito seguidor de tensão com cada um dos ampops indicados  e verifique osefeitos decorrentes da máxima e mínima tensão de entrada. 
  
  ### AD4080
  
![trabalho img 1](https://user-images.githubusercontent.com/75046369/109560130-40869680-7aba-11eb-89e6-9b133c88823d.jpg)

Para alimentação do AmpOp, foi utilizado -5V na entrada -V e 5V na entrada +V, seguindo as especificações encontradas no datasheet, o AmpOp trabalha fora da saturação no máximo em ±5V. Acima disso, podemos observar essa tensão sendo ceifada no pico de no máximo 5V, justamente por ser a tensão limite de alimentação. No gráfico abaixo podemos perceber o funcionamento do AD8040 como um seguidor de tensão, para uma fon te de 5V com frequência de 1kHz.
![image](https://user-images.githubusercontent.com/75046369/109438396-8edb5d00-7a08-11eb-8b1d-170994987418.png)
Obtemos um valor máximo de Vmax=4.998245 e um valor mínimo de Vmin=-4.997561, onde temos um offset de 1.75mV no máximo e 2.44mV no mínimo, nos indicando que está dentro do especificado pelo datasheet, onde mostra um valor típico de 1.60mV porém máximo de 5mV.
![image](https://user-images.githubusercontent.com/75046369/109438479-f2658a80-7a08-11eb-978b-59d46daad63a.png)
No gráfico acima, foi aplicada uma tensão de 6V na fonte colocada na entrada não inversora, com a alimentação do AmpOp de modo especificado pelo datasheet.


### AD8539

![image](https://user-images.githubusercontent.com/75046369/109438416-add9ef00-7a08-11eb-9733-9b1bb897d014.png)
No AD8539 utilizamos alimentação de ±2.5V. A fonte na entrada não inversora foi de 2.5V com frequência de 1kHz. A partir de 2,5V temos saturação.
![image](https://user-images.githubusercontent.com/75046369/109438450-d3ff8f00-7a08-11eb-81a1-f05916f50266.png)

## 3 - Simule um circuito amplificador inversor com cada um dos ampops  indicados e calcule osresistores para ter um ganho igual -100V/V
### 1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.
### 2. Aplique um sinal senoidal de 10mVpp@1kHz na entrada e verifique o sinal de saída.Explique o resultado.

### AD4080

![trabalho img 1](https://user-images.githubusercontent.com/75046369/109561118-8001b280-7abb-11eb-8d0c-579dcc070651.jpg)

O circuito simulado acima, nos dá um Vout = 16,96mV quando aplicado uma tensão de 0V a sua entrada inversora. Sabemos que o tensão offset é 0,1696mV já que a tensão offset é Vout dividido pelo ganho.
![trabalho img 1](https://user-images.githubusercontent.com/75046369/109600250-8b74ce00-7afb-11eb-8dde-1e1028bea201.jpg)



### AD8539

![image](https://user-images.githubusercontent.com/75046369/109588037-dafccf00-7ae6-11eb-8760-6494ff3e56d6.png)
![grafico_ad8539_5mv](https://user-images.githubusercontent.com/75046369/109589663-6d9e6d80-7ae9-11eb-8fb3-178097008323.png)
No circuito simulado acima temos na sua crista 500mv e em seu vale -500mV.

## 4 - Simule um circuito amplificador não inversor com cada um dos ampops  indicados e calculeos resistores para ter um ganho igual 10V/V
### 1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.
### 2. Aplique um sinal continuo de 5mV, 50mV, 200mV e 500mV na entrada e verifique o sinalde saída. Qual o erro com relação ao ganho calculado? Explique o resultado.

### AD8040

![trabalho img 1](https://user-images.githubusercontent.com/75046369/109598876-f7a20280-7af8-11eb-8195-b40dda0f2a6c.jpg)
Ao aplicar 0V na entrada foi obtido cerca de -1,5mV na saída.

Aplicando agora:

    5 mV: 48,29 mV
    50 mV: 497,49 mV
    200 mV: 1,986 V
    500 mV: 4,89 V
    
Ao calcular o erro percentual em relação ao ganho de 10V/V, obtemos:

      5 mV:  3,3 %
     50 mV: 0,48 %
    200 mV: 0,21 %
    500 mV: 0,49 %
    
### AD8539

![image](https://user-images.githubusercontent.com/75046369/109599438-f1f8ec80-7af9-11eb-967e-ccdb050d5524.png)
Ao aplicar 0V na entrada foi obtido cerca de 137uV na sáida.


Aplicando agora:

      5mV -> Vout = 50,1 mV
     50mV -> Vout = 500,10 mV
    200mV -> Vout = 2,00 V
    500mV -> Vout = 2,469 V - *saturação*
    
Ao calcular o erro percentual em relação ao ganho de 10V/V, obtemos:

      5mv -> 0,27%
     50mV -> 0,0279%
    200mV -> 0,0049%
    500mV -> *saturação*
    

### Caso   deseja-se   projetar   um   amplificador   subtrator   com   ganho   de   100V/V,   para   sinais   muitopequenos com variação de +/-10uV até +/-30mV de muito baixa frequência, qual desses ampopsvocê utilizaria? Justifique a sua resposta.


### Escolha um terceiro ampop com características melhores que os ampops acima para uma aplicaçãocomo subtrator.






