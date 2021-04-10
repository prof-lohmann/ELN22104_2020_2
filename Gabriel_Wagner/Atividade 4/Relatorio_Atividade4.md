# Atividade 4
Aluno: 
* Gabriel Wagner - <gabrielstd545@gmail.com>

Professores: 
* Daniel Lohmann

## Parte 01: Entendendo um regulador linear

### Princípios de regulação de tensão
A regulação de tensão é um método em que se deseja manter a tensão de certa parte do circuito praticamente constante, mesmo na mudança de alguns aspectos desse circuito,
como tensão de entrada, valor da carga, entre outros.

### Tensão de saída
A tensão de saída após o retificador deve ser contínua, bem como continua em relação ao tempo.

### Tensão de ripple
A tensão de ripple é comumente associada a uma tensão retificada e filtrada por um capacitor. Ela é muito importante quando queremos converter uma tensão alternada em uma
tensão contínua.
Seu valor é dado pela subtração da tensão superior menos a tensão inferior, depois de filtrada e retificada.

### Regulação de linha
A regulação de linha é um importante aspecto da regulação de tensão. Quando estamos alimentando qualquer circuito, não queremos que essa tensão de alimentação varie muito.
A regulação de linha mede essa variação, comparando a variação da tensão de saída pela tensão de entrada. Dada pela fórmula:
Regulação de linha = (delta Vout) / (delta Vin)
Sendo expressada em V/V.

### Regulação de Carga
Enquanto isso, quem regula a tensão de saída quando diferentes cargas são conectadas, é o regulador de carga. O regulador de carga segue a seguinte fórmula:
Regulação de carga = (delta Vout) / (delta Iout)
Sendo expressada em V/A.

### Conceito de LDO – Low Dropout Voltage
Da forma mais básica que se pode explicar, LDO é o mínimo delta que se pode alcançar entre as tensões de entrada e saída, mantendo o funcionamento da regulação do circuito.
Essa característica é definida principalmente pela tensão VDO.
A tensão VDO, é a tensão diferencial mínima que a tensão Vin deve manter acima da tensão Vout, para uma regulação correta.
A equação que descreve esse comportamento é:

Vin >= Vout + VDO

Se Vin diminuir para um valor menor que (Vout + VDO) o regulador linear irá entrar em operação de "dropout", não regulando a tensão de saída desejada.
Nesse estado a equação que rege o regulador é:

Vout = Vin - VDO

## Parte 01.1:

<img src="1.jpg" width="500">

* Qual relação entre a tensão de alimentação do ampop e a tensão de
saída?

A tensão de saída sempre será limitada pela alimentação do ampop, bem como as limitações do próprio ampop em relação a tensão na saída, que podem restringir essa tensão
em um valor menor que as tensões de alimentação.

* O que devemos considerar para esse circuito operar como um LDO?

Utilizando a equação do LDO (Vin >= Vout + VDO) podemos discutir pontos importantes.

Vin  -> A tensão de entrada será limitada pela escolha do diodo zenner.

Vout -> A tensão de saída será limitada por questões do ampop, como explicado anteriormente(tensões de alimentação e limites na saída).

* Como obter as tensões de alimentação para o AmpOp (VCC e VEE)?

As tensões de alimentação devem ser maiores que a soma da tensão de zenner e a queda de tensão VGS no transistor NMOS.

## Parte 01.2:

<img src="2.jpg" width="500">

* Utilizando o circuito dobrador de tensão, qual valor de VCC você obtêm para um sinal Vin+ de
12Vrms?

O circuito dobrador de tensão segue a seguinte fórmula:

Obs.: Consideraremos a tensão de entrada muito maior que a queda de tensão nos diodos.

Vout = 2* Vinpico -VD1 - VD2

Para um sinal de 12rms temos uma saída de:

Vout = (12 * raiz(2)) * 2 - 0,7 - 0,7
Vout = Aproximadamente 32 V

* Quais problemas apresentam esse circuito? Podemos melhorar?

Esse circuito apresenta ondulação devido a tensão de ripple, então deve-se tomar cuidado na escolha do capacitor, levando em conta o tempo de carga do capacitor, que será longo se o valor do capacitor for alto, e a ondulação, que será alta se o valor do capacitor for baixo.

Além disso, sabemos que a saída está em funcão de aproximadamente duas vezes a tensão de entrada, onde um surto de tensão poderá acarretar em mal funcionamento na alimentação do ampop.

Podemos melhorar o circuito fazendo o balanço correto na escolha do capacitor e além disso, podemos adicionar um regulador linear de tensão na saída do dobrador, limitando a tensão de saída que irá alimentar o ampop.
 
## Parte 01.3:

<img src="3.jpg" width="500">

* Qual a Tensão VGS? Descreva como obter o valor

A tensão VGS é a tensão gate-source do MOS, é a tensão que polariza esse transistor, possibilitando a passagem de corrente, além disso é a tensão que controla a resistência
RDS dele. Quanto maior a tensão VGS, menor a resistência RDS desse MOS.

Podemos perceber através do circuito empregado, que a tensão VGS para esse circuito, é a subtração entre a tensão de saída do ampop U1 e a tensão de saída da fonte(Vout).

Tomando a tensão de saída como 15 V, e olhando o datasheet do NMOS IR540, que para uma corrente IDS de 1 A, precisa de uma tensão VGS de 4,5 V, temos que:

Saída do ampop U1 = 4,5 + 15 = 19,5 V

Podemos arredondar para 20 V devido a quedas de tensões que podem variar no circuito.

* Qual a corrente de alimentação do AmpOp?

Olhando o datasheet do LM324, podemos verificar uma corrente de alimentação mínima de 3 mA.

* Qual a tensão de alimentação do AmpOP?

O ampop LM324 pode ser alimentado com até 32 V de alimentação única, pórem ele estará sendo alimentado com uma tensão de 24 V, oferecendo uma margem de erro. É necessária uma tensão de 20 V na saída do LM324, por esse motivo foi escolhida essa margem.

* Qual fator devo considerar para escolher o transistor Q1?

É necessário um hfe ou beta de valor alto, maior que 100. Para que a corrente que alimente a base desse bjt seja muito menor que a corrente do diodo zener.

* Qual valor da tensão do diodo zener D6?

Foi escolhida uma tensão de zener de 24 V, para que o ampop U1 receba tensão suficiente na alimentação, podendo fornecer assim, 20 V na saída.

* Como escolher o diodo zener D6, maximizando a eficiência energética e minimizando os ruídos no circuito?

A resistência de zener deve ser analisada para resolver esse problema. A corrente que atravessa o zener pode variar em algum momento, então é necessário que a resistência de zener seja baixa para que a tensão de regulação do zener não varie muito.

* Considere que, por alterações futuras no circuito, o AmpOp poderá ter uma
aumento de 10mA na corrente de alimentação, o circuito proposto continuará
funcionando?

Sim, se a corrente de alimentação for maior que a mínima corrente de alimentação o ampop continuará funcionando.

## Parte 02: Calculando e dimensionando os componentes

* Para o primeiro bloco (D1, D2 e C1) considere vin+ = 12Vrms, vripple_pós_retificador = 1V e I_carga = 1,1A. Justifique a escolha dos componentes.

Os diodos D1 e D2 devem ter uma queda de tensão menor que 1 V, para que essa queda não consuma grande parte da tensão do circuito. Além disso, ambos devem poder dissipar mais que 18,7 W de potência, sem danificar o componente.

O capacitor C1 será escolhido com base no retificador de onda completa, levando em conta que o produto da capacitância e da resistência de carga são muito maiores que o período da onda. Deste modo temos que:

C = IL/(2 * f * Vr)
C = 1,1/(2 * 60 * 1)
C = 9,17 mF








