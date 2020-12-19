
# Atividade 02
## Bruno Rosa
## Daniel Lohmann
## Eletrônica

# Questões

 !Questão 1
### Amplificador Operacional é um Circuito Integrado (CI), capaz de manusear o sinal de entrada e realizar operações matemáticas como soma, subtração, multiplicação. Possui uma composição de muitos componentes como resistores, capacitores e transistores.

!Questão 2
### As características de um AmpOp Ideal são: Impedância de entrada infinita, ganho infinito e impedância de saída nula.

!Questão 3
### O sistema "malha aberta" não depende do sinal de saída, não são realimentados. Já o sistema "malha fechada" recebe informações sobre a saída (realimentação).

!Questão 4
### O método mais utilizado nos cálculos dos circuitos com AmpOp em malha fechada é a Primeira Lei de Kirchhoff (Lei dos Nós).

!Questão 5

### - Seguidor de Tensão (Buffer):

### É obtido através de um Amp Op com configuração não inversora com R1 = oo e R2 = 0, para obtermos o amplificador de ganho unitário.

### - Amplificador Inversor:

### Consiste em um Amp Op e dois resistores R1 e R2. O R2 é conectado entre o terminal da entrada inversora que causa uma realimentação negativa, e o terminal de saída. 

### - Amplificador não inversor:

###  O sinal de entrada V1 é conectado diretamente ao terminal de entrada positivo do Amp Op e o Resistor 1 é conectado ao terra.

### - Amplificador Somador Inversor:

### É um circuito responsável por somar algebricamente as n tensões, como cada tensão é multiplaca por um ganho constante fazendo com que haja um ganho à saída.

### - Amplificador Somador Não Inversor:

### O circuito do somador não inversor assemelha-se muito ao somador inversor, porém, neste caso as n entradas são conectadas ao terminal 2, ou entrada não inversora, por isso a tensão de saída não sofre inversão de sinal.

### - Subtrator:

### O Subtrator permite que tenhamos uma tensão de saída igual a diferença entre as duas entradas multiplicada por um ganho.

### - Amplificador de Instrumentação:

### É composto amplificador diferença e por dois amplificadores não inversores.

!Questão 6
 
!Questão 7
### É a diferença potencial entre os sinais de sua entrada, saída não inversora e inversora. Podemos ter problemas em alguns circuitos pois a (CMRR) e a faixa de tensão são descritas para que não tenhamos erros.

!Questão 8
### O CMRR é a relação de rejeição de modo comum. Quando dois sinais de mesma amplitude, frequência e fase, são aplicados às entradas de um Amp Op, eles devem cancelar-se entre sí, fazendo com que não tenha nenhuma saída. Porém na prática essa saída não é nula.

!Questão 9

!Questão 10
## A)
### É um amplificador que ajusta a tensão na saída com as tensões aplicadas na alimentação do Amp Op

!Questão 11
### Por definção, a tensão de offset é a tensão que aparece no terminal de saída (na ordem de milivolts) quando os terminais de entrada são curtocircuitados e causando assim um desiquilibrio interno. 

!Questão 12
### Para minimizar o efeito da tensão de offset é necessário conectar aos terminais de entrada do ampop uma fonte de tensão de mesmo valor, porém com polaridade oposta.Sendo assim, as tensões deveriam se anular porém com efeitos de correntes indesejadas e temperatura essa anulação não ocorre.

!Questão 13
### Alguns circuitos podem ser colocados em temperaturas elevadas ou baixas, a tensão offset é afetada fortemente por fortes variações de temperatura sejam elas muito baixas ou muito elevadas, afetando os circuitos.
### A)
### Podemos verificar esses parâmetros atráves do manual do fabricante sendo a tensão representada por ΔV/Δt e seu valor é fornecido em uV/°C.

!Questão 14
### São correntes indesejáveis que surgem com a aplicação de tensões nas entradas. Uma maneira de anular essas correntes é aterrar os terminais de entrada para que essas correntes não circulem internamente pelo ampOp.
### A)
### Introduzindo um resistor em série com o terminal de entrada inversora.
### B)
### É a diferença entre as correntes de polarização de entrada.


