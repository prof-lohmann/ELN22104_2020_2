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

>

### Correntes de polarização (Ibias) de um AmpOp

>

#### Minimizar o efeito destas correntes

>

### O que é CMRR?

>

### As limitações de tensão de entrada e saída de um AmpOp

>

#### Exemplo:

>

### O que é um AmpOp Rail-to-rail?

>

### Tensão de offset em Ampops

> 

### Corrente de offset na polarização dos AmpOp

>

#### Calculo do efeito resultante na tensão de saída de um amplificador inversor

>

#### Como minimizar efeitos da tensão de offset em ampops

>

#### Variação da tensão de offset pela temperatura

> 

