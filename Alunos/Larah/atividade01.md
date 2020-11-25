## Aps 01:
![Aps010102](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/aps_01.ex.1e2.jpg)


![Aps0103](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/aps_01.ex.3.jpg)

![Aps0104](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/aps_01.ex.4.jpg)


#  Questão 5
# a)

# O que é o NETLIST? Como descrever a NETLIST?
Netlist é a forma como um progama SPICE descreve os componentes de um circuito, indicando os nomes e nós relacionados a cada componente. A netlist pode ser descrita como um texto, no qual cada linha representa um componente, com o nome do componente seguido de seu nó origem, nó destino e de seu valor atribuído.

# Como é representado cada um dos componentes? Explique com um exemplo. O que é o “LABEL” de um nó e qual a vantagem de usar o mesmo?
Cada componente é representado por um símbolo, alguns predefinidos, sendo que existe também a possibilidade de desenhar seu próprio símbolo para um componente não exitente na bilbioteca padrão do SPICE.
LABEL é o nome dado a um nó, ele auxilia na organização do circuito facilitando a leitura do mesmo, observe o exemplo a seguir:
![circuito.semlabel](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/circuito.semlabel.JPG)

![netlist.semlabel](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/netlist.semlabel.JPG)

![circuito.comlabel](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/circuito.comlabel.JPG)

![netlist.commlabel](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/netlist.comlabel.JPG)


# Quais os componentes básicos implementados no SPICE?
Os componentes mais básicos do SPICE possuem ícones de atalhos na parte superior direita do programa, são eles:
![componentes.basicos](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/componentes.basicos.JPG)

Além destes, para acessar os demais componentes basta clicar no ícone "component" que se abrirá o seguinte menu:

![biblioteca.componentes](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/componentes.bilbioteca.JPG)

# O que é um “SUBCKT”? 
Um sub-circuito (SUBCKT) permite definir uma coleção de elementos como um sub-circuito, por exemplo, um amplificador operacional e
inserir esta descrição no circuito global, como qualquer outro componente. 
Um sub-circuito é definido através de uma declaração de controle .SUBCKT, seguido pela descrição do circuito como se
segue:
.SUBCKT SUBNAME N1 N2 N3 ...
Declaração dos elementos
.
.
.
.ENDS SUBNAME

# Como incluir novos modelos de componentes em um simulador SPICE?
Para incluir um novo modelo, pode se inserir o texto do subckt em uma diretiva .op na tela do esquemático ou então, com o texto salvo em um documento na pasta do seu projeto, usar a diretiva .lib com o caminho que leva ao documento para indicar que se quer utilizar aquele modelo de componente.

# b)

# 







