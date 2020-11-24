# ATIVIDADE 1

## IMAGENS DAS RESOLUÇÕES DAS QUESTÕES

![resolção](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/resolu%C3%A7%C3%A3o%20parte%201.png)

![resolução2](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/resolu%C3%A7%C3%A3o%20parte%202.png)

### QUESTÃO 5

1. O que é o NETLIST?

+ É a descrição do circuito no SPICE. Se trata de uma declaração definindo cada elemento do circuito e suas propriedades

2. Como descrever o NETLIST de um circuito?

+ Primeiramente deve-se enumerar todos os nós presentes no circuito. Dessa forma, os componentes serão descritos por suas letras de referência, localização entre dois nós e o seu valor.

3. Como é representado cada um dos componentes? Explique com um exemplo.

+ O componente é representado por uma letra maiúscula(no caso do SPICE), os dóis nós que se encontram em seus polos e o seu valor. 

+ R25 6 0 100 (Resistor R25 conectado entre os nós 0 e 6 com valor de 100 ohms) 

4. O que é o “LABEL” de um nó e qual a vantagem de usar o mesmo?

+ O "label" de um nó seria um nome atribuído ao fio.

5. Quais os componentes básicos implementados no SPICE? (resistor, capacitor etc)

+ Resistor, capacitor, indutor, diodo e ground.

6. O que é um “SUBCKT”? Faça um exemplo.

+ É um subcircuito do SPICE. Um subcircuito simplifica as listas de spice netlists permitindo o reuso de um conjunto de elementos de circuito.

+ A sintaxe para criar um subcircuito é:

"SUBCKT <SubName> <N1> <N2> ...
...
.ENDS"

7. Como incluir novos modelos de componentes em um simulador SPICE?

b) Faça um resumo em forma de tutorial sobre o como funciona os parâmetros de simulação
do SPICE, respondendo:
1. O que é simulação transiente (.trans)? Quando usar? Faça um exemplo.
2. O que é simulação “ DC operating point” (.op)? Quando usar? Faça um exemplo
3. Quando usar .trans ou .op no SPICE?
4. O que faz a diretiva “.step”? Forneça exemplos de utilização.
5. O que faz a diretiva “.means”? Forneça exemplos de utilização.
6. O que é a simulação “DC sweep” (.dc)? Quando usar? Faça um exemplo.
7. Como simular um circuito em diferentes temperaturas de funcionamento?
