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

>

##### Seguidor de Tensão (Buffer):

>

##### Amplificador Inversor:


>

##### Amplificador Não Inversor:

>

##### Amplificador Somador Inversor:

>

##### Amplificador Somador Não Inversor:

>

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

