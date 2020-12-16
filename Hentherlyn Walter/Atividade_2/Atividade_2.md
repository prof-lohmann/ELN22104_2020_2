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

