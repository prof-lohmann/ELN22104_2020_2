# Atividade 2 
## Resumo sobre Amplificadores Operacionais

### O que é o AmpOp?

> O Amplificador operacional é um circuito integrado, capaz de amplificar um sinal de entrada e realizar operações matemáticas.
> Sua principal característica é possuir duas entradas e uma saída que será resultante a partir da operacao realizada em sua configuracao.

### Simbologia e as características do AmpOp

> O diagrama abaixo mostra um típico Amplificador Operacional.
>
>![Opamppinouts](https://user-images.githubusercontent.com/12564754/102247973-6bac1180-3edf-11eb-9dbc-ea5f073403fe.png)
> 
> Os seus terminais são:
>
> * V+: entrada não-inversora
> * V−: entrada inversora
> * Vout: saída
> * VS+: alimentação positiva
> * VS−: alimentação negativa
>
> As caracteristicas ideais de um AmpOp sao:
>
> * Impedancia de entrada infinita;
> * Impedancia de saida nula;
> * Ganho de tensao infinito;
> * Resposta em frequencia infinita;
> * Insensibilidade a temperatura.
> 
> Fisicamente sua estrutura em circuito integrado é organizada em pares ou quartetos. Como exemplo abaixo temos um LM358.
>
> ![Capture](https://user-images.githubusercontent.com/12564754/102249035-a95d6a00-3ee0-11eb-9228-acd0030f68d1.PNG) 
>
> A entrada positiva não-inversora produz uma saída que está em fase com o sinal aplicado, enquanto a entrada inversora resulta numa saída com polaridade oposta.

### AmpOp em Malha Aberta e Malha Fechada

> Malha aberta: Uma configuração sem realimentação do retorno da saída do amp-op à sua entrada. O ganho do amp-op de malha aberta geralmente excede 10.000.
> Exemplo: 
>
> ![malha_aberta](https://user-images.githubusercontent.com/12564754/102251474-9bf5af00-3ee3-11eb-935a-546c97a68ea3.PNG)
>
> Malha fechada: Uma configuração que tem um caminho de realimentação da saída do ampOp à sua entrada negativa ou positiva.
> Exemplo:
>
> ![malha_fechada](https://user-images.githubusercontent.com/12564754/102251814-10305280-3ee4-11eb-9ac6-4adf18d3d9e2.PNG)
>

#### Calcular circuitos de AmpOps em malha aberta e fechada

>

#### Topologias para Ampops:

> Abaixo temos algumas opcoes de  configuracao de circuitos utilizando  os Amplificadores Operacionais.

##### Seguidor de Tensão (Buffer):

> O Seguidor de tensao ou seguidor unitario atua como um isolador (buffer). Este circuito fornece um ganho unitario, sem inversao  de polaridade de fase  mantendo a saida com a mesma integridade do sinal de entrada. 
> Abaixo temos uma ilustracao com o seguidor unitario:
>
> ![seguidor_unitario](https://user-images.githubusercontent.com/12564754/102254617-a1ed8f00-3ee7-11eb-9a4e-acc5080b18a2.PNG)
>
> Tambem a casos em que o seguidor de tensao possui resistores em serie colocada no terminal nao-inversor para alterar o valor do ganho do ampOp. 
> Outra utilidade seria para o casamento de impedancias de saidado sistema.
> Abaixo temos uma ilustracao com o seguidor com resistencias:
>
> ![seguidor tensao](https://user-images.githubusercontent.com/12564754/102647610-c5614580-4144-11eb-98d5-6ee4af73ce14.PNG)
>

##### Amplificador Inversor:

> 
> Este amplificador é chamado de inversor porque além de amplificar o sinal de entrada, o sinal de saída possui polaridade invertida, ou seja, valores positivos na entrada se tornam valores negativos na saída e vice-versa.
> Exemplo de Amplificador Inversor:
>
> ![inversor](https://user-images.githubusercontent.com/12564754/102647951-69e38780-4145-11eb-96f3-9898952b6e93.PNG)


##### Amplificador Não Inversor:

> 
> Este amplificador é chamado de nao-inversor porque além de amplificar o sinal de entrada, o sinal de saída nao possui a polaridade invertida
> Exemplo de Amplificador Nao-Inversor:
>
> ![nao inversor](https://user-images.githubusercontent.com/12564754/102648330-132a7d80-4146-11eb-9368-bf43135b1faf.PNG)
>

##### Amplificador Somador Inversor:

> O amplificador somador inversor realiza o somatórios das tensões que entram no terminal inversor, resultando na saida o resultado desta operacao.
> Exemplo de Amplificador Somador Inversor: 
>
>![somador_inversor](https://user-images.githubusercontent.com/12564754/102648755-d9a64200-4146-11eb-9924-81b4634fb6e3.PNG)

##### Amplificador Somador Não Inversor:

> O amplificador somador Nao-inversor realiza o somatórios das tensões que entram no nao-terminal inversor, resultando na saida o resultado desta operacao.
> Exemplo de Amplificador Somador Inversor: 
>
> ![somador-naoinver](https://user-images.githubusercontent.com/12564754/102648998-3dc90600-4147-11eb-8479-bab8e12d9142.PNG)

##### Subtrator:

>

##### Amplificador de Instrumentação:

>

### Efeito do ganho em malha aberta finito para as topologias Amplificador Inversor e Amplificador não inversor

>

#### Exemplo com circuitos com ganhos em malha fechada elevado:

>

### Tensão de modo comum (VCM)

> É a diferença potencial entre os sinais de sua entrada, saída inversora e não inversora. Em alguns circuitos pode ocasionar problemas, faixa de tensão do modo comum e a taxa de rejeição do modo comum (CMRR) são descritas para que possíveis erros de medidas não ocorram. A faixa de tensão do modo comum é definida como a máxima variação de tensão permitida em cada entrada. Caso não esteja dentro da faixa não apenas pode causar um erro de medição, mas também em possível dano aos componentes circuito.


### Correntes de polarização (Ibias) de um AmpOp

> Para o AmpOp operar, deve ter uma corrente para fazer o funcionamento dos componentes internos do mesmo, de forma a possuir uma corrente medida com o AmpOp em repouso.
> Correntes de polarização de entrada significa fontes de correntes cc ligadas ao AmpOp. O fabricantes especifica o valor média de Ibias, bem como sua diferença, corrente de
> offset entre outras especificacoes.

#### Minimizar o efeito destas correntes

> Adicionar um resistor em série com o terminal de entrada inversora. O resitor em série deve ser igual à associação em paralelo de R1 e R2. Outra forma de minimizar o efeito caso o resistor não seja suficiente é procurando outro AmpOp com corrente de offset menor.

### O que é CMRR?

> CMRR significa rejeição de modo comum, é utilizada para medir a eficácia de um amplificador diferencial, geralmente medida pelo grau de sua rejeição a sinais de modo comum.
> Teoricamente esse diferencial deveria ser zero, mas na prática ainda é visto um sinal. Valores altos de CMRR podem ocasionar em um erro grande na medida no sinal de saída.
> A rejeição do modo comum pode ser medido desta forma:
>```
> CMRR = 20log(|ad|/|acm|)
>```

### As limitações de tensão de entrada e saída de um AmpOp

> Existe um limite de tensão na entrada de acordo com a alimentação do ampop. Por exemplo temos o LM324, de acordo com seu datasheet, os limites de tensão de alimentação vão de 3 a 26V, mas para tensão de entrada vai de 0 a -2V. Caso alimente um AmpOp com ±15V, sua saída vai ser saturada em ±13V.


### O que é um AmpOp Rail-to-rail?

> Um amplificador preciso cuja tensão na saída tende alcançar o mesmo nível que as tensões de alimentação do AmpOp. A maioria dos amplificadores possui uma saída limitada entre a alimentação negativa e a positiva a partir de 0,2V.

### Tensão de offset em Ampops

>  É um desequilíbrio nas entradas do AmpOp, devido a altos valores de ganho. Nos circuitos é visto como uma fonte de tensão na entrada não inversora do circuito.
> Para calcular o efeito sobre a tensão de saída pelo teorema de superposição, anulando as fontes uma por uma e vendo seus efeitos no sinal de saída, como no exemplo a seguir:
> 
> Este valores de offset sao fornecidos em datasheets dos amplificadores operacionais.

### Corrente de offset na polarização dos AmpOp

> É definida como a diferença entre as correntes de polarização de entrada do ampop, seu calculo é dado por:
> ```
> Ios=|Ib1-Ib2|
> ```

#### Calculo do efeito resultante na tensão de saída de um amplificador inversor

> Para calcular o efeito sobre a tensão de saída pelo teorema de superposição, anulando as fontes uma por uma e vendo seus efeitos no sinal de saída.

#### Como minimizar efeitos da tensão de offset em ampops

> É possível acoplar um capacitor na entrada inversora, mas somente em aplicações que não exijam uma amplificação de sinais cc ou frequências muitos baixas ou procurando outro AmpOp com tensão de offset menor.

#### Variação da tensão de offset pela temperatura

> As variacoes termicas podem provicar alteracoes acentuadas nas caracteriscas eletricasde um amplificados. Este fenomeno é chamado de DRIFT nos datasheets dos ampops. A variacao da corrente é representada por ΔI/ΔT e seu valor é fornecido em nA/ºC. A variacao da tensao é representada por ΔV/ΔT e seu valor fornecido é em µV/ºC.

