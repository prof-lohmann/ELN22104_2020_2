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

"SUBCKT SubName N1 N2 ...
...
.ENDS"

7. Como incluir novos modelos de componentes em um simulador SPICE?

+ Basta procurar um modelo SPICE e incluir na biblioteca.

#### b)
1. O que é simulação transiente (.trans)? Quando usar? Faça um exemplo.

+ É  um simulação em que o tempo é um parâmetro. Pode ser usado para observar o valor de uma carga em função do tempo. Um exemplo seria um fonte que varia com o tempo controlando um circuito.

2. O que é simulação “ DC operating point” (.op)? Quando usar? Faça um exemplo

+ É uma simulação que analisa o circuito em corrente contínua.

3. Quando usar .trans ou .op no SPICE?

+ .trans deve ser usado em simulações em que o tempo é um parâmetro. Já .op deve ser usado em simulações em que os parâmetros não variam com o tempo, ou seja, corrente contínua. 

4. O que faz a diretiva “.step”? Forneça exemplos de utilização.

+ É uma simulação em que um parâmetro de um componente muda(aumenta ou diminui) a cada ciclo.

5. O que faz a diretiva “.means”? Forneça exemplos de utilização.

+ A diretiva realiza uma análise em um componente do circuito em condições controladas. Ou seja, medir um intervalo ou um ponto na absicissa.

6. O que é a simulação “DC sweep” (.dc)? Quando usar? Faça um exemplo.

+ A simulação .dc calcula as tensões e correntes contínuas de um circuito para uma de variáveis diversas.

7. Como simular um circuito em diferentes temperaturas de funcionamento?

+  Utilizando a diretiva .temp, definindo uma temperatura geral em °C para o circuito. Também é possível utilizar .step para variar a temperatura do circuito.
