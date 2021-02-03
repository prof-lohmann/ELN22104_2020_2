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

| Ampop  | V+ e V- Max  | V+ e V- Mim |  Vout modo comum  | CMRR  | VS+ e VS- Max  | VS+ e VS- Mim  | V Ofsset | I Polarizacao | I Consumo | G Malha aberta | Impedância entrada |
--- | --- | --- | --- | ---| --- | ---| --- | ---| --- | --- | ---
| AD8040 |              |             |dfsdfds            |       | are neat       |    $1          |          |               |           |                |                    |
| AD8539 |              |             |dfsdfds            |       | are neat       |    $1          |          |               |           |                |                    |

### 2. Simule um circuito seguidor de tensão com cada um dos ampops indicados e verifique osefeitos decorrentes da máxima e mínima tensão de entrada.

#### 1. Dica utilize um sinal senoidal de 1kHz para auxiliar na visualização.
#### 2. Responda quais os valores das tensões de saturação?

### 3. Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule osresistores para ter um ganho igual -100V/V. 

#### 1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.
#### 2. Aplique um sinal senoidal de 10mVpp@1kHz na entrada e verifique o sinal de saída. Explique o resultado.

### 4. Simule um circuito amplificador não inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual 10V/V.

#### 1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.
#### 2. Aplique um sinal continuo de 5mV, 50mV, 200mV e 500mV na entrada e verifique o sinal de saída. Qual o erro com relação ao ganho calculado? Explique o resultado.

### Caso deseja-se projetar um amplificador subtrator com ganho de 100V/V, para sinais muito pequenos com variação de +/-10uV até +/-30mV de muito baixa frequência, qual desses ampops você utilizaria? Justifique a sua resposta. Escolha um terceiro ampop com características melhores que os ampops acima para uma aplicação como subtrator.
