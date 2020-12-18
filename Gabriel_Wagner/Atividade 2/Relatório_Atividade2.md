# Atividade 2
Aluno: 
* Gabriel Wagner - <gabrielstd545@gmail.com>

Professores: 
* Daniel Lohmann

## Exercício 1

### Amplificadores Operacionais
Os amplificadores operacionais são circuitos integrados capazes de realizar várias diversas funções, medição de tensões com isolamento elétrico, amplificação de sinais e operações aritméticas. O ampop oferece muitas outras opções dependendo do circuito empregado.
Seus terminais são: Entrada inversora, entrada não inversora, terminais de alimentação e saída.

### Ampop Ideal
Figura 1 - Ampop Ideal

![](ampop_ideal.png)

Referência: http://intranet.deei.fct.ualg.pt/AC/Sebenta_Online/www.isr.uc.pt/~paulino/cse/Sebenta_Online/cap_15/ampopid.htm

No ampop ideal as impedâncias de entrada são infinitas, ou seja, não entram correntes no ampop pelas entradas inversora e não inversora.
A impedância de saída é igual a zero. Isso significa que toda tensão da saída será aproveitada por uma provável carga.
O ganho do ampop ideal é infinito. Tomando pela equação do ampop ideal (V0 = A*(V+ - V_)), qualquer diferença de tensão entre as entradas inversora e não inversora resultará em uma tensão infinita na saída.


### Malha aberta
A malha aberta é uma configuração onde o ampop não apresenta realimentação, tanto positiva quanto negativa. O ganho nessa configuração apresenta um valor muito alto, teoricamente infinito.

### Malha fechada
A malha fechada é uma configuração onde o ampop apresenta realimentação, usualmente negativa. O ganho nessa configuração apresenta valores menores que em malha aberta.

### Cálculo de malha fechada

Os cálculos em malha fechada dependem muito dos reistores empregados, anteriormente tínhamos ganhos muito altos, teoricamente infinitos, mas na malha fechada isso não acontece.
Tomando como exemplo o amplificador inversor, temos que:

Figura 0 - Inversor

<img src="inversor.png" width="500">

Vout = Av * (V+ - V-), no circuito inversor V+ = 0, então:

Vout = Av * (0 - V-).

Fazendo a malha de realimentação e passando o sinal de negativo para fora dos parênteses temos que:

Vout = - Av * (V3 + R1 * i).

Olhando para o circuito sabemos que a corrente neste nó é, i = (Vin - Vout) / (R1 + R2), substituindo i na equação, temos:

Vout = - Av * (V3 + R1 * (V3 - Vout) / (R1 + R2)).

Isolando Vout temos que:

Vout = - V3 * R2 / ((R1+R2)/Av + R1).

Perceba que se colocamos o ganho Av como infinito, como na malha aberta, voltamos para a equação original do ampop inversor:

Vout = -(R2/R1) * V3.

### Buffer

Figura 2 - Buffer

<img src="buffer.png" width="500">

O buffer é uma implementação do ampop onde a tensão de entrada será a mesma tensão na saida. Muito utilizado quando você quer saber a tensão em uma parte do circuito, por exemplo em um resistor shunt, verificando assim a corrente naquela parte do circuito. A utilização do buffer para medição de tensão é muito interessante pois o ampop faz um isolamento elétrico entre ampop e circuito, pois a impedância de entrada do ampop é muito alta.

### Amplificador Inversor

Figura 3 - Inversor

<img src="inversor.png" width="500">

O amplificador inversor tem a função de amplificar ou atenuar o sinal de entrada, jogando uma tensão com sinal contrário na saída.

Vout = Ganho * Vin

Sendo o Ganho = -R2/R1, lembrando que R2 é o resistor na realimentação e R1 o resistor da tensão de entrada.

### Amplificador Não Inversor

Figura 4 - Não Inversor

<img src="nao_inversor.png" width="500">

O amplificador não inversor tem a função de amplificar ou atenuar o sinal de entrada, jogando uma tensão com o mesmo sinal na saída.

Vout = Ganho * Vin

Sendo o Ganho = 1 + (R2/R1), lembrando que R2 é o resistor na realimentação e R1 o resistor ligado ao terra.

### Amplificador Somador Inversor

Figura 5 - Somador Inversor

<img src="somador_inversor.png" width="500">

O amplificador somador inversor faz os somatórios das tensões que entram no terminal inversor, e libera esse resultado na saída.
O somador inversor segue a seguinte equação.

Vout = -RF * (V1/R1 + V2/R2 + V3/R3 ... Vn/Rn)

Conforme você vai adicionando mais sinais, a equação aumenta até n fontes e por conseguinte n resistores. 

### Amplificador Somador Não Inversor

Figura 6 - Somador Não Inversor

<img src="somador_nao_inversor.png" width="500">

O amplificador somador não inversor faz os somatórios das tensões que entram no terminal não inversor, e libera esse resultado na saída.
O somador não inversor segue a seguinte equação.

Vout = (1 + RF/RA) * (V1/R1 + V2/R2 + V3/R3 ... Vn/Rn)

Conforme você vai adicionando mais sinais, a equação aumenta até n fontes e por conseguinte n resistores. 

### Subtrator

Figura 7 - Subtrator

<img src="ampopsubtrator.png" width="500">

O ampop subtrator subtrai os sinais que entram nas saídas inversora e não inversora e joga essa tensão na saída, amplificado, atenuado ou de mesmo módulo.
A equação completa do subtrator é a seguinte:

Vout = (V1*(-R3/R1)) + (V2*(R4/(R2+R4)) * (1 + R3/R1)) + (Vref*(R2/(R2+R4)) * (1+(R3/R1)))

Como no nosso exemplo o Vref é igual a zero temos a seguinte equação:

Vout = (V1*(-R3/R1)) + (V2*(R4/(R2+R4)) * (1 + R3/R1)) + (0*(R2/(R2+R4)) * (1+(R3/R1)))
Vout = (V1*(-R3/R1)) + (V2*(R4/(R2+R4)) * (1 + R3/R1))

Fazendo a aproximação onde R1=R2 e R3=R4 temos a seguinte equação:

Vout = (V2 - V1) * (R3/R1)

Onde rapidamente se percebe que o ganho do subtrator é G = R3/R1

### Amplificador de Instrumentação

Figura 8 - Circuito com três ampops para instrumentação 

<img src="instrumentação.png" width="500">

O circuito com ampops de instrumenação funciona como um subtrator com um inversor em cada entrada.
Devido aos inversores na entrada, a impedância de entrada tem valor altíssimo, diminuindo as correntes de entrada do circuito.
Além disso, o circuito apresenta uma grande atenuação do sinal de modo comum, ou seja alto CMRR, e apresenta também baixo offset.
Esse circuito é muito utilizado em equipamentos de medição e teste.

A equação que rege o amplificador de instrumentação com três ampops é a seguinte:

Vout = (V2 - V1) * Ganho + Vref. Sendo arbitrado Vref = 0.

O ganho para este circuito é Ganho = (R4/R3) * (1+((2 * R5)/R10)).

Por facilidade arbitramos os resistores de alimentação iguais, ou seja R5 = R6. Dando como exemplo o valor de 10K ohms. 
Para colocarmos o ganho de Vref = 1 V/V, mantendo um alto valor de CMRR, precisamos que R4 seja igual a R3, e R2 seja igual a R1.
Facilitando ainda mais a compra de componentes pode ser estabelecido valores iguais para todos os quatro resistores, por exemplo 10K ohms.
Percebe-se assim a necessidade de resistores de precisão, pois o menor descasamento afetaria as características do circuito.
Depois de estabelecermos os valores dos reistores, nota-se que somente R10 não foi escolhido, ele será o resistor que define o ganho deste circuito.

Se quisermos por exemplo um Ganho = 10V/V, R10 deve ser:

Ganho = (10k/10k) * (1+((2 * 10k)/R10)) = 10 V/V.

10 = (1+(20k/R10))

9 = 20k/R10

R10 = 2222.2 ohms.

### Ganho de malha aberto finito
Para demonstrar as diferenças deste ganho finito, compararemos o ganho nominal com o ganho em malha fechada do ampop inversor. Variaremos o ganho nominal de -1000 e -10 para o inversor e 1000 e 10 para o não inversor. Além disso, variaremos Av em 10000 e 100.

#### Inversor

erro = (|G| - (R2/R1)) / (R2/R1) * 100

Av | Módulo de (-R2/R1) | Módulo de G | Erro (%)
-- | ------------------ | ----------- | --------
10000 | 1000 | 909 | 9,1
100 | 1000 | 90,83 | 90,9
10000 | 10 | 9,98 | 0,2
100 |10 | 9,01 | 9,9

#### Não Inversor

erro = (G - (1+(R2/R1))) / (1+(R2/R1)) * 100

Av | 1+(R2/R1) | G | Erro (%)
-- | --------- | - | --------
10000 | 1000 | 909 | 9,1
100 | 1000 | 90,9 | 90,9
10000 | 10 | 9,99 | 0,1
100 |10 | 9,09 | 9,1

Para ambos os casos, percebe-se que conforme o valor de Av aumenta em direção ao ganho de malha aberta, menor o erro é.

### Tensão de modo comum (Vcm) e ganho em modo comum (Acm)
A tensão de modo comum, são as tensões idênticas em fase e módulo nas entradas inversoras e não inversoras. Você pode calcular essa tensão pela expressão:

Vcm = (Vin+ + Vin-)/2

A tensão de modo comum surge na saída amplificada por um ganho em modo comum, idealmente zero, como um acréscimo a diferença dos sinais de entrada. A expressão que rege essa soma de tensões é:

Vout = Ad * Vin + Acm * Vcm

Sendo Ad o ganho da diferença dos sinais e Acm o ganho em modo comum, predicial ao ampop.
Um dos problemas que a tensão de modo comum causa, é a limitação das tensões de entrada e saída, que serão faladas posteriormente.

### Razão da rejeição de modo comum (CMRR)
A razão da rejeição de modo comum é uma característica importantíssima do ampop, pois ela define a razão do ganho da diferença dos sinais das entradas inversora e não inversora pelo ganho da tensão de modo comum.

CMRR = Ad / Acm. 
Sendo Ad o ganho da diferença dos sinais e Acm o ganho da tensão de modo comum.
Lembramos que o ampop trabalha com a amplificação de sinais diferentes, então um alto CMRR é o ideal para o ampop. Podemos salientar também que quanto maior o ganho Acm, maior a tensão de modo comum, prejudicial para o ampop, significando por conseguinte um CMRR menor.

### Influência da tolerância dos resistores no CMRR
Para analisar o efeito do descasamento dos resistores, foi montado dois circuitos subtratores com ganho 1000 V/V. Os resistores de realimentação foram variados em uma taxa de 1% e 5%. Segue a montagem abaixo.

Figura 9 - Montagem dos dois subtratores

<img src="subtrator_tolerancia.png" width="500">

Com essa variação a tensão de saída de ambos ampops variou diferentemente.

Segue abaixo as tensões de saída do LT1001A e as tensões de saída do OP296:

Figura 10 - Tensões de saída do LT1001A

<img src="subtrator_tolerancia_lt.png" width="500">

Figura 11 - Tensões de saída do OP296

<img src="subtrator_tolerancia_ad.png" width="500">

Percebe-se que o efeito do descasamento de resistores é maior no ampop OP296.

### Limitações das tensões de entrada e saída do ampop

Devido a tensão de modo comum e as oscilações das tensões de saída, que são problemas internos do ampop. Os amplificadores apresentam limitações nas tensões de entrada e saída.

Podemos observar através da imagem abaixo:

Figura 12 - Limitações de entrada e saída, training Texas Instruments

<img src="input_output_limitations_trainingti.png" width="500">

Referência: Training Texas Instruments; https://training.ti.com/ti-precision-labs-op-amps-input-and-output-limitations-non-linear-behavior

Observa-se que o ampop está sendo alimentado com 5V na alimentação positiva e 0V na negativa.
As tensões nas entradas inversora e não inversora serão limitadas por:

0-0,1 no limite inferior de tensão de entrada, e 5-3,5 no limite superior das tensões de entrada.

O mesmo acontece com as tensões de saída, com:

0+0,2 no limite inferior de tensão de saída, e 5-0,2 no limite superior das tensões de saída.

Tomando como exemplo o LM324 podemos encontrar rapidamente as limitações no datasheet. Como na imagem abaixo:

Figura 13 - Limitações de entrada e saída, LM324, Texas Instruments

<img src="input_output_limitations_lm324.png" width="500">

Referência: LM324; Texas Instruments; https://www.ti.com/lit/ds/symlink/lm324.pdf?ts=1608243756511&ref_url=https%253A%252F%252Fwww.ti.com%252Fproduct%252FLM324

O datasheet demonstra como em algumas condições você pode mitigar essas limitações. Dando como exemplo a escolha das tensões de alimentação e a resistência de carga que o ampop está trabalhando.

### Ampop Rail-to-rail
Ampops eram comumemte alimentados com alimentação única, VCC na alimentação positiva e 0V na alimentação negativa. Como demonstrado anteriormente, isso gerava uma baixa variação de tensões nas entradas e saídas, que são limitadas por problemas internos, para aumentar a variação ou alcance das tensões de entrada foram construídos os ampops rail-to-rail, eles apresentam alimentação dupla e simétrica, com +VCC na alimentação positiva e -VCC na alimentação negativa. Essa característica diminui muitos as limitações de entrada e saída além de problemas com ruído.








