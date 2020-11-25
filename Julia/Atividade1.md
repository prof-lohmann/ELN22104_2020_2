# ATIVIDADE 1

## Imagem das resoluções de Circuitos

![resolução](https://github.com/Julialcomelli/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/imagem%201.jpeg)

![resolução](https://github.com/Julialcomelli/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/imagem%202.jpeg)


### Questão 5

#### Parte A

1 O que é o NETLIST?
É um texto que descreve o circuito a ser simulado. Ele ajuda na identificação de erros e também na compreensão da linguagem no SPICE

2 Como descrever o NETLIST de um circuito?
Primeiro, deve-se enumerar os nós do circuito. Assim, os componentes vão ser descritos de acordo com a numeração que foi usada

3 Como é representado cada um dos componentes? Explique com um exemplo
São representados por uma letra maiúscula. Por exemplo, os resistores são representados por R1, R2 e R3.
R5 3 1 50 (resistor R5 que está conectado entre os nós 1 e 3, de 50 ohms

4. O que é o “LABEL” de um nó e qual a vantagem de usar o mesmo?
Com o LABEL você nomeia os componentes. A vantagem é que ele deixa o circuito mais organizado e fácil de visualizar

5 Quais os componentes básicos implementados no SPICE? (resistor, capacitor etc)
Resistor, diodo, capacitor, amplificador operacional e transistor

6 O que é um “SUBCKT”? Faça um exemplo.
é um subcircuito do SPICE. Seria um bloco formado pelos componentes básicos, permitindo o reuso de um conjunto de elementos

7 Como incluir novos modelos de componentes em um simulador SPICE?
Primeiro deve procurar, de preferência, no site do fabricante o componente, baixar o arquivo de texto e incluir na biblioteca

#### Parte B

1 O que é simulação transiente (.trans)? Quando usar? Faça um exemplo.
é uma simulação que tem como parâmetro o tempo. Usado para observar a variação de uma carga em função do tempo. Um exemplo é uma fonte que varia com o tempo

2 O que é simulação “ DC operating point” (.op)? Quando usar? Faça um exemplo
é usado para analisar circuitos em análise contínua

3 Quando usar .trans ou .op no SPICE?
O .trans se usa quando o tempo é um parâmetro. O .op deve ser usado em corrente contínua

4 O que faz a diretiva “.step”? Forneça exemplos de utilização.
é uma simulação em que a cada ciclo um parâmetro de um componente muda, aumentando ou diminuindo

5 O que faz a diretiva “.means”? Forneça exemplos de utilização
Ela mede um intervalo de um ponto na abcissa, analisando um componente do circuito

6 O que é a simulação “DC sweep” (.dc)? Quando usar? Faça um exemplo.
Ela traça os gráficos das correntes e tensões no circuito em função da variação de uma fonte DC

7 Como simular um circuito em diferentes temperaturas de funcionamento?
usando a diretiva.temp e definindo uma temperatura em C°. Ou usando o .step variando a temperatura


