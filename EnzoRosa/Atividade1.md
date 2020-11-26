# Atividade 1
## Questões 1, 2, 3, 4 
![resolução](https://github.com/enzosilvar/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/eln1.jpg)
![resolução](https://github.com/enzosilvar/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/eln2.jpg)


## Questão 5:
### A) O que é NETLIST?

+ O NETLIST é a descrição do circuito no SPICE, serve basicamente para analisar o circuito, relatando cada componente e propriedade no mesmo.

### B) Como descrever o NETLIST de um circuito?

+ Devemos enunciar todos os componentes presentes no circuito, juntamente com os nós que estão entre o próprio componente e seu valor.

### C) Como é representado cada um dos componentes? Explique com um exemplo.

+ Cada componente caracterizado por uma letra e um número, que seria para identificar qual componente é. Por exemplo: R5 N1 N2 10 (Resistor 5 vinculado com os respectivos nós 1 e 2, com o valor de 10 ohms).

### D) O que é o “LABEL” de um nó e qual a vantagem de usar o mesmo?

+ O LABEL é utilizado para identificar um nó específico, ou seja, é seu próprio nome, porém, ajuda o mesmo a ser detectado mais facilmente em grandes circuitos na hora da simulação e etc.

### E) Quais os componentes básicos implementados no SPICE? (resistor, capacitor etc)

+ São eles: Resistor, Capacitor, Indutor, Ground e Diodo.

### F) O que é um “SUBCKT”? Faça um exemplo.

+ Um SUBCKT é um subcircuito de um componente eletrônico, utiliza-se ele para simplificar o uso dos componentes no SPICE, deferindo assim a possivel reutilização de recursos já utlizados anteriormente no circuito. Para a criar o subcircuito: "SUBCKT SubName N7 N8 ...... .ENDS".

### G) Como incluir novos modelos de componentes em um simulador SPICE?

+ Devemos procurar o modelo SPICE de algum componente e incluir o mesmo na biblioteca.

## Questão 6:
### A) O que é simulação transiente (.trans)? Quando usar? Faça um exemplo.

+ A simulação transiente é uma simulação que tem seu fator o tempo, sendo assim pode ser utilizado para observar o valor de uma carga em função do tempo. Um exemplo seria uma fonte de tensão que varia com o tempo controlando o circuito.

### B) O que é simulação “ DC operating point” (.op)? Quando usar? Faça um exemplo.

+ Essa simulação teu seu fator a corrente contínua, ou seja, analisa o circuito nesse tipo de variação de corrente.

### C) Quando usar .trans ou .op no SPICE?

+ .trans é utilizado em simulações em que o seu fator é o tempo. Já .op deve ser usado em simulações em que os fatores não variam com o tempo, ou seja, utilizam a corrente contínua.

### D) O que faz a diretiva “.step”? Forneça exemplos de utilização.

+ A diretiva .step realiza uma análise modificando um parâmetro de componente em cada repetição da diretiva.

### E) O que faz a diretiva “.means”? Forneça exemplos de utilização.

+ A diretiva .meas faz uma análise específica de um ponto no circuito em certas condições. Por exemplo, em um circuito em .trans podemos utilizar o .meas para verificar qual a tensão de um resistor em um determinado tempo. 

### F) O que é a simulação “DC sweep” (.dc)? Quando usar? Faça um exemplo.

+ A simulação .dc calcula as tensões e correntes contínuas de um circuito. Um exemplo é que essa simulação é utilizado para descrever o comportamento de um transistor.

### G) Como simular um circuito em diferentes temperaturas de funcionamento?

+ Para simular um circuito em diferentes temperaturas no LTSpice, utilizamos a diretiva .STEP TEMP. Exemplo:

.step temp 50 90 10

A temperatura começa em 50ºC até 90ºC e tem variação de 10ºC. 


