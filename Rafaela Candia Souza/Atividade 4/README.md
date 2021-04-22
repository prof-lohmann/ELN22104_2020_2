# Atividade 4 

## Integração dos blocos de uma fonte linear

### Parte 01: Entendendo um regulador linear

#### Considerando o circuito da figura 01 que representa uma fonte linear com regulador MOSFET, temos o seguinte problema:

> ![figura1](https://user-images.githubusercontent.com/12564754/115304825-cc708280-a13b-11eb-8aaa-7998525d5d56.PNG)

##### Qual relação entre a tensão de alimentação do ampop e a tensão de saída?
###### A relação é que a tensao de saida será a alimentacao do ampop subtraida das quedas de tensao internas do proprio ampop.

##### O que devemos considerar para esse circuito operar como um LDO?
###### Para operar como um LDO, deve-se garantir que a tensao que alimenta o ampop e o MOSFET  seja maior que a esperada na saída, e considere as quedas de tensao de saida do ampop e gate do mosfet.

##### Como obter as tensões de alimentação para o AmpOp (VCC e VEE)?
###### Qualquer forma de regulacao que garanta um VCC superior ao valor necessario para polarizar o gate do mosfet e que considere a queda de tensao do ampop.

#### Circuito proposto (01) para a alimentação do AmpOp:

> ![figura2](https://user-images.githubusercontent.com/12564754/115305876-6422a080-a13d-11eb-9d1a-5cbae9928abc.PNG)

##### Utilizando o circuito dobrador de tensão, qual valor de VCC você obtêm para um sinal Vin+ de 12Vrms? Quais problemas apresentam esse circuito? Podemos melhorar?



