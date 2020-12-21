# Atividade 1
Aluno:
* Paulo Cezar Ventura Junior - <paulo.cvj@aluno.ifsc.edu.br>

Professores:
* Daniel Lohmann

## 01. O que é um AmpOp?

Amplificadores operacionais são circuitos integrados (CI) capazes de amplificar um sinal de entrada e também realizar algumas funções matemáticas, como soma, subtração, multiplicação, derivação e integração. Ele possui dois terminais de entrada, um chamado de entrada inversora e outro de entrada não inversora, sendo a inversora geralmente identificada por um sinal negativo, e a não inversora por um sinal positivo. Além deles, possui dois terminais de entrada de alimentação, positiva e negativa (Vcc+ e Vcc-). E por fim temos a saída Vout.

Abaixo temos a figura de um amplificador operacional e seus terminais.

![ampop](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2002/Exemplos/ampop.jpg)

## 02. Mostre os símbolos e as características do AmpOp IDEAL.

O AmpOp ideal possui uma impedância de entrada infinita, ocasionando para que supostamente nenhuma corrente de entrada seja drenada, para que a corrente no terminal inversor (v1) e não inversor (v2) seja igual a zero. No terminal de saída 3, em um AmpOp ideal, temos uma fonte de tensão ideal, sendo sempre igual a v2-v1. Portanto, se tivermos v1=v2 em um AmpOp ideal, teremos teoricamente uma saída igual a zero, sendo chamado de rejeição de modo comum, que será infinita no AmpOp ideal.
Além disso, o AmpOp ideal deve ter um ganho A constante, para amplificar sinal de qualquer frequência, sempre com o mesmo ganho, e esse ganho A deve tender ao infinito.

## 03. O que significa Malha Aberta e Malha Fechada?

Malha aberta é denominado quando o AmpOp não possui realimentação, seja pelo terminal não inversor, ou inversor. Nesse tipo de configuração, possuímos um ganho A no AmpOp com um valor muito alto, porém pouco preciso.
Malha fechada é justamente o contrário, quando o AmpOp recebe realimentação. Essa realimentação por muitas vezes acontece no terminal inversor, porém ela pode ocorrer no terminal não inversor também. Nesse tipo de configuração, trocamos o ganho pela precisão, tendo um ganho menor porém estável e preciso.

## 04. Exemplifique como resolver e calcular circuitos com AmpOps em Malha Fechada.

Existem formas diferentes de análise e resolução de circuitos com AmpOps em malha fechada.

Para essa questão, utilizaremos o exemplo presente no capítulo 2 do livro do Sedra Smith - Microeletrônica.
A figura abaixo representa a configuração do AmpOp na figura 2.4 (Capítulo 2). Este é um Amplificador Operacional Inversor, mas existem outros modelos.

![ampop_2.4](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2002/Exemplos/ampop_2.4.png)

Esse circuito está em Malha Fechada pois o resistor R2 gera a realimentação entre a entrada inversora e a saída.

Podemos determinar o ganho G dessa malha fechada com a equação:

``
G ≡ Vout/v1
``

Por definição, após determinar idealidades no AmpOp (como o fato dele estar em um curto-circuito virtual, por exemplo), chegamos na expressão de ganho em malha fechada:

``
Vout/v1 = -R2/R1
``

Temos, portanto, uma razão entre R2 e R1, com uma inversão no sinal de entrada, indicado pelo símbolo negativo antes de R2.
Conseguimos calcular a corrente i1, determinando da seguinte forma:

``
i1 = v1/R1
``

Como o ganho não é infinito, temos a tensão de entrada como Vout/A. No caso do AmpOp da figura, temos o terminal de entrada positivo aterrado, portanto a tensão no terminal inversor será -Vout/A. Desta forma, a corrente i1 é calculada da seguinte maneira:

``
i1 = [v1 - (-Vout/A)]/R1 = (v1 + Vout/A)/R1
``

E então temos uma tensão de saída Vout:

``
G ≡ Vout/v1 = (-R2/R1)/[1+(1+R2/R1)/A]
``

Basicamente, em um circuito com AmpOp, devemos determinar o ganho do circuito e a partir disto aplicar conceitos elétricos, métodos nodais/de malhas e descobrir a tensão e corrente no circuito, mas sempre se atentando a particularidades do circuito.

## 05. Descreva as principais características das topologias:

#### a. Seguidor de tensão (Buffer);

Um Buffer é um circuito onde temos uma entrada Vin igual a saída Vout. Todo sinal de entrada aparece diretamente na saída, isso devido a alta impedância na entrada do AmpOp, o que gera um bom isolamento elétrico entre o AmpOp e o circuito que está sendo utilizado.
Uma visualização desse circuito pode ser a seguinte:

![ampop_buffer](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2002/Exemplos/ampop_buffer.png)

Onde derivamos de um AmpOp não-inversor, porém com seu resistor R1 em aberto e R2 em curto-circuito. Dessa forma, o ganho do circuito fica da seguinte forma:

``
Vout = Vin * (1 + R2/R1)
``

Como R1 = ∞ e R2 = 0, temos:

``
Vout = Vin * 1 -> Vout = Vin
``

#### b. Amplificador inversor;

O AmpOp inversor tem a característica de amplificar o sinal de entrada com uma tensão contrária na saída. Por exemplo, utilizando uma fonte senoidal, temos um ganho idealmente de relação R2/R1 (R2 sendo o resistor de realimentação, e R1 sendo o resistor da tensão de entrada) porém com fase de 180º em relação ao sinal inicial. Em uma fonte comum, teremos simplesmente um sinal negativo na saída.

#### c. Amplificador não inversor;

Em um AmpOp não inversor, teremos um sinal de saída em mesma fase do sinal de entrada, caso seja uma fonte senoidal, ou de mesmo sinal caso seja uma fonte comum. Porém, diferente do Buffer, ele terá um ganho ou atenuação no sinal, com seu ganho G dado por:

``
G = 1 + (R2/R1)
``

Sendo R2 o resistor da realimentação, e o R1 o resistor ligado ao terra, como podemos verificar na figura abaixo.

![ampop_naoinversor](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2002/Exemplos/ampop_naoinversor.png)

#### d. Amplificador Somador Inversor;

Um AmpOp Somador Inversor consiste em um circuito com mais de um sinal de entrada, cada um com sua resistência correspondente, todos conectados no terminal inversor do AmpOp.
Para tal aplicação, teremos uma corrente i chegando na entrada inversora, onde será a soma de todas as correntes das entradas:

``
i = i1 + i2 + ... + in
``

Portanto, Vout pode ser dado por:

``
Vout = -i*Rf
``

Como i = V/R, temos a equação final:

``
Vout = -Rf*(V1/R1 + V2/R2 + ... + Vn/Rn)
``

Dessa forma, a saída no terminal Vout vai ser o inverso da soma de todas as tensões de entrada, como podemos ver na imagem abaixo.

![ampop_somador_inversor](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2002/Exemplos/ampop_somador_inversor.png)

#### e. Amplificador Somador Não Inversor;

Funciona de maneira parecida com o inversor, porém sua saída não sofre inversão, mas vai funcionar da mesma maneira, com a saída sendo a soma de todas as entradas. Porém, como temos um circuito levemente diferente, temos uma equação também diferente.
O circuito Somador Não Inversor é o da imagem abaixo:

![ampop_somador_nao_inversor](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2002/Exemplos/ampop_somador_nao_inversor.png)

Como dessa vez não temos um dos terminais diretamente ligado ao terra, a equação vai ser um pouco diferente. O resistor Ra aparece no meio do caminho entre o terminal inversor e o terra, portanto temos a equação:

``
Vout = (1 + Rf/Ra) * [(V1/R1 + V2/R2 + ... + Vn/Rn)/(1/R1 + 1/R2 + ... + 1/Rn)]
``

#### f. Subtrator;

O circuito Subtrator permite que obtenhamos em sua saída Vout a diferença entre os sinais de entrada, multiplicada por um ganho determinado pelo circuito.
Dessa forma, temos o seguinte circuito:

![ampop_subtrator](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2002/Exemplos/ampop_subtrator.png)

Note que possuímos apenas resistores de valor R1 e R2 nesse circuito, ou seja, os resistores R1 são de valores iguais entre si, e os resistores R2 também.
Portanto, chegamos a equação do AmpOp Subtrator:

``
Vout = R2/R1*(v2-v1)
``

#### g. Amplificador de instrumentação;

Um amplificador de instrumentação possui algumas características desejadas pela parte de projetos, como uma alta rejeição de sinais de modo comum, impedância elevada nas entradas, baixo offset e baixa corrente de bias (corrente de polarização).
Um modelo de AmpOp de instrumentação é o AD8221. Podemos ver a sua utilização na imagem abaixo.

![ampop_instrumentacao](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2002/Exemplos/ampop_instrumentacao.png)

Dessa forma, temos um CMRR alto, com um ganho também alto, permitindo trabalhar com sinais de amplitude muito baixa.

## 6. Explique o efeito do ganho em Malha Aberta Finito para as topologias Amplificador Inversor e Amplificador Não Inversor.

O fato do ganho em malha aberta ser finito implica que a tensão entre os terminais de entrada do ampop será -Vout/A, isso para um ampop inversor. Portanto, a corrente que passa na entrada inversora será:

``
i1 = [v1 - (-Vout/A)]/R1 = (v1 + Vout/A)/R1
``

Dessa forma, temos que a tensão Vout é:

``
G ≡ Vout/v1 = (-R2/R1)/[1+(1+R2/R1)/A]
``

Isso para um AmpOp Inversor, como o da figura abaixo que será utilzado para análise.

![ampop_inversor](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2002/Exemplos/ampop_inversor.png)

No circuito, definimos o ganho em malha aberta como 60dB, e o ganho em malha fechada originalmente é 10V/V pois R2/R1 = 10. Porém, utilizaremos R1 = 1k e R2 = 1M por enquanto. O cálculo de Vout fica:

```
G = (-R2/R1)/[1+(1+R2/R1)/A]
G = -1000/(1002/1000) = -998V/V

E = |(|-998| - 1000)|/1000*100 = 0,2% de erro percentual
```

Para um ganho em malha fechada original (R1 = 1k ; R2 = 10k), temos:

```
G = -10/(12/1000)
G = -833,33 V/V

E = |(|-833,33| - 1000)|/1000*100 = 16,67% de erro percentual
```

## 7. Explique o que é a tensão de modo comum (Vcm) e quais os efeitos desta tensão nas topologias estudadas.

A tensão de modo comum (Vcm) é a média das tensões das entradas do AmpOp, ou seja, Vcm = (v1 + v2)/2.
Em um Inversor, como não temos tensão no terminal não inversor, a tensão de modo comum é a metade da tensão de entrada.
Em um não inversor, a definição é a mesma.
Na verdade, essa definição acontece para todos as topologias, com exceção do AmpOp Subtrator e do de instrumentação.
A tensão de modo comum implica em um Ganho de Modo Comum. Ou seja, nossa saída Vout em teoria depende da diferença entre as tensões de entrada multiplicada pelo Ganho. Dessa forma, teríamos:

``
 Vout = (v1 - v2)*A
``

Utilizando dois sinais idênticos na entrada, a saída deveria ser sempre 0V, porém na prática, ao aplicar duas tensões iguais diferente de 0V na entrada, vamos sempre ter alguma saída diferente de 0 em Vout.
Por exemplo, digamos que aplicamos, em um AmpOp em malha aberta, 2V na entrada inversora e na entrada não inversora. Em teoria, aplicando a fórmula, não importa qual o ganho, ainda teríamos que medir 0V em Vout.
Mas ao medir, digamos que chegamos em um valor de 50uV. Ele aparece justamente pelo Ganho em Modo Comum, pois há um erro em amplificadores operacionais na prática que acaba gerando um pequeno diferencial de tensão, e multiplicado pelo Ganho gera uma pequena tensão em Vout. Por isso, idealmente a tensão de modo comum é 0, pois implica que com isso não temos Ganho em modo comum.

## 8. O que é CMRR?

CMRR é a sigla para Common Mode Rejection Rate (relação da Rejeição de modo comum). Em teoria, ao aplicar o mesmo sinal nas duas entradas (v1 = v2), deveríamos ter como resultado em Vout uma saída nula, afinal, teríamos Vout = (v1-v2/2)A = (0/2)A = 0V.
Porém, na prática, ainda temos um pequeno sinal na saída Vout, fruto do ganho máximo para atenuar ou para fazer a rejeição, em dB ou V/V. A capacidade do AmpOp de rejeitar esses sinais é chamado de Rejeição de Modo Comum.
O modo para fazer a medição vai ser da seguinte forma:

``
CMRR = Avd/Avcm
``

Onde Avd é o ganho diferencial (especificado pelo fabricante) e Avcm é o ganho em modo comum. Portanto, para calcular em dB ou V/V, temos:

``
CMRR = 20*log(Avd/Avcm) dB
``

## 9. Utilizando o Amplificador Subtrator com ganho 1000V/V, demonstre o efeito da tensão de modo comum (Vcm), indicando:

#### a. o impacto na tensão de saída com relação a tolerância dos resistores no circuito;

Em teoria, tendo um ganho 1000V/V, podemos possuir um R1 como 1k e um R2 como 1M. Com uma tolerância de 5% em R1 e 5% em R2, temos:

```
R1 = 1k + 1% = 1010 Ohm ; 1k - 1% = 990 Ohm
R2 = 1M + 5% = 1050000 Ohm ; 1M - 5% = 950000 Ohm
```

Fazendo a relação do ganho (R2/R1) novamente temos:

```
G = 1050000/1010 = 1039V/V em +5%
G = 950000/990 = 960V/V em -5%
```

O que gera uma diferença de aproximadamente 40V/V no ganho do circuito. Como esse valor pode variar, o pico de diferença (maior com menor) fica 80V/V.

## 10. Faça um resumo explicando as limitações de tensão de entrada e saída de um AmpOp.

As limitações de entrada e saída de um AmpOp ocorrem da forma que a saída, idealmente, é no máximo o valor de alimentação positivo do AmpOp. Esse valor máximo é chamado de saturação do AmpOp. Na prática é um pouco diferente, a saturação do AmpOp é na ordem de 90% do valor da alimentação positiva. Por exemplo, um AmpOp que tem seu Vcc+ em 15V, pode apresentar em Vout, idealmente, 15V, porém na prática esse valor deve chegar em torno de 13,5V. Isso também vale para valores negativos.

AmpOp rail-to-rail é um amplificador operacional onde é prometido que a saturação ocorra somente no limite do valor da alimentação, tanto positiva quanto negativa. Existem ampops rail-to-rail de entrada, saída, e ambos.

## 11. O que é tensão de offset? Como calcular o efeito resultante na tensão de saída de um amplificador inversor?

Tensão de offset é uma peculiaridade que ocorre na prática com amplificadores operacionais, onde acontece uma pequena diferença entre as tensões dentro do amplificador, gerando um Vout diferente do calculado de forma ideal.
Utilizando o circuito em malha aberta da figura abaixo, temos em teoria que Vout será 0V. porém, utilizando o ampop modelo LM741, que possui um Vio (input offset) de 1mV, e um ganho em malha aberta de 200k V/V, o ampop irá saturar (1mv * 200k = 200V).

![ampop_offset](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2002/Exemplos/ampop_offset.png)

Em um AmpOp inversor, temos o seguinte circuito:

![ampop_inversor](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2002/Exemplos/ampop_inversor.png)

De acordo com a teoria, temos as equações:

```
G ≡ Vout/vin
Vout/vin = -R2/R1
Vout/1 = -10k/1k
Vout = -10V
```
Porém, utilizando novamente o LM741, e tendo um Vio de 1mV, temos um Vout que varia entre -9,99V e -10,01V.

## 12. Como minimizar o efeito da tensão de offset?

É possível minimizar o efeito fazendo os seguintes passos:
- Balanceando as duas entradas em termos de corrente contínua (Alguns AmpOps possuem bornes para o ajuste de offset);
- Mantendo a temperatura do ambiente constante;
- Utilizando uma fonte de alimentação estabilizada.

## 13. O que é a variação da tensão de offset pela temperatura?

A variação da tensão de offset pela temperatura ocorre quando há uma variação térmica no ambiente, que acaba acentuando as características elétricas como um todo do amplificador. Idealmente um ampop não apresenta sensibilidade a temperatura.
Nos datasheets, o termo utilizado é geralmente input offset voltage drift, e é medido em V/ºC. Na figura abaixo podemos ver o datasheet do modelo LM741A, com a parte referente a temperatura em vermelho.

![lm741a](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2002/Exemplos/lm741a.png)

## 14. O que são as correntes de polarização (Ibias) de AmpOp?

As correntes de polarização são correntes que passam pelas entradas de tensão do ampop, geralmente na ordem de nA. Idealmente, a resistência de entrada do ampop deveria ser infinita, implicando em uma corrente sendo igual a 0A, porém na prática isso não ocorre.
Em um circuito com realimentação, dependendo da ordem do resistor que for utilizado, podemos ter corrente desde a ordem de mA até nA. Quanto maior o valor do resistor da realimentação, mais evidente fica a corrente de polarização do ampop.

Portanto, para minimizar o efeito das correntes de polarização, pode ser utilizado resistores de menor resistência, para consequentemente deixar a corrente de polarização menos evidente. Mas, em alguns casos, é necessário utilizar uma corrente baixa (a maioria dos AmpOps funciona com correntes de até 20mA), e um resistor de ordem muito alta não irá mais funcionar.

De qualquer forma, o que mais vale a pena fazer é realmente verificar a Ibias do AmpOp e escolher um que tenha em menor ordem, a fim de funcionar o circuito em específico.
