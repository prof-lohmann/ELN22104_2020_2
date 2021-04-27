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
###### Em teoria, teremos um VCC de 24Vrms. Porem, o circuito real teria problemas como queda de tensao dos diodos, a carga dos capacitores e o fato deste circuito dobrador de tensao teria drenagem de corrente para cada semi ciclo, gerando ripple. A melhoria recomendada para este circuito seria substituir od diodos por schottky, por possuirem menor queda de tensao de suas juncoes e aumentar a frequencia de operacao da fonte para diminuir o ripple.

#### Circuito proposto (02) para a alimentação do AmpOp:

> ![figura3](https://user-images.githubusercontent.com/12564754/116309279-f569c680-a77e-11eb-9f5d-917d43a399ba.PNG)

##### Vamos projetar esse circuito de alimentação do AmpOp?
##### Considere: AmpOp LM324, MOSFET IRF540, VOUT = 15V, IOUT = 1A, vin+ = 12Vrms, vripple_pós_retificador = 1V, considere as quedas de tensão nos diodos de 0,7V.
##### Responda: 

• Qual a Tensão VGS? Descreva como obter o valor.
• Qual a corrente de alimentação do AmpOp?
• Qual a tensão de alimentação do AmpOP?
• Qual fator devo considerar para escolher o transistor Q1?
• Qual valor da tensão do diodo zener D6?
• Como escolher o diodo zener D6, maximizando a eficiência energética e
minimizando os ruídos no circuito?
• Considere que, por alterações futuras no circuito, o AmpOp poderá ter uma
aumento de 10mA na corrente de alimentação, o circuito proposto continuará
funcionando?





	


