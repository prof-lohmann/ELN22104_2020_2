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
    Ganho em malha aberta:
    Impedância de entrada:
    
  ## 2 - Simule um circuito seguidor de tensão com cada um dos ampops indicados  e verifique osefeitos decorrentes da máxima e mínima tensão de entrada. 
  
  ### AD4080
  

Para alimentação do AmpOp, foi utilizado -5V na entrada -V e 5V na entrada +V, seguindo as especificações encontradas no datasheet, o AmpOp trabalha fora da saturação no máximo em ±5V. Acima disso, podemos observar essa tensão sendo ceifada no pico de no máximo 5V, justamente por ser a tensão limite de alimentação. No gráfico abaixo podemos perceber o funcionamento do AD8040 como um seguidor de tensão, para uma fon te de 5V com frequência de 1kHz.
![image](https://user-images.githubusercontent.com/75046369/109438396-8edb5d00-7a08-11eb-8b1d-170994987418.png)
Obtemos um valor máximo de Vmax=4.998245 e um valor mínimo de Vmin=-4.997561, onde temos um offset de 1.75mV no máximo e 2.44mV no mínimo, nos indicando que está dentro do especificado pelo datasheet, onde mostra um valor típico de 1.60mV porém máximo de 5mV.
![image](https://user-images.githubusercontent.com/75046369/109438479-f2658a80-7a08-11eb-978b-59d46daad63a.png)
No gráfico acima, foi aplicada uma tensão de 6V na fonte colocada na entrada não inversora, com a alimentação do AmpOp de modo especificado pelo datasheet.


### AD8539

![image](https://user-images.githubusercontent.com/75046369/109438416-add9ef00-7a08-11eb-9733-9b1bb897d014.png)
No AD8539 utilizamos alimentação de ±2.5V. A fonte na entrada não inversora foi de 2.5V com frequência de 1kHz. A partir de 2,5V temos saturação.
![image](https://user-images.githubusercontent.com/75046369/109438450-d3ff8f00-7a08-11eb-81a1-f05916f50266.png)

