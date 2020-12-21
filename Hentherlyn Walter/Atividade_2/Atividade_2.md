# Atividade 2

## Resumo sobre Amplificadores Operacionais

### O que é _Amp Op_?

O Amplificador Operacional é um circuito integrado amplificador e é responsável por ampliar sinais fracos na faixa de microvolt (uV) ou milivolt (mV). Sendo assim, ele é projetado para operar como um medidor da diferença entre os sinais de tensão aplicados aos seus dois terminais de entrada.

### Mostre os símbolos e as características do _Amp Op_ IDEAL?

O símbolo mais básico do Amplificador Operacional apresenta três terminais sendo, dois terminais de entrada, entrada inversora (terminal 1) e entrada não inversora (terminal 2) e um terminal de saída (3).

![Figura_1](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_2/Imagens/Figura%201.JPG)

_Figura 1._

Porém, os amplificadores devem ser alimentados com uma fonte cc para operar. Quase todos os circuitos integrados devem ser alimentados com uma fonte cc simétrica, conforme podemos observar na figura 2.

![Figura_2](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_2/Imagens/Figura%202.JPG)

_Figura 2._

Em se tratando das características, quando estudamos um Amp Op ideal sempre supomos que não existe corrente nos terminais 1 e 2, em outras palavras a impedância de entrada do Amp Op ideal é supostamente infinita. Já em relação ao terminal 3, supõe-se que ele seja um dos terminais de uma fonte de tensão, ou seja, a tensão entre este terminal e o terra será sempre igual A*(V2 – V1), o que caracteriza que a impedância de saída do Amp Op ideal é supostamente igual a zero.  

V1 – Tensão entre o terminal 1 e o terra;

V2 – Tensão entre o terminal 2 e o terra;

Além disso, como já visto, o Amp Op opera com a diferença entre as tensões de entrada, portanto, qualquer sinal comum a ambas as entradas é ignorado, ou seja, se V1=V2 então a saída ideal será 0, a esta característica chamamos de rejeição de modo comum infinita.

Outras características do Amp Op são: ganho de malha aberta A infinito e largura de faixa e resposta em frequência infinita.

### O que significa Malha Aberta e Malha Fechada?

Malha aberta nada mais é do que um Amp Op sem realimentação da saída para a entrada, enquanto que, na malha fechada o Amp Op apresenta realimentação negativa da saída para a entrada.

### Exemplifique como resolver e calcular circuitos com AmpOps em Malha Fechada.

![Figura_3](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_2/Imagens/C%C3%A1lculo%20do%20Inversor.jpeg)

_Figura 3._

### Descreva as principais características das topologias:

#### I) Seguidor de Tensão (Buffer);

![Figura_4](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_2/Imagens/Buffer.JPG)

_Figura 4._

O Seguidor de tensão é obtido através de um Amp Op com configuração não inversora com R1 = oo e R2 = 0, para obtermos o amplificador de ganho unitário. Este circuito é chamado de seguidor de tensão visto que a saída “segue” a entrada.

#### II) Amplificador Inversor;

![Figura_5](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_2/Imagens/Inversor.JPG)

_Figura 5._

A configuração Inversora consiste em um Amp Op e dois resistores R1 e R2. O resistor 2 é conectado entre o terminal de saída (3) e o terminal da entrada inversora (1), o que caracteriza uma realimentação negativa. Podemos observar que R2 fecha a malha em torno do Amplificador. Outra característica importante desta configuração é que o terminal 2 é aterrado e um resistor R1 é conectado entre o terminal 1 e uma fonte de sinal de entrada com tensão V1.

#### III) Amplificador não inversor;

![Figura_6](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_2/Imagens/N%C3%A3o%20inversor.JPG)

_Figura 6._

Nesta configuração, o sinal de entrada V1 é conectado diretamente ao terminal de entrada positivo do Amp Op e o Resistor 1 é conectado ao terra.

#### IV) Amplificador Somador Inversor;

![Figura_7](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_2/Imagens/Somador%20inversor.JPG)

_Figura 7._

Esta configuração, conforme a figura abaixo, é um circuito responsável por somar algebricamente as n tensões, cada uma multiplicada por um ganho constante, ou seja, cada entrada gera um ganho à saída. É importante citar que nesta modelo, as n entradas são conectadas os terminal 1, ou entrada inversora.

#### V) Amplificador Somador Não Inversor;

![Figura_8](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_2/Imagens/Somador%20nao%20inversor.JPG)

_Figura 8._

O circuito do somador não inversor assemelha-se muito ao somador inversor, porém, neste caso as n entradas são conectadas ao terminal 2, ou entrada não inversora, por isso a tensão de saída não sofre inversão de sinal.

#### VI) Subtrator;

![Figura_9](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_2/Imagens/Subtrator.JPG)

_Figura 9._

Esta configuração permite que tenhamos uma tensão de saída igual a diferença entre as duas entradas multiplicada por um ganho.

#### VII) Amplificador de Instrumentação;

![Figura_10](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_2/Imagens/Amplificador%20de%20instrumenta%C3%A7%C3%A3o-.JPG)

_Figura 10._

O amplificador de instrumentação, representado na figura abaixo, é composto por dois amplificadores não inversores e um amplificador diferença. Desta forma, a resistência de entrada vista por cada uma das fontes é infinita e o ganho de tensão é dado pelo produto de dois cocientes entre as resistências.

### Explique o efeito do ganho em MALHA ABERTA FINITO, para as topologias Amplificador Inversor e Amplificador não inversor. 

Idealmente o ganho em malha aberta tendem ao infinito, porém, na prática, os ampops apresentam características não ideais bem como, tensão de offset e corrente de polarização o que não possibilita ganhos infinitos.

![Figura_11](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_2/Imagens/C%C3%A1lculo%20do%20Inversor.jpeg)

_Figura 11 - Cáculo de Vo para o amplificador inversor._

![Figura_12](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_2/Imagens/C%C3%A1lculo%20do%20n%C3%A3o%20inversor.jpeg)

_Figura 12 - Cáculo de Vo para o amplificador não inversor._

### Explique o que é a tensão de modo comum (VCM) e quais os efeitos desta tensão nas topologias estudadas.

Na forma ideal dos AmpOps, a tensão de modo comum, ou VCM, é nula, entretanto, na prática ela se caracteriza como a média dos valores aplicados às entradas inversora e não inversora, tendo como efeito uma alteração na tensão de saída do amplificador.

### O que é CMRR?

O CMRR é a relação de rejeição de modo comum.  De forma ideal, quando dois sinais de mesma frequência, amplitude e fase, são aplicados às entradas de um Amp Op, os mesmos devem se cancelar e nenhuma saída deve aparecer. Na prática, esta saída não é nula e é especificada em relação ao ganho máximo. A capacidade do Amplificador Operacional em rejeitar este sinal é a rejeição de modo comum, sendo medida de decibéis (dB).

### Faça um resumo explicando as limitações de tensão de entrada e saída de um AmpOp. De exemplos, utiliza-se valores de datasheet. 

Os Amplificadores Operacionais apresentam limitações de tensão de entrada e de saída pois, na prática, eles apresentam características não ideais, o que acaba limitando sua área de funcionamento.

![Figura_13](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_2/Imagens/Lm741.JPG)

_Figura 13._

![Figura_14](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_2/Imagens/Datasheet.JPG)

_Figura 14._

Disponível em: https://www.ti.com/lit/ds/symlink/lm741.pdf

#### I) Defina o que é um AmpOp Rail-to-rail.

O AmpOp Rail-to-Rail é um modelo de amplificador com alimentação simétrica que têm como característica principal a expansão da área de funcionamento, ou seja, foram criados para aumentar a variação das tensões que podem ser aplicadas na entrada e na saída.

### O que é tensão de offset? Como calcular o efeito resultante na tensão de saída de um amplificador inversor?

A tensão em offset nada mais é do que a tensão que aparece na saída do ampop, quando ambas as entradas são 0. Esta tensão pode interferir direta e negativamente na utilização do amplificador em aplicações de instrumentação. Uma forma de calcular a tensão de saída, neste caso, é aterrar as duas entradas (inversora e não inversora) e depois fazer a análise.

### Como minimizar o efeito da tensão de offset?

Para minimizar o efeito da tensão de offset é necessário conectar à entrada do ampop uma fonte de tensão de mesmo valor, porém com polaridade oposta. Desta forma, idealmente uma iria anular a outra, entretanto, na prática existem outros efeitos geram alterações, como a variação da temperatura e as correntes indesejadas.

### O que é a variação da tensão de offset pela temperatura?

Idealmente, um amp op não sofre alteração no seu comportamento devido à variação da temperatura, porém na prática, a mudança de temperatura pode provocar muitas alerações no comportamento de um Amplificador operacional. A este efeito damos o nome de DRIFT.

#### I) Como verificar esse parâmetro no datasheet?

No manual dos fabricantes podemos encontrar informações sobre o comportamento da tensão e da corrente conforme a variação de temperatura. Normalmente, a variação de corrente é representada por ΔI/Δt e seu valor é dado em nA/°C e a variação de tensão é representada por ΔV/Δt e seu valor é fornecido em uV/°C.

### O que são as correntes de polarização (Ibias) de AmpOp?

As correntes de polarização são correntes indesejadas que entram ou saem da entrada do AmpOp devido às correntes de base ou de fuga dos transistores.

#### I) Como minimizar o efeito destas correntes? Descreva as aproximações e os possíveis circuitos para mitigar o problema.

Da mesma forma que a tensão de offset, é possível adicionar uma fonte de corrente com a mesma amplitude, frequência e fase da corrente de polarização, porém de sentido oposto, com o objetivo de minimizar o efeito indesejado. É possível que a soma da corrente de polarização com a fonte de corrente não resulte em 0, pois estamos tratando de AmpOps não ideias, desta forma, podemos adicionar um resistor ao ciruito de forma a mitigar com o problema.

#### II) Descreva a corrente de offset na polarização dos AmpOp.

Como já dito anteriormente, o amplificador operacional apresenta impedância de entrada infinita, já os ampops não ideais apresentam correntes de polarização nas suas entradas. Como na prática a simetria de entrada não é perfeita, as duas correntes de polarização são diferentes. A corrente de offset é dada pelo módulo da diferença entre as duas correntes de polarização.
