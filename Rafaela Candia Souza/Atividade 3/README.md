# Atividade 3
## Simulação de circuitos com Amplificadores operacionais AD8040 e AD8539.
### 1. Verifique no datasheet dos Ampops indicados os valores dos itens abaixo:

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
> Ao aplicar 0V no circuito, obtemos Vout ≅ 70mV. Este valor está sendo multiplicado pelo ganho, o que significa que o valor do offset é 100 vezes menor do que 
> o valor de Vout, o que nos dá aproximadamente 0,7mV de offset, estando dentro do valor conforme o datasheet informa. 
##### AD8539
> ![AD8539c](https://user-images.githubusercontent.com/12564754/114095979-804c5500-9894-11eb-88e2-2334ecd57630.PNG)
> 
> Ao aplicar 0V no circuito, obtemos Vout ≅ 1,40mV. Este valor está multiplicado pelo ganho, ou seja, o valor do offset é 100 vezes menor do que  o valor de Vout,
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
> ![AD8040e](https://user-images.githubusercontent.com/12564754/114100925-66fad700-989b-11eb-90ba-026f03174496.PNG)
> 
> Ao aplicar 0V no circuito, obtemos Vout ≅ 700µV. Este valor está sendo multiplicado pelo ganho, o que significa que o valor do offset é 10 vezes menor do que 
> o valor de Vout, o que nos dá aproximadamente 70µV de offset, estando dentro do valor conforme o datasheet informa. 
##### AD8539
> ![AD8539e](https://user-images.githubusercontent.com/12564754/114101104-a295a100-989b-11eb-89e7-5959b09c0179.PNG)
> 
> Ao aplicar 0V no circuito, obtemos Vout ≅ 250µV. Este valor está multiplicado pelo ganho, ou seja, o valor do offset é 10 vezes menor do que  o valor de Vout,
> o que nos dá aproximadamente 25µV de offset, estando 12µV fora do valor conforme o datasheet informa.


#### b) Aplique um sinal continuo de 5mV, 50mV, 200mV e 500mV na entrada e verifique o sinal de saída. Qual o erro com relação ao ganho calculado? Explique o resultado.

##### AD8040

| V in  |    5mV  |  50mV | 200mV | 500mV | 
--- | ---  | --- | ---| --- 
| V out |49,7mV| 500,02mV| 2,02V| 4,84V  |  
| E% |  0,60%   |   0,04%   | 1,00%    |    3,30%   | 

##### AD8539

| V in  |    5mV  |  50mV | 200mV | 500mV | 
--- | ---  | --- | ---| --- 
| V out |50,2mV| 500,01mV| 2,01V| 4,72V  |  
| E% |  0.40%   |   0,002%    | 0,50%   |    5,93 %  | 

### 5. Caso deseja-se projetar um amplificador subtrator com ganho de 100V/V, para sinais muito pequenos com variação de +/-10uV até +/-30mV de muito baixa frequência, qual desses ampops você utilizaria? Justifique a sua resposta. Escolha um terceiro ampop com características melhores que os ampops acima para uma aplicação como subtrator.

> O AD8539 é mais adequado para esta aplicacao, devido sua tensao de offset ser menor e possuir menor erro com relação ao ganho calculado conforme na tabela anterior.
> 
> Outro Ampop que poderia ser utilizado é o TSV7721, ou qualquer outro da familia TSV772x. Isso devido aos seguintes parametro:

* Gain bandwidth product 22 MHz, unity gain stable
* High accuracy input offset voltage: 50 µV typ., 200 µV max.
* Low input bias current: 2 pA typ.
* Low input voltage noise density: 7 nV/√Hz

> Informacoes retiradas do site: https://www.st.com/en/amplifiers-and-comparators/tsv7722.html?ecmp=tt20710_gl_ps_apr2021&aw_kw=op%20amps&aw_m=p&aw_c=12734036595&aw_tg=kwd-195551462&aw_gclid=Cj0KCQjw38-DBhDpARIsADJ3kjnoNdUDcL6AZw-5mIA6CAceAqqaI4IQC4-vTQXelF0c-zaOuvBwBEQaAnl3EALw_wcB&gclid=Cj0KCQjw38-DBhDpARIsADJ3kjnoNdUDcL6AZw-5mIA6CAceAqqaI4IQC4-vTQXelF0c-zaOuvBwBEQaAnl3EALw_wcB
