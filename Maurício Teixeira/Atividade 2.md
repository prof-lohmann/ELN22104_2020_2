# 01. O que é um AmpOp?
  Amplificadores operacionais são circuitos integrados (CI) que possuem a capacidade de amplificar o sinal que recebem em sua entrada e também de realizar algumas funções matemáticas, como soma, subtração, multiplicação, derivação e integração. Amplificadores operacionais possuem dois terminais de entrada, denominados como entrada inversora (Sinal negativo) e entrada não inversora (Sinal positivo). Além deles, possui dois terminais de entrada de alimentação, positiva (Vcc+) e negativa (Vcc-). E por fim temos a saída Vout.
![Ampop](https://github.com/mauriciots96/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Maur%C3%ADcio%20Teixeira/Ampop.png)
# 02. Mostre os símbolos e as características do AmpOp IDEAL.
  Um AmpOp ideal pode ser representado pela seguinte imagem:
  ![Ampop ideal](https://github.com/mauriciots96/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Maur%C3%ADcio%20Teixeira/Ampop%20ideal.png)
  AmpOps ideais possuem uma impedância de entrada infinita, levando os valores de uama possível corrente de entrada a zero, para que a corrente no terminal inversor (v1) e não inversor (v2) seja igual a zero. No terminal de saída 3, temos uma fonte de tensão ideal representada pela expressão (v2-v1). Quando temos v1=v2 em um AmpOp ideal, teremos uma condição especial chamada de rejeição de modo comum, onde temos saída igual a zero. Além disso, o AmpOp ideal deve ter um ganho "A" constante, para amplificar sinal de qualquer frequência, sempre com o mesmo ganho, e esse ganho "A" deve tender ao infinito. Possui também ganho de modo comum igual a zero, insensibilidade à temperatura, resposta de frequência infinita e impedância de saída igual a zero.

# 03. O que significa Malha Aberta e Malha Fechada?
  Quando o AmpOp não possui realimentação, seja pelo terminal não inversor, ou inversor ele é denominado como Malha aberta. Nesse tipo de configuração, o amplificador mostra em sua saída um sinal resultante de uma amplificação da diferença entre os potenciais de entrada com um valor alto e impreciso. Malha fechada é justamente o contrário, quando o AmpOp recebe realimentação, que geralmente acontece no terminal inversor. Nesse segundo tipo de configuração, trocamos o ganho pela precisão, tendo um ganho menor porém estável e preciso.

# 04. Exemplifique como resolver e calcular circuitos com AmpOps em Malha Fechada.
  Utilizaremos o exemplo presente no capítulo 2 do livro do Sedra Smith - Microeletrônica. 
![Exemplo 2.4 do livro](https://github.com/mauriciots96/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Maur%C3%ADcio%20Teixeira/Exemplo%202.4%20do%20livro.jpg)
A figura acima representa a configuração do AmpOp na figura 2.4 (Capítulo 2). 

Podemos constatar que esse circuito está em Malha Fechada devido ao posicionamento do resistor R2 que gera a realimentação entre a entrada inversora e a saída.
O ganho "G" é determinado pela expressão:
G ≡ Vout/v1
Por definição, chegamos na expressão de ganho em malha fechada:
Vout/v1 = -R2/R1
A partir das expressões acima, temos a razão entre R2 e R1, e podemos constatar uma inversão no sinal de entrada devido ao sinal negativo em -R2/R1. Posteriormente podemos calcular a corrente i1 da seguinte forma:
i1 = v1/R1
O ganho não é infinito, portanto, temos a tensão de entrada como Vout/A. Como temos o terminal de entrada positivo aterrado, a tensão no terminal inversor será -Vout/A. Desta forma, a corrente i1 pode ser obtida pela expressão:
i1 = [v1 - (-Vout/A)]/R1 = (v1 + Vout/A)/R1
E uma tensão de saída Vout:
G ≡ Vout/v1 = (-R2/R1)/[1+(1+R2/R1)/A]

# 05. Descreva as principais características das topologias:
### a. Seguidor de tensão (Buffer);
![seguidor de tensão](https://github.com/mauriciots96/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Maur%C3%ADcio%20Teixeira/Seguidor%20de%20tens%C3%A3o.png)
Um seguidor de tensão nada mais é que um circuito amplificador operacional que não apresenta ganho de. Isso significa que o Ampop não fornece nenhuma amplificação ou atenuação ao sinal. Um circuito de amplificador operacional é um circuito com uma impedância de entrada muito alta, esta alta impedância de entrada é a razão pela qual os seguidores de tensão são usados. A alta impedância faz com que seu uso em circuitos divisores de tensão seja muito importante quando colocados em série com cargas de baixa impedância que não receberiam o nível de tensão adequeda para funcionar. Eles atuam como amortecedores isolantes, isolando um circuito para que a potência do circuito seja muito pouco alterada.

### b. Amplificador inversor;
![Amplificador inversor](https://github.com/mauriciots96/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Maur%C3%ADcio%20Teixeira/amplificador-inversor-com-ampop.png)
O amplificador inversor possui dois resistores de realimentação e possui como característica a amplificação do sinal de entrada e a inversão da polaridade do sinal de saída.

### c. Amplificador não inversor;
![Amplificador não inversor](https://github.com/mauriciots96/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Maur%C3%ADcio%20Teixeira/amplificador-n%C3%A3o-inversor-com-ampop.png)
Em um AmpOp não inversor, temos dois resistores de realimentação, assim como no amplificador inversor, porém, teremos um sinal de saída de mesma polaridade do sinal de entrada, caso seja uma fonte senoidal, ou de mesmo sinal caso seja uma fonte comum. Porém, diferente do Buffer, ele terá um ganho ou atenuação no sinal, com seu ganho G.

### d. Amplificador Somador Inversor;
![Amplificador somador inversor](https://github.com/mauriciots96/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Maur%C3%ADcio%20Teixeira/amplificador-somador-inversor-com-ampop.png)
O amplificador somador inversor permite realizar a soma de dois ou mais sinais, basta apenas ligar os sinais adicionais a resistores de entrada que na saída teremos a soma ponderada dos sinais de entrada com polaridade inversa.

### e. Amplificador Somador Não Inversor;
Possui a mesma funcionalidade do somador inversor, com a diferença de que não inverte a polaridade do sinal de saída.

### f. Subtrator;
O amplificador subtrator ou diferencial, permite realizar a subtração (diferença) de dois sinais por meio da combinação do amplificador inversor com o amplificador não-inversor, onde uma das entradas é no terminal inversor e a saída correspondente possui polaridade invertida e a outra entrada é no terminal não-inversor e a saída correspondente mantém a polaridade.
![Subtrator](https://github.com/mauriciots96/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Maur%C3%ADcio%20Teixeira/amplificador-subtrator-com-ampop.png)

### g. Amplificador de instrumentação;
Os amplificadores de instrumentação surgem como grandes aliados conseguindo agregar características como elevado CMR, elevada impedância nas entradas, baixo offset e baixa corrente de bias. Em resumo, podemos dizer que agrega a maior quantidade possível das características mais desejadas pelos projetistas.
![Amlificador de instrumentação](https://github.com/mauriciots96/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Maur%C3%ADcio%20Teixeira/amplificador-de-instrumentacao-ina-ad8221.png)

# 6. Explique o efeito do ganho em Malha Aberta Finito para as topologias Amplificador Inversor e Amplificador Não Inversor.
### A. Exemplifique com circuitos com ganhos em malha fechada elevado (Ex. 1000V/V e -1000V/V) e com ganhos menores (Ex. 10V/V e -10V/V ), faça a comparação com erros percentuais e utilize uma variação de ganho em malha aberta entre 120dB e 20dB.
Como o ganho em malha aberta é finito, a tensão entre os terminais de entrada do ampop inversor será -Vout/A, resultando numa corrente de entrada inversora igual:
i1 = [v1 - (-Vout/A)]/R1 = (v1 + Vout/A)/R1
Dessa forma, temos que a tensão Vout é:
G ≡ Vout/v1 = (-R2/R1)/[1+(1+R2/R1)/A]
No circuito de um Ampop inversor ou não inversor, utilizaremos R1 = 1 e R2 = 1k. O cálculo de tensão de saída fica:
G = (-R2/R1)/[1+(1+R2/R1)/A]
G = -1000/(1002/1000) = -998V/V
E = |(|-998| - 1000)|/1000*100 = 0,2% de erro percentual
Para um ganho em malha fechada original (R1 = 1k ; R2 = 10k), temos:
G = -10/(12/1000)
G = -833,33 V/V
E = |(|-833,33| - 1000)|/1000*100 = 16,67% de erro percentual

# 7. Explique o que é a tensão de modo comum (Vcm) e quais os efeitos desta tensão nas topologias estudadas.
A tensão de modo comum (Vcm) é a média das tensões das entradas do AmpOp. Como não temos tensão no terminal não inversor, a tensão de modo comum é a metade da tensão de entrada, com exceção do AmpOp Subtrator e do de instrumentação. Com a tensão de modo comum nossa saída Vout seria dada pela seguinte expressão:
Vout = (v1 - v2)*A

Se os sinais de entrada forem iguais, a saída teoricamente seria sempre 0V, porém na prática, como não temos condições ideais, vamos sempre ter alguma saída diferente de 0.

# 8. O que é CMRR?
CMRR é a sigla em inglês para Common Mode Rejection Rate ou em português; Rejeição de modo comum. Ao aplicar sinais de mesma magnetude nas duas entradas, deveríamos ter como resultado em Vout um valor nulo. Mas o que se pode constatar na prática é que ainda temos um pequeno sinal na saída Vout, fruto do ganho para atenuar ou para fazer a rejeição, em dB ou V/V. Logo, a capacidade do AmpOp de rejeitar esses sinais é denominada de Rejeição de Modo Comum. 

# 9. Utilizando o Amplificador Subtrator com ganho 1000V/V, demonstre o efeito da tensão de modo comum (Vcm), indicando:
### a. o impacto na tensão de saída com relação a tolerância dos resistores no circuito;
### b. Qual erro na tensão de saída com relação CMRR do AmpOp.
### c. Dica de exemplos com valores diferentes de tensão de modo comum (VCM) . Faça
o mesmo circuito com resistores com tolerâncias bem distintas, ex. 1% e 5%.
Em teoria, tendo um ganho 1000V/V, podemos possuir um R1 como 1 e um R2 como 1k. Com uma tolerância de 5% em R1 e 5% em R2, temos:
R1 = 1 + 1% = 1,01 Ohm ; 1 - 1% = 0,99 Ohm
R2 = 1k + 5% = 1050 Ohm ; 1k - 5% = 950 Ohm
Fazendo a relação do ganho (R2/R1) novamente temos:
G = 1050/1,01 = 1039,60 V/V em +5%
G = 950/0,99 = 959,59 V/V em -5%
O que gera uma diferença de aproximadamente 40V/V para mais ou para menos no ganho do circuito.

# 10. Faça um resumo explicando as limitações de tensão de entrada e saída de um AmpOp.
### a. Defina o que é um AmpOp Rail-to-rail.
Os valores de saída dos Ampops não ultrapassam os seus valores de entrada. Em um Ampop ideal, o valor de saída é igual ao de alimentação positivo do AmpOp. Esse valor máximo é chamado de saturação do AmpOp. Empiricamente, a saturação do AmpOp é na ordem de 90% do valor da alimentação positiva, isso também vale para valores negativos.
Um tipo de Ampop que soluciona esse problema é o AmpOp rail-to-rail, que consiste em um amplificador operacional onde é prometido que a saturação ocorra somente no limite do valor da alimentação, tanto positiva quanto negativa. Existem ampops rail-to-rail de entrada, saída, e ambos.

# 11. O que é tensão de offset? Como calcular o efeito resultante na tensão de saída de um amplificador inversor?
Tensão de offset é a diferença entre as tensões necessária entre os terminais de entrada para anular a saída.

# 12. Como minimizar o efeito da tensão de offset?
Para reduzir o efeito da tensão de offset é utilizado um divisor de tensão conectado ao estágio diferencial de entrada, balanceando assim as duas entradas em termos de corrente, mantendo a temperatura do ambiente constante e utilizando uma fonte de alimentação de boa confiabilidade.
# 13. O que é a variação da tensão de offset pela temperatura?
### a. Como verificar esse parâmetro no datasheet?
Encontrado nos datasheets como input offset voltage drift, e é medido em V/ºC, a variação da tensão de offset pela temperatura, como o próprio nome diz, ocorre quando há uma variação térmica no ambiente, alterando as características elétricas do amplificador. 

# 14. O que são as correntes de polarização (Ibias) de AmpOp?
### a. Como minimizar o efeito destas correntes? Descreva as aproximações e os possíveis circuitos para mitigar o problema.
### b. Descreva a corrente de offset na polarização dos AmpOp.
As correntes de polarização são correntes que passam pelas entradas de tensão do ampop, geralmente na ordem de nA. Em circuitos com realimentação, dependendo do resistor utilizado, podemos ter corrente desde a ordem de mA até nA, sendo que a corrente de polarização do Ampop é diretamente proporcional ao valor do resistor. Por meio dessas afirmações, é evidente que para minimizar o efeito das correntes de polarização, pode ser utilizado resistores de menor resistência.
