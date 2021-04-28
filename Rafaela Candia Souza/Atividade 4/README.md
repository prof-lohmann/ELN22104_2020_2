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

> - Qual a Tensão VGS? Descreva como obter o valor.
> ##### O valor de VGS é obtido subtraindo o valor de saida (Vout) do valor de tensao da saida do ampop (LM324). Analisando o datasheet do MOSFET IRF540, temos que o Gate-Source Threshold Voltage esperado para a opecao do mesmo sera um valor entre 2 a 4V.
> - Qual a corrente de alimentação do AmpOp?
> ##### Segundo o datasheet do Ampop LM324, a corrente de alimentacao pode variar de 12 a 50mA. 
> - Qual a tensão de alimentação do AmpOP?
> ##### Segundo o datasheet do Ampop LM324, a tensao de alimentacao varia entre -0,3 a 32V.
> - Qual fator devo considerar para escolher o transistor Q1?
> ##### O transistor deve operar dentro da faixa de tensao e corrente tolerados pelo LM324. 
> - Qual valor da tensão do diodo zener D6?
> ##### O diodo zener terá uma tensao de referencia para que a saida do transistor tenha o valor de alimentacao do ampop. A queda de base emissor do transistor é 0.7V, a queda de tensao do mosfet (4V) e a queda de tensao do proprio ampop (1V). Logo o zener deve ser de ser no minimo 20,7V para a fonte de 15V.
> - Como escolher o diodo zener D6, maximizando a eficiência energética e minimizando os ruídos no circuito?
> ##### Ajustar o resistor de polarizacao do zener para entregar somente o necessario para a polarizacao do mesmo.
> - Considere que, por alterações futuras no circuito, o AmpOp poderá ter uma aumento de 10mA na corrente de alimentação, o circuito proposto continuará funcionando?
> ##### Se o transistor escolhido para o circuito for por exemplo o BC541, o  circuito continuará funcionando.
### Circuito simulado para estudos:
> ![figura7](https://user-images.githubusercontent.com/12564754/116324739-0c1c1780-a797-11eb-8da8-ae303bf4ff67.PNG)

### Parte 02: Calculando e dimensionando os componentes

##### a) Para o primeiro bloco (D1, D2 e C1) considere vin+ = 12Vrms, vripple_pós_retificador = 1V e I_carga = 1,1A. Justifique a escolha dos componentes.
> ##### Para dimencionar o Capacitor C1, devemos levar em conta o calculo do ripple para que sejá o valor estipulado de 1V, logo temos que:
> ![ripple](https://user-images.githubusercontent.com/12564754/116431002-b9397300-a81d-11eb-8437-570f539e2952.png)
> ##### Como se trata de uma forma de onda retificada de forma completa, temos que nossa frequencia será duplicada.
> ##### Logo temos que: 1.1/120*1=C2f, nosso capacitor sera de 9.166uF.
> ##### Para os diodos D1 e D2, deve-se levar em consideracao a corrente especificada, logo escolhi o diodo 1N4007 que suporta este valor. 

##### b) Circuito referência de tensão zener (R1 e D3):

> - Quais fatores devo considerar para escolher o diodo zener para essa aplicação?
> ##### A tensao que chegara ao circuito de referencia será entre 15,2 a 16,2V devido as quedas dos diodos e variacao do ripple. Como a saída desejada é 12V, utilizarei uma referencia de 6,2V, utilizando o zener1N4735. O resistor R1 deverá limitar uma corente de 41mA determinada pelo datasheet do zener. Logo, temos que no pior caso: 16,2/41m = 395,12 calculado, o resistor mais proximo comercialmente é 430 ohms. 
> - Qual a influência da regulação de linha e da regulação de carga para este circuito?
> ##### Manter uma tensao constante para a carga, evitar variacoes na carga e ruidos para a carga.
> - Qual o impacto da regulação linha / carga do circuito com o diodo zener na tensão de saída do regulador linear?
> ##### Manter uma referencia fixa para o ampop e por consequencia, manter o circuito estavel.

##### Podemos melhorar esse circuito? Quais problemas podemos identificar nesta topologia?
###### Sim. Por um capacitor em paralelo com o zener, para evitar a oscilacao de tensao.

##### Sugestão de melhoria:

> ![figura4](https://user-images.githubusercontent.com/12564754/116310372-4c23d000-a780-11eb-9dde-d6c5db03fbcb.PNG)

##### No qual o circuito com R1, R5, Q2 e Q3 é uma fonte de corrente constante para polarizar o diodo zener D3. Vamos projetar?

> ![figura5](https://user-images.githubusercontent.com/12564754/116311196-5c887a80-a781-11eb-9104-b52fe3d1118e.PNG)

##### Podemos melhorar mais ainda? Que tal deixar essa fonte com valor ajustável? Como fazer isso?
###### Podemos por um potenciometro em paralelo com o zener para regular a tensao de referencia.

##### c) Escolhendo o transistor M1 e calculando R2 e R3.
> ###### Mosfet IRF540
> - Qual a corrente contínua necessária?
> ###### 1,1A
> - Quais os limites de tensão para este circuito?
> ###### 16,2V
> - Quais os os parâmetros L, W, uo, Cox, VA e Vt?
> ###### Vt = VGS - VDS -> VDS = VGS, logo Vt segundo o datasheet está entre 2 a 4V
> ###### 
> - Calcule o valor de RDS para as tensões VGS de 2V, 3V, 4V, 5V e 10V
> ######
> - Quais as tensões máximas de operação deste componente?
> ######
> - Obtenha as curvas ID x VDS para esse componente para as tensões VGS de 2V, 3V, 4V, 5V e 10V e compare os resultados com as curvas presentes no Datasheet.
> ######
> - Utilizando a curva ID x VDS obtenha os valores RDS e compare com os valores teóricos.
> ######
> - Qual o valor da capacitância de gate?
> ######
> - Justifique a escolha dos resistores R2 e R3.
> 

### Parte 03: Adicionando um circuito de proteção de sobre corrente ao regulador linear

##### O que é sobrecorrente? 
> É uma carga de corrente que possui magnitude acima da qual o equipamento foi projetado para funcionar. 
##### Quais os impactos neste circuito?
> trenar corrente do mosfet M1 e ampop de modo a queimar ambos.
##### O que deve fazer um circuito de proteção de sobrecorrente? 
> Evitar que o circuito opere com corrente acima do dimencionamento do circuito. Esta protecao pode ser feita de dois modos, desarmando o circuito para que pare de operar, ou diminuir a tensao para manter o circuito operado em 1,1A.

##### Exemplo de circuito:

> ![figura6](https://user-images.githubusercontent.com/12564754/116313992-e5ed7c00-a784-11eb-83b3-58cb9f170a82.PNG)