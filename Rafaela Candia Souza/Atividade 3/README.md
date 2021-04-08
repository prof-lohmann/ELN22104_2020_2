# Atividade 3
## Simulação de circuitos com Amplificadores operacionais AD8040 e AD8539.
### 1. Verifique no datasheet dos Ampops indicados os valores dos itens abaixo:

>
> ![Opamppinouts](https://user-images.githubusercontent.com/12564754/102247973-6bac1180-3edf-11eb-9dbc-ea5f073403fe.png)
>
> * V+: entrada não-inversora
> * V−: entrada inversora
> * Vout: saída
> * VS+: alimentação positiva
> * VS−: alimentação negativa
>

| Ampop  |    V+ e V-   |  Vout modo comum  | CMRR  | VS+ e VS- | V Offset | I Polarizacao | I Consumo | G Malha aberta | Impedância entrada |
--- | ---  | --- | ---| --- | ---| --- | ---| --- | --- 
| AD8040 |+2,7 a +12 V| -0,2 a +5,2 V| -4,5 a +3 V| 200 mV a 5,2 V  |   6 mV max |-1,5 uA a +0,7   | 1.3 mA  |±4 V |  6 MΩ e 2 pF      |
| AD8539 |  +2,7 a +5,5 V   |   0 a +5 V    | 0 a +5 V    |    0 a +5 V    | 15 µV max  |25 pA a 60pA  | 180 µA  |    +0,1 a +7 V    |       10 KΩ e 300 pF      |
  
### 2. Simule um circuito seguidor de tensão com cada um dos ampops indicados e verifique osbefeitos decorrentes da máxima e mínima tensão de entrada.

#### Responda quais os valores das tensões de saturação?

##### AD8040
> 
> Este circuito se trata de um seguidor de tensão. Nessa simulação foi utilizada alimentação de ±5 V nas entradas V+ e V- e 5V na entrada nao-inversora. Analisando o gráfico > presente na imagem, o AmpOp trabalha fora de saturação, já que atinge no máximo ±5 V. 
> 
> Ao colocar 5,2V na entrada nao-inversora, o AmpOp comeca a apresentar sinais de saturação.

##### AD8539
> ![AD8534-a](https://user-images.githubusercontent.com/12564754/114081577-1d05f700-9883-11eb-839e-9249a3eb211e.PNG)
> Nessa simulação foi utilizada alimentação de ±2,5 V nas entradas V+ e V- e 2V na entrada nao-inversora. Analisando o gráfico  presente na imagem, o AmpOp trabalha fora de saturação, já que atinge no máximo ±2,5 V. 
> ![AD8534-b](https://user-images.githubusercontent.com/12564754/114081703-46bf1e00-9883-11eb-83f1-09c90d6ec9b7.PNG)
> Ao colocar 2,59V na entrada nao-inversora, o AmpOp comeca a apresentar sinais de saturação.

### 3. Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual -100V/V. 

#### a) Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.

##### AD8040
> ![AD8040-c](https://user-images.githubusercontent.com/12564754/114077047-c0eca400-987d-11eb-9750-62f6e5fe6eb7.PNG)
> Ao aplicar 0V no circuito , obtemos Vout ≅ -1,79mV. Este valor está sendo multiplicado pelo ganho, o que significa que o valor do offset é 100 vezes menor do que 
> o valor de Vout, o que nos dá aproximadamente 17,9mV de offset. 
##### AD8539
> ![AD8534-c](https://user-images.githubusercontent.com/12564754/114080076-52114a00-9881-11eb-80e2-8596a34f2ca2.PNG)
> Ao aplicar 0V no circuito , obtemos Vout ≅ 1,37mV. Este valor está multiplicado pelo ganho, ou seja, o valor do offset é 100 vezes menor do que  o valor de Vout,
> o que nos dá aproximadamente 13,7mV de offset.

#### b) Aplique um sinal senoidal de 10mVpp 1kHz na entrada e verifique o sinal de saída. Explique o resultado.

##### AD8040
> 
>

##### AD8539
> ![AD8534-d](https://user-images.githubusercontent.com/12564754/114082417-17f57780-9884-11eb-8571-5a29dbb42ade.PNG)
>

### 4. Simule um circuito amplificador não inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual 10V/V.

#### a) Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.

##### AD8040
> Sabendo que o ganho do amplificador não inversor é calculado por: G= 1 + Rf/R1, utilizaremos os valores:
> ´ Rf = 900 ohms e R1 = 100 ohms. ´
> 

#### b) Aplique um sinal continuo de 5mV, 50mV, 200mV e 500mV na entrada e verifique o sinal de saída. Qual o erro com relação ao ganho calculado? Explique o resultado.

### 5. Caso deseja-se projetar um amplificador subtrator com ganho de 100V/V, para sinais muito pequenos com variação de +/-10uV até +/-30mV de muito baixa frequência, qual desses ampops você utilizaria? Justifique a sua resposta. Escolha um terceiro ampop com características melhores que os ampops acima para uma aplicação como subtrator.
