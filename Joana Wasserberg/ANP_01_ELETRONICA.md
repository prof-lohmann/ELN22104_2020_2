## Eletrônica 1 2020.2 
## Joana Wasserberg
---
## TUTORIAL: Aprendendo a simular com os simuladores *SPICE*.
-------------------------------------------------------------


### 1. O que é o NETLIST?
O NETLIST faz uma descrição do circuito, analisando através de nós e da referência terra. 

### 2. Como descrever o NETLIST de um circuito?
A partir dos nomes de nós que o circuito possui, o *SPICE* informará o mapeamento do mesmo.

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

INSERIR IMAGEM PRINT QUE BATI


### 7. Como incluir novos modelos de componentes em um simulador SPICE?

---
## Resumo sobre como funciona os parâmetros de simulação do *SPICE*.
### 1. O que é simulação transiente (. trans)? Quando usar? Faça um exemplo.
### 2. O que é simulação “DC operating point” (.op)? Quando usar? Faça um exemplo
### 3. Quando usar .trans ou .op no SPICE?
### 4. O que faz a diretiva “. step”? Forneça exemplos de utilização.
### 5. O que faz a diretiva “. means”? Forneça exemplos de utilização.
### 6. O que é a simulação “DC sweep” (.dc)? Quando usar? Faça um exemplo.
### 7. Como simular um circuito em diferentes temperaturas de funcionamento?
