Curso Superior em Engenharia Eletrônica

Unidade Curricular: Eletrônica  I

Professor: Daniel Lohmann

Aluno: Ramon Busiquia Serafim


# Laboratório Final



## Parte 1: Entendendo um regulador linear.



**Qual relação entre a tensão de alimentação do ampop e a tensão de saída?**.

Tensão de alimentação do AmpOp deve ser maior que a tensão de saída para que o mesmo nao sature. Para não ocorrer esse problema devemos verificar no datasheet e analisar as tensões de alimentação do AmpOp

**O que devemos considerar para esse circuito operar como um LDO?**

Uma baixa queda de tensão no mosfet. Potência dissipada no mosfet é diretamente proporcional a corrente que passa por ele e pela diferença de potencial


**Como obter as tensões de alimentação para o AmpOp (VCC e VEE)?**
Após verificar o datasheet, utilizaresmos um dobrador de tensão para obter a tensão VCC e conectaremos o VEE no gnd.



**Utilizando o circuito dobrador de tensão, qual valor de VCC você obtêm para um sinal Vin+ de 12Vrms?**

12Vrms= 12*(2/sqrt(2))Vp

Vp=16.97V

​		VCC= 2 * Vp - 2 * Vd

​		VCC= 2 * 16,97 - 2 * 0,7

​		VCC= 32,54V





**Quais problemas apresentam esse circuito? Podemos melhorar?**


Esse circuito apresenta variação na tensão de ripple, isso ligado a alimentação do AmpOp pode ocasionar ruído na saída do circuito. Para melhorar podemos utiliz um regulador linear que ajuda a eliminar ruídos do circuito.    

Circuito Dobrador de tensão:

<img src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-2/Ramon_Serafim/Lab_Final/dobredor%20de%20tensao%20sem%20reg.PNG?raw=true">

Simulação Dobrador de tensão:

<img src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-2/Ramon_Serafim/Lab_Final/simula%C3%A7ao%20dobrador%20de%20tensao%20sem%20reg.PNG?raw=true">


Vamos projetar esse circuito de alimentação do AmpOP?
Considere: AmpOp LM324, MOSFET IRF540, VOUT = 15V, IOUT = 1A, vin+ = 12Vrms, vripple_pós_retificador = 1V, considere as quedas de tensão nos diodos de 0,7V.
Pontos Importantes para iniciar o projeto responda justificando as escolhas.


• **Qual a Tensão VGS? Descreva como obter o valor.**


Visualizar no datasheet do componente, encontrar o gráfico IDxVGS, encontrar a corrente desejada que nesse caso é 1A e traçar uma reta até encontrar a tensão que satisfaz a curva, nesse caso foi encontrado uma tensão VGS de 4V.

<img  src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-2/Ramon_Serafim/Lab_Final/IDxVGS.PNG?raw=true">


• **Qual a corrente de alimentação do AmpOp?**

		De 1mA até 3mA.

• **Qual a tensão de alimentação do AmpOP?**

		±16V sendo máximo 32V. Nesse projeto utilizaremos VEE conectado ao ground.

• **Qual fator devo considerar para escolher o transistor Q1?**

		Um beta elevado, BC547C possui em média de 520 (entre 420 a 800).

• **Qual valor da tensão do diodo zener D6?**

		Considerando a saida do AmpOp maior que 20V devido o VGS ser 4V. Em uma margem a tensão do diodo seria 15+4= 19V. Tensão do diodo deverá 		ser maior que 19V para satisfazer o circuito.

• **Como escolher o diodo zener D6, maximizando a eficiência energética e minimizando os ruídos no circuito?**

		Escolher um zener que utilize a menor corrente possível, escolhendo um zener com um resistor zener bem pequeno.

• **Considere que, por alterações futuras no circuito, o AmpOp poderá ter uma aumento de 10mA na corrente de alimentação, o circuito proposto continuará funcionando?**

		Sim, se a corrente de alimentaçao for maior do que a mínima pedida no datasheet o circuito continuará funcionando.

Projete o circuito de alimentação do AmpOp com as especificações acima.


Circuito  Dobrador de tensão com regulador linear:

<img src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-2/Ramon_Serafim/Lab_Final/Dobrador%20de%20tens%C3%A3o%20com%20reg%20linear.PNG?raw=true">

Simulação Dobrador de tensão com regulador linear:

<img src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-2/Ramon_Serafim/Lab_Final/simulacao%20dobrador%20de%20tensao%20com%20reg%20linear.PNG?raw=true">




## Parte 2

##### Calculando e dimensionando os componentes



**a) Para o primeiro bloco (D1, D2 e C1) considere vin+ = 12Vrms, vripple_pós_retificador = 1V e I_carga = 1,1A. Justifique a escolha dos componentes.**

		Para calcular o valor do capacitor utilizamos a formula abaixo:
    

​		C1= Icarga/2 * f * Vripple

​		C1= 1.1/120

​		C1= 9.2mF


​		Devemos analisar o pico de corrente em cima do diodo, na simulação estava apresentando 4A de pico, primeiramente escolhi o 1N4148 mas ele 		suporta um pico de 2A somente, após rever alguns diodos foi escolhido o 1N4001 que possui pico de corrente de 30A, utilizável para a aplicação que 		queremos.

Circuito Retificador de onda:

<img  src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-2/Ramon_Serafim/Lab_Final/Retificador%20de%20onda.PNG?raw=true">

Simulação antes e pós retificador de onda (vermelho = pós retificador):

<img  src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-2/Ramon_Serafim/Lab_Final/simula%C3%A7ao%20antes%20e%20p%C3%B3s%20retificador%20de%20onda.PNG?raw=true">

Visualizando a tensão_de_ripple pós retificador:

<img  src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-2/Ramon_Serafim/Lab_Final/simulacao%20vripple%20pos%20retificador.PNG?raw=true">


**b) Circuito referência de tensão zener (R1 e D3):**


**• Quais fatores devo considerar para escolher o diodo zener para essa aplicação?**

		Menor ruído na saída, resultando em um diodo com resistência zener baixa.

• **Qual a influência da regulação de linha e da regulação de carga para este circuito?**		

Regulação de linha influência a estabilidade da fonte em relação a tensão de entrada, caso apresente muita oscilação nesse momento irá haver efeito cascata em todo o resto do circuito, afetando a saída do AmpOp, entre outros. Regulação de carga afeta a carga  própriamente dita, caso haja muito ruído em  cima da carga pode haver erro de leitura em alguns circuitos, como nesse caso utilizamos uma carga exemplar não haveria problema.


• **Qual o impacto da regulação linha / carga do circuito com o diodo zener na tensão de saída do regulador linear?**		

Regulação de linha pode afetar a tensão de zener,  mostrando essa oscilação na saída. Para não apresentar essa variação a resistência de zener precisa ser baixa. Regulação de carga representa a corrente que deixa de passar no zener e vai para a carga,  pode influen no circuito, geralmente diminuir a tensão de zener.


**Podemos melhorar esse circuito? Quais problemas podemos identificar nesta topologia?**

Sim, utilizar uma fonte de corrente. A corrente  será constante no zener, a tensão não varia.


No qual o circuito com R1, R5, Q2 e Q3 é uma fonte de corrente constante para polarizar o diodo
zener D3. Vamos projetar?

Utilizando transistores 2N2907 para fazer a fonte de corrente, suporta a corrente e tensão necessarias para o circuito. Corrente que passa no resistor R1 é a mesma que passa no D3 (em teoria). R5 acaba por ser um resistor grande, no mínimo 14kΩ.


<img  src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-2/Ramon_Serafim/Lab_Final/Fonte%20corrente%20continua.PNG?raw=true">


**Podemos melhorar mais ainda? Que tal deixar essa fonte com valor ajustável? Como fazer isso?**

Podemos colocar um circuito sobrecorrente que determina a faixa de operação da fonte.



**c)Escolhendo o transistor M1 e calculando R2 e R3.**

**• Qual a corrente contínua necessária?**

		O pré-requisito do projeto é que a corrente no transistor M1 seja 1A.



**• Quais os limites de tensão para este circuito?**

		O circuito fica limitado no valor de tensão retificado que fica por volta de 17V.


Ao escolher o transistor obtenha:

**Quais os os parâmetros L, W, uo, Cox, VA e Vt?**


Verificando a .lib juntamente com o datasheet podemos verificar os parâmetros.

		
L=100uH


W=100uW

		
LAMBDA =  0.00291031	

		
u0 (valor padrão) = 600 cm²/V/s


C0x = KP/u0 = 25,0081/600 = 41,68 mF/m²


VA = 1/LAMBDA = 1/0.00291031 = 343,61 v


Vt = 3.56362 V


**Quais as tensões máximas de operação deste componente?**

Segundo o datasheet, Vds possui limite de 100V e  Vgs possui limites de ±20V.

<img  src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-2/Ramon_Serafim/Lab_Final/tensoes%20maximas.PNG?raw=true">


**Obtenha as curvas ID x VDS para esse componente para as tensões VGS de 2V, 3V, 4V, 5V e 10V e compare os resultados com as curvas presentes no Datasheet.**

<img  src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-2/Ramon_Serafim/Lab_Final/IDxVGS.PNG?raw=true">


**Qual o valor da capacitância_de_gate?**

<img  src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-2/Ramon_Serafim/Lab_Final/capacitancia%20de%20gate.PNG?raw=true">


**Justifique a escolha dos resistores R2 e R3.**

Afim de encontrar 15V em Vout, calculamos o ganho na topologia do AmpOp não inversor para encontrar o resultado de 15V.

Vout= ((R2/R3)+1)* Vin

(Vout/Vin) - 1= R2/R3

15/12 - 1= R2/R3

R2/R3 = 1/4

Utilizando resistores grandes para uma menor corrente, foi utilizado resistores de 25 e 100k.



## Parte 3

##### Adicionando um circuito de proteção de sobre corrente ao regulador linear.

Cálculo do resistor saindo do ampop, VCC/(corrente desejada geralmente 10m) = R6

		R6 = 23,64/10m
		R6 = 2364Ω


**Primeiramente reflita e pesquise sobre o que é sobrecorrente?**

		Sobrecorrente é o excesso de corrente presente no circuito, quando excede o valor nominal. Pode ser classificada em curto-circuito e sobrecarga, a 		diferença das duas é o tempo de operação. Curto-circuito é um pico elevado de corrente em um espaço de tempo muito pequeno, já a sobrecarga é 		o valor da corrente acima da nominal por um longo tempo.



**Quais os impactos neste circuito?**

		Caso ocorra uma sobrecorrente independente do caso pode danificar os componentes do circuito e/ou diminuindo a vita útil do projeto junto com a 		eficiência do mesmo.



**O que deve fazer um circuito de proteção de sobrecorrente?**

		Um circuito de proteção deve interromper a corrente que circula no circuito de alguma maneira, dependendo do circuito de proteção, impor limites 		de corrente para não danificar os componentes.



**O que é a proteção foldback?**

		Proteção contra curto-circuito foldback: é um método usado em fontes de alimentação para protegê-las de situações como curto-circuito na saída 		com um fio ou conexão de muitos equipamentos à fonte de alimentação. Quando a tensão cai, o limite de corrente também cai de maneira linear. 		Isso fornece proteção mais segura contra curtos-circuitos, pois um curto-circuito "muito ruim" resultará em pouco consumo de corrente, para que o 		suprimento não fique recebendo uma corrente máxima. Foldback sobre a proteção de corrente é melhor e mais seguro do que apenas ter uma alta 		limitação de corrente lateral.

Circuito Fonte Completa junto com proteção sobrecorrente:

<img  src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-2/Ramon_Serafim/Lab_Final/fonte%20completa.PNG?raw=true">

O valor do resistor na saída do AmpOp de proteção foi encontrado arbitráriamente, o Resistor de 100kΩ na prática é utilizado um potenciômetro de 100k.

Demonstrando a tensão_de_ripple em cima da carga:

<img  src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-2/Ramon_Serafim/Lab_Final/ripple%20de%20saida.PNG?raw=true">



**Pesquise as topologias disponíveis, caso deseja-se fazer um circuito LDO, o que devemos levar em consideração para o regulador?**

​		**(LDO - Low Dropout)** Para se conseguir que os dispositivos usados no controle da corrente sobre a carga apresentem uma baixa queda de tensão, 		existem diversas possibilidades que são dadas por configurações, usando transistores comuns como transistores de efeito de campo de potência.

​		As configurações apresentadas têm, entretanto, limitações que devem ser consideradas em cada projeto. Analisemos as características dessas
configurações como:

Vmin - trata-se da tensão mínima de entrada com que pode operar a configuração.
IL       - corrente de carga
Zout - impedância de saída
BW   - Faixa passante



**a) Transistor NPN**
Nesse caso o transistor opera como seguidor de emissor com uma baixa impedância de saída e uma faixa passante (BW) larga.
\* Vmin = 1 V
\* IL = < 1 A



**b) Darlington NPN**
Com um par Darlington operando como seguidor de emissor temos uma baixa impedância de saída e uma faixa passante larga. No entanto:
*Vmin = 2 V
\* IL > 1 a



**c) Transistor PNP**
Essa é uma configuração interessante para LDOs, pois usando o transistor como inversor temos uma alta impedância de saída, uma faixa estreita mas uma tensão de entrada muito baixa.
\* Vmin = 0,1 V
\* IL < 1 a



**d) Par PNP/NPN**
Nessa configuração temos transistores complementares funcionando como inversores, obtendo-se uma alta impedãncia de saída e uma faixa passante estreita. Além disso:
\* Vmin = 1,5 V
\* IL > 1 A



**e) PMOS**
Usando um transistor de efeito de capo PMOS a tensão mínima de entrada será dada pelo produto:
Rds(on) x IL





### Algumas topologias encontradas em LDOs comerciais

As principais características são comuns, mas existem diferenças em alguns pontos, as quais devem ser consideradas no tipo específico para uma aplicação.



**Topologia Tradicional**

Na figura 5 temos a arquitetura tradicional de um LDO que faz uso de um transistor PNP para controlar a corrente principal. Esse transistor tem um transistor NPN controlado por um comparador de tensão como elemento que determina a sua condução. Na mesma configuração pode também ser usado um transistor de efeito de campo de potência de canal P (PMOS).

A principal característica dessa configuração está no uso de um transistor de potência de baixo ganho, excitado por uma alta corrente de base, o que permite obter uma baixa queda de tensão entre o coletor e o emissor, nas condições desejadas de operação.

Um circuito desse tipo pode apresentar quedas de tensão típicas de 0,3 e 0,6 V com uma corrente de 150 mA. Um ponto importante que deve ser levado em conta nesse tipo de regulador é que a carga é ligada ao coletor do transistor, ou seja, ele opera na configuração de emissor comum. Isso significa que a carga vê a fonte como um circuito de alta impedância.



**Topologia Pole-Splitting**

Essa configuração é mostrada na figura 6, usando também como elemento principal de controle ou dispositivo de passagem, tanto um transistor PNP como um MOSFET de potência de canal P.

Nesse circuito destaca-se o capacitor de compensação (Ccomp) interno ligado entre o coletor e a base do transistor. Esse componente ajuda a evitar os problemas que podem ser causados pela presença de C1 no circuito de entrada.

Essa configuração não é das melhores pois a presença de C1 afeta a rejeição de ripple da fonte que, não é das melhores.



**Topologia AnyCAP**

Essa é uma topologia desenvolvida pela Analog Devices (www.analog.com) que, conforme o nome sugere, permite o uso de capacitores de qualquer valor no circuito de entrada, sem que isso afete a rejeição de ripple e outras características do regulador. Na figura 7 temos um exemplo dessa topologia de LDOs de baixa corrente da Analog.

Com essa topologia a Analog tem como exemplo o circuito integrado ADP33O0 que fornece tensões de saída de 2,7 V a 5 V com uma queda de tensão de apenas 0,3 V apenas. Isso significa que numa fonte de 5 V ele pode ser alimentado com tensões a partir de 5,3 V.

Na figura 8 temos uma sugestão de circuito de aplicação com esse componente.



**Controladores Reguladores**

Uma outra categoria de regulador de tensão que pode ser empregado no projeto de LDO é o controlador de regulador. A diferença básica entre um regulador completo e o controlador de regulador é que no controlador de regulador, o transistor de potência ou de passagem, é um componente externo.







Link para as topologias:

https://www.newtoncbraga.com.br/index.php/como-funciona/6102-art767.html




Datasheets:

AmpOp LM324:

https://www.ti.com/lit/ds/symlink/lm324.pdf?ts=1618824027289&ref_url=https%253A%252F%252Fwww.ti.com%252Fproduct%252FLM324




MOSFET IRF540:

https://www.vishay.com/docs/91021/91021.pdf



NPN BC547C:

https://datasheetspdf.com/pdf/128408/ONSemiconductor/BC547C/1 



1N4001:

https://www.vishay.com/docs/88503/1n4001.pdf
