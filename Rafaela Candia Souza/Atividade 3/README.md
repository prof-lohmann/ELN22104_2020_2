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
> ![AD8040a](https://user-images.githubusercontent.com/12564754/114089080-1cbe2980-988c-11eb-871b-da7faa2b6068.PNG)
> 
> Este circuito se trata de um seguidor de tensão. Nessa simulação foi utilizada alimentação de ±5 V nas entradas V+ e V- e 5V na entrada nao-inversora. Analisando o gráfico
> presente na imagem, o AmpOp trabalha fora de saturação, já que atinge no máximo ±5 V. 
> ![AD8040b](https://user-images.githubusercontent.com/12564754/114089471-90f8cd00-988c-11eb-8a3e-a09d7d053fcd.PNG)
> 
> Ao colocar 5,2V na entrada nao-inversora, o AmpOp comeca a apresentar sinais de saturação.

##### AD8539
> ![AD8539a](https://user-images.githubusercontent.com/12564754/114094945-46c71a00-9893-11eb-8858-fe1b5bfdafca.PNG)
> 
> Nessa simulação foi utilizada alimentação de ±2,5 V nas entradas V+ e V- e 2V na entrada nao-inversora. Analisando o gráfico  presente na imagem, o AmpOp trabalha fora de saturação, já que atinge no máximo ±2,5 V. 
> ![AD8539b](https://user-images.githubusercontent.com/12564754/114095084-652d1580-9893-11eb-939a-7254330aa9d0.PNG)
> 
> Ao colocar 2,59V na entrada nao-inversora, o AmpOp comeca a apresentar sinais de saturação.

### 3. Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual -100V/V. 

> O ganho do amplificador inversor é calculado por: G=R1/R2, utilizaremos os valores:
> ` R1 = 1KΩ e R2 = 100KΩ. ` 

#### a) Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.

##### AD8040
> ![AD8040c](https://user-images.githubusercontent.com/12564754/114095658-10d66580-9894-11eb-8618-22fad36bcc80.PNG)
> 
> Ao aplicar 0V no circuito , obtemos Vout ≅ 70mV. Este valor está sendo multiplicado pelo ganho, o que significa que o valor do offset é 100 vezes menor do que 
> o valor de Vout, o que nos dá aproximadamente 0,7mV de offset conforme o datasheet informa. 
##### AD8539
> ![AD8539c](https://user-images.githubusercontent.com/12564754/114095979-804c5500-9894-11eb-88e2-2334ecd57630.PNG)
> 
> Ao aplicar 0V no circuito , obtemos Vout ≅ 1,40mV. Este valor está multiplicado pelo ganho, ou seja, o valor do offset é 100 vezes menor do que  o valor de Vout,
> o que nos dá aproximadamente 14µV de offset conforme o datasheet informa.

#### b) Aplique um sinal senoidal de 10mVpp 1kHz na entrada e verifique o sinal de saída. Explique o resultado.

##### AD8040
> ![AD8040d](https://user-images.githubusercontent.com/12564754/114096647-63645180-9895-11eb-9508-abb370bd9a37.PNG)
> O sinal de saída esta invertido, como esperado para um circuito inversor. Apresenta o valor de saída 100 vezes maior do que o de entrada como previsto para o ganho definido no circuito. O Offset do amplificador fica aparente ao vermos o Vmax= 560mv e Vmim= -420mV.

##### AD8539
> ![AD8539d](https://user-images.githubusercontent.com/12564754/114096669-6cedb980-9895-11eb-8965-3427563344aa.PNG)
> O sinal de saída esta invertido, como esperado para um circuito inversor. Apresenta o valor de saída 100 vezes maior do que o de entrada como previsto para o ganho definido no circuito. O Offset do amplificador fica aparente ao vermos o Vmax= 495mv e Vmim= -495mV.

### 4. Simule um circuito amplificador não inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual 10V/V.

> O ganho do amplificador nao inversor é calculado por: G=R1/R2, utilizaremos os valores:
> ` R1 = 1KΩ e R2 = 100Ω. ` 

#### a) Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.

##### AD8040
>
> 

##### AD8539
>  
>

#### b) Aplique um sinal continuo de 5mV, 50mV, 200mV e 500mV na entrada e verifique o sinal de saída. Qual o erro com relação ao ganho calculado? Explique o resultado.


##### AD8040


##### AD8539

### 5. Caso deseja-se projetar um amplificador subtrator com ganho de 100V/V, para sinais muito pequenos com variação de +/-10uV até +/-30mV de muito baixa frequência, qual desses ampops você utilizaria? Justifique a sua resposta. Escolha um terceiro ampop com características melhores que os ampops acima para uma aplicação como subtrator.
