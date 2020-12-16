# Atividade 2

## Resumo sobre Amplificadores Operacionais

### Questão 1: O que é _Amp Op_?

O Amplificador Operacional é um circuito integrado amplificador e é responsável por ampliar sinais fracos na faixa de microvolt (uV) ou milivolt (mV). Sendo assim, ele é projetado para operar como um medidor da diferença entre os sinais de tensão aplicados aos seus dois terminais de entrada.

### Questão 2: Mostre os símbolos e as características do _Amp Op_ IDEAL?

O símbolo mais básico do Amplificador Operacional apresenta três terminais sendo, dois terminais de entrada, entrada inversora (terminal 1) e entrada não inversora (terminal 2) e um terminal de saída (3).

![Figura_1](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_2/Imagens/Figura%201.JPG)

Porém, os amplificadores devem ser alimentados com uma fonte cc para operar. Quase todos os circuitos integrados devem ser alimentados com uma fonte cc simétrica, conforme podemos observar na figura 2.

![Figura_2](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_2/Imagens/Figura%202.JPG)

Em se tratando das características, quando estudamos um Amp Op ideal sempre supomos que não existe corrente nos terminais 1 e 2, em outras palavras a impedância de entrada do Amp Op ideal é supostamente infinita. Já em relação ao terminal 3, supõe-se que ele seja um dos terminais de uma fonte de tensão, ou seja, a tensão entre este terminal e o terra será sempre igual A*(V2 – V1), o que caracteriza que a impedância de saída do Amp Op ideal é supostamente igual a zero.  

V1 – Tensão entre o terminal 1 e o terra;
V2 – Tensão entre o terminal 2 e o terra;

Além disso, como já visto, o Amp Op opera com a diferença entre as tensões de entrada, portanto, qualquer sinal comum a ambas as entradas é ignorado, ou seja, se V1=V2 então a saída ideal será 0, a esta característica chamamos de rejeição de modo comum infinita.

Outras características do Amp Op são: ganho de malha aberta A infinito e largura de faixa e resposta em frequência infinita.

### Questão 3: O que significa Malha Aberta e Malha Fechada?

Malha aberta nada mais é do que um Amp Op sem realimentação da saída para a entrada, enquanto que, na malha fechada o Amp Op apresenta realimentação negativa da saída para a entrada.

### Questão 4: Exemplifique como resolver e calcular circuitos com AmpOps em Malha Fechada.

### Questão 5: Descreva as principais características das topologias:

#### Seguidor de Tensão (Buffer);

O Seguidor de tensão é obtido através de um Amp Op com configuração não inversora com R1 = oo e R2 = 0, para obtermos o amplificador de ganho unitário. Este circuito é chamado de seguidor de tensão visto que a saída “segue” a entrada.

#### Amplificador Inversor;

A configuração Inversora consiste em um Amp Op e dois resistores R1 e R2. O resistor 2 é conectado entre o terminal de saída (3) e o terminal da entrada inversora (1), o que caracteriza uma realimentação negativa. Podemos observar que R2 fecha a malha em torno do Amplificador. Outra característica importante desta configuração é que o terminal 2 é aterrado e um resistor R1 é conectado entre o terminal 1 e uma fonte de sinal de entrada com tensão V1.

#### Amplificador não inversor;

Nesta configuração, o sinal de entrada V1 é conectado diretamente ao terminal de entrada positivo do Amp Op e o Resistor 1 é conectado ao terra.

#### Amplificador Somador Inversor;
#### Amplificador Somador Não Inversor;
#### Subtrator;
#### Amplificador de Instrumentação;

### Questão 6:Explique o efeito do ganho em MALHA ABERTA FINITO, para as topologias Amplificador Inversor e Amplificador não inversor. 

#### Exemplifique com circuitos com ganhos em malha fechada elevado (Ex. 1000V/V e -1000V/V) e com ganhos menores (Ex. 10V/V e -10V/V ), faça a comparação com erros percentuais e utilize uma variação de ganho em malha aberta entre 120dB e 20dB.

### Questão 7:	Explique o que é a tensão de modo comum (VCM) e quais os efeitos desta tensão nas topologias estudadas.

### Questão 8: O que é CMRR?

### Questão 9: Utilizando o Amplificador Subtrator com ganho 1000V/V, demonstre o efeito da tensão de modo comum (VCM), indicando:
#### O impacto na tensão de saída com relação a tolerância dos resistores no circuito; 
#### Qual erro na tensão de saída com relação CMRR do AmpOp. 

### Questão 10: Faça um resumo explicando as limitações de tensão de entrada e saída de um AmpOp. De exemplos, utiliza-se valores de datasheet. 
#### Defina o que é um AmpOp Rail-to-rail.

### Questão 11: O que é tensão de offset? Como calcular o efeito resultante na tensão de saída de um amplificador inversor?

### Questão 12: Como minimizar o efeito da tensão de offset?

### Questão 13: O que é a variação da tensão de offset pela temperatura?
#### Como verificar esse parâmetro no datasheet?

### Questão 14: O que são as correntes de polarização (Ibias) de AmpOp?
#### Como minimizar o efeito destas correntes? Descreva as aproximações e os possíveis circuitos para mitigar o problema.
#### Descreva a corrente de offset na polarização dos AmpOp.
