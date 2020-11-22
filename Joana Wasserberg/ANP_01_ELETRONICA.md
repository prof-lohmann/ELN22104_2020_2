## Eletrônica 1 2020.2 
## Joana Wasserberg
---
## TUTORIAL: Aprendendo a simular com os simuladores *SPICE*.
-------------------------------------------------------------


### 1. O que é o NETLIST?
O NETLIST faz uma descrição do circuito, analisando através de nós e da referência terra. 

### 2. Como descrever o NETLIST de um circuito?
A partir dos nomes de nós que o circuito possui, o *SPICE* informará o mapeamento do mesmo.

![Exemplo NETLIST](https://github.com/joananana/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Joana%20Wasserberg/Imagens/Netlist.PNG)

Na aba principal do programa vá para **VIEW-> NETLIST Spice**. Assim, exibirá uma nova janela com a descrição do circuito respectivo.

### 3. Como é representado cada um dos componentes? Explique com um exemplo.
Os componentes são representados por letras e um respectivo número para indicar qual dos componentes é.

Exemplo: Resistor [R], Capacitor [C], Transistor MOS [M],     Sub-circuito [X].

### 4. O que e o “LABEL” de um nó e qual a vantagem de usar o mesmo?
O *LABEL* de um nó é o nome desse nó. Utilizar ele facilita implementar um circuito muito grande, assim como, quando simular o circuito, a visualização fica mais fácil.

### 5. Quais os componentes básicos implementados no SPICE? (resistor, capacitor).
O *SPICE* já possui uma biblioteca padrão, os principais componentes são: Resistor, Capacitor, Indutor, Diodo, Zener.

### 6. O que e um “SUBCKT”? Faça um exemplo.
O *SPICE* tem símbolos "modelos" para certos componentes reais desde que esses componentes compartilhem uma lista de rede de pinos e portas idênticas em ordem. Para isso, se utiliza a diretiva .SUBCKT associando um modelo do *SPICE* a um componente.

![Exemplo SUBCKT](https://github.com/joananana/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Joana%20Wasserberg/Imagens/subckt.PNG)


### 7. Como incluir novos modelos de componentes em um simulador SPICE?
Com o modelo do componente baixado no seu computador, escolha um componente que de adeque e o modelo pode ser incluido usando a diretiva .LIB seguindo o destino até chegar no arquivo do componente ou utilizar o .OP e colar o texto descritivo do modelo do componente.

---
-----

## Resumo sobre como funciona os parâmetros de simulação do *SPICE*.
---


### 1. O que é simulação transiente (. trans)? Quando usar? Faça um exemplo.
A simulação transiente é uma simulação em função do temppo, útil para circuitos que apresentem mudanças ao decorrer do tempo nos valores analisados.

![]()

### 2. O que é simulação “DC operating point” (.op)? Quando usar? Faça um exemplo
A simulação DC ponto de operação faz apenas uma análise do circuito em corrente contínua, útil para analisar o estado inicial de um circuito ou para analisar seu comportamente em corrente contínua.

![]()

### 3. Quando usar .trans ou .op no SPICE?
Utilizar .TRANS quando deseja-se analisar as alterações de um circuito no decorrer do tempo e utilizar .OP quando deseja-se analisar um circuito em corrente contínua.

### 4. O que faz a diretiva “.step”? Forneça exemplos de utilização.
A diretiva .STEP faz uma variação de determinado parâmetro de um componente no circuito utilizado.
Exemplo:

.step param X 5k 10k 1k

![]()

O parâmetro {X} é um resistor que começa em 5k Ω até 10k Ω e varia seu valor em 1k Ω.

### 5. O que faz a diretiva “.means”? Forneça exemplos de utilização.
A diretiva .MEANS avalia as grandezas elétricas definidas pelo usuário.  A utilização mais comum é usada para imprimir um valor de dados ou sua expressão em um ponto específico ou quando uma condição é atendida.

### 6. O que é a simulação “DC sweep” (.dc)? Quando usar? Faça um exemplo.
A simulação DC sweep faz uma variação da tensão de uma determinada fonte de corrente contínua.
Utiliza-se para analisar o comportamente de um transistor, pro exemplo.

### 7. Como simular um circuito em diferentes temperaturas de funcionamento?
Para simular um circuito em diferentes temperaturas no LTSpice, utilizamos a diretiva .STEP TEMP.
Exemplo:

.step temp 30 60 10

A temperatura começa em 30ºC até 60ºC e tem variação de 10ºC.
