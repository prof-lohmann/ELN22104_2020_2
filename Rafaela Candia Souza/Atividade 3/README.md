# Atividade 3
## Simulação de circuitos com Amplificadores operacionais AD8040 e AD8539.
### 1. Verifique no datasheet dos Ampops indicados os valores dos itens abaixo:

>
>![Opamppinouts](https://user-images.githubusercontent.com/12564754/102247973-6bac1180-3edf-11eb-9dbc-ea5f073403fe.png)
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
> ![AD8040-a](https://user-images.githubusercontent.com/12564754/113760899-337a4a00-96ed-11eb-8d7c-5c834b3d527e.PNG)
> Este circuito se trata de um seguidor de tensão. Nessa simulação foi utilizada alimentação de 5V e -5V nas entradas V+ e V- e 5V na entrada nao-inversora. Analisando o gráfico > presente na imagem, o AmpOp trabalha fora de saturação, já que atinge no máximo ±5 V. 
> ![AD8040-b](https://user-images.githubusercontent.com/12564754/113762037-886a9000-96ee-11eb-80c2-3f106d2c4073.PNG)
> Ao colocar 5,2V na entrada nao-inversora, o AmpOp comeca a apresentar sinais de saturação.

##### AD8539

### 3. Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual -100V/V. 

#### 1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.
#### 2. Aplique um sinal senoidal de 10mVpp@1kHz na entrada e verifique o sinal de saída. Explique o resultado.

### 4. Simule um circuito amplificador não inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual 10V/V.

#### 1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.
#### 2. Aplique um sinal continuo de 5mV, 50mV, 200mV e 500mV na entrada e verifique o sinal de saída. Qual o erro com relação ao ganho calculado? Explique o resultado.

### Caso deseja-se projetar um amplificador subtrator com ganho de 100V/V, para sinais muito pequenos com variação de +/-10uV até +/-30mV de muito baixa frequência, qual desses ampops você utilizaria? Justifique a sua resposta. Escolha um terceiro ampop com características melhores que os ampops acima para uma aplicação como subtrator.
