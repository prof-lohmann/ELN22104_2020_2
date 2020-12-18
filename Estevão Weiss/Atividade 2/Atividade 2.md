## Resumos sobre Amplificadores Operacionais

* O que é um AmpOp?

AmpOp (amplificador operacional) é um circuito integrado (CI) capaz de amplificar sinais com um ganho muito elevado. 

* AmpOp Ideal e suas características

------COLOCAR IMAGEM-----------

As características de um AmpOp Ideal são: Impedância de entrada infinita, impedância de saída nula e ganho infinito. Essas situações não são encotradas na prática e são utilizadas para fins didáticos.

* Sistemas em Malha Aberta e Malha Fechada

Os sistemas em malha aberta independem do sinal de saída, não são realimentados. Já os sistemas em malha fechada recebem informações sobre a saída (realimentação) e, assim, são mais eficazes.

* Como calcular circuitos com AmpOp em Malha Fechada?

O método mais utilizado nos cálculos dos circuitos com AmpOp em malha fechada é a Primeira Lei de Kirchhoff (Lei dos Nós), onde as correntes nos terminais de entrada são utilizadas para obter os parâmetros.

* Topologias principais e suas características

Seguidor de Tensão (Buffer)
----------IMAGEM BRUFFER---------

Nesta topologia a entrada é realimentada diretamente com o sinal de saída do ampop e é conhecido por seu ganho unitário, sendo a saída igual a entrada e vice e versa.

Amplificador Inversor
----------IMAGEM INVERSOR--------

O amOp inversor tem como sua característica principal a inversão do sinal de entrada junto com um ganho, descrito na fórmula da imagem acima.

Amplificador Não Inversor
----------IMAGEM NÃO INVERSOR---------

O ampOp não inversor, como o nome já diz, não inverte o sinal de entrada e tem seu ganho descrito pela formúla da imagem acima.

Amplificador Somador Inversor
----------IMAGEM DO SOMADOR INVERSOR---------

A topologia do somador inversor tem como sua principal característica a soma de dois ou mais sinais de entrada, junto com a inversão desses sinais e o ganho descrito na fórmula da imagem acima.

Amplificador Somador Não Inversor 
----------SOMADOR NÃO INVERSOR------------

A topologia do somador não inversor tem como sua principal característica a soma de dois ou mais sinais de entrada junto com o ganho descrito na fórmula da imagem acima.

Amplificador Substrator
---------Subtrator---------

Como o nome já diz, essa topologia substrai sinais de entrada de acordo com a fórmula descrita na imagem acima.

Amplificador de Instrumentação
---------- Amplificador de instrumentação--------------

Esta configuração é uma junção de topologias, nela temos um amplificador subtrator em conjunto com dois amplificadores inversores. O controle do ganho é feito através da variação da resistência Rg, como pode ser visto na fórmula descrita na imagem.

* Questão 6!!!!!!!!!!!!!!!!!!!!
Até agora todas as nossas análises foram feitas através de modelos de ampOps ideias, com suas características ideais, que fazem com que o ganho do amplificador tenda ao infinito. Como na prática não existem modelos ideais, os ampOps reais têm suas NÃO-IDEALIDADES, obviamente não se consegue ganhos infinitos e a limitação de ganho de um ampOp real fica na ordem de 10^5 a 10^6.

* Tensão de Modo Comum (Vcm)

Quando tratamos de amplificadores de diferenças utilizamos a fórmula Vo=Ad*Vd + Acm*Vcm, onde Ad e Vd são, respectivamente, o ganho e a entrada diferencial do ampOp (a parcela útil que será amplificada) e Acm e Vcm são o ganho de modo comum (idealmente nulo) e a entrada de modo comum, sendo as duas últimas as parcelas rejeitadas (não amplificadas) pelo ampOp.

* Razão de Rejeição de Modo Comum (CMRR)










