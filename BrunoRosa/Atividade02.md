
# Atividade 02
## Bruno Rosa
## Daniel Lohmann
## Eletrônica

# Questões

! Questão 1
### Amplificador Operacional é um Circuito Integrado (CI), capaz de manusear o sinal de entrada e realizar operações matemáticas como soma, subtração, multiplicação. Possui uma composição de muitos componentes como resistores, capacitores e transistores.

! Questão 2
### As características de um AmpOp Ideal são: Impedância de entrada infinita, impedância de saída nula e ganho infinito. Essas situações não são encotradas na prática e são utilizadas para fins didáticos.

! Questão 3
### Os sistemas em malha aberta independem do sinal de saída, não são realimentados. Já os sistemas em malha fechada recebem informações sobre a saída (realimentação) e, assim, são mais eficazes.

! Questão 4
### O método mais utilizado nos cálculos dos circuitos com AmpOp em malha fechada é a Primeira Lei de Kirchhoff (Lei dos Nós).

! Questão 5

### Seguidor de Tensão (Buffer);

### É obtido através de um Amp Op com configuração não inversora com R1 = oo e R2 = 0, para obtermos o amplificador de ganho unitário.

### Amplificador Inversor;

### A configuração Inversora consiste em um Amp Op e dois resistores R1 e R2. O resistor 2 é conectado entre o terminal de saída (3) e o terminal da entrada inversora (1), o que caracteriza uma realimentação negativa. 

### Amplificador não inversor;

### Nesta configuração, o sinal de entrada V1 é conectado diretamente ao terminal de entrada positivo do Amp Op e o Resistor 1 é conectado ao terra.

### Amplificador Somador Inversor;

### Esta configuração, é um circuito responsável por somar algebricamente as n tensões, cada uma multiplicada por um ganho constante, ou seja, cada entrada gera um ganho à saída.

### Amplificador Somador Não Inversor;

### O circuito do somador não inversor assemelha-se muito ao somador inversor, porém, neste caso as n entradas são conectadas ao terminal 2, ou entrada não inversora, por isso a tensão de saída não sofre inversão de sinal.

### Subtrator;

### Esta configuração permite que tenhamos uma tensão de saída igual a diferença entre as duas entradas multiplicada por um ganho.

### Amplificador de Instrumentação;

### O amplificador de instrumentação, é composto por dois amplificadores não inversores e um amplificador diferença.

! Questão 6
### Nossas análises foram feitas através de modelos de ampOps ideias, com suas características ideais, que fazem com que o ganho do amplificador tenda ao infinito. 

! Questão 7
### É a diferença potencial entre os sinais de sua entrada, saída inversora e não inversora. Em alguns circuitos pode haver problemas, a faixa de tensão do modo comum e a taxa de rejeição do modo comum (CMRR) são descritas para que possíveis erros de medidas não aconteçam.

! Questão 8
### O CMRR é a relação de rejeição de modo comum. De forma ideal, quando dois sinais de mesma frequência, amplitude e fase, são aplicados às entradas de um Amp Op, os mesmos devem se cancelar e nenhuma saída deve aparecer. Na prática, esta saída não é nula e é especificada em relação ao ganho máximo.

! Questão 9
### Afim de evitar distorção e/ou erros de leitura, existe um limite de tensão na entrada de acordo com a sua alimentação. 

! Questão 10
## A)
### Esses tipos de amplificadores tem como característica principal o "ajusta automático" da tensão de saída de acorda com as tensões de alimentação do ampOp.

! Questão 11
### Por definção, a tensão de offset é a tensão que aparece no terminal de saída (na ordem de milivolts) quando os terminais de entrada são curtocircuitados e causa um desiquilibrio interno. A solução para esse desequilibrio é conectar uma fonte de tensão de mesma amplitude, mas de polaridade oposta, ao valor da tensão de offset. 

! Questão 12
### Para minimizar o efeito da tensão de offset é necessário conectar à entrada do ampop uma fonte de tensão de mesmo valor, porém com polaridade oposta. Desta forma, idealmente uma iria anular a outra, entretanto, na prática existem outros efeitos geram alterações, como a variação da temperatura e as correntes indesejadas.

! Questão 13
### Alguns circuitos podem ser postos em temperaturas extremas como uma fundição ou um frigorifico, a tensão de offset pode ser afetada pela temperatura.

! Questão 14
### São correntes indesejáveis que surgem, naturalmente, com a aplicação de tensões nas entradas. Uma maneira que anular essas correntes é aterrar os terminais de entrada para que essas correntes não circulem internamente pelo ampOp.


