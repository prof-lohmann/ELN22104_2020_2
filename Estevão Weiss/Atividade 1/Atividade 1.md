## Exercício 1
![](https://github.com/estevaoweiss/ELN22104_2020_2/blob/main/Estev%C3%A3o%20Weiss/Atividade%201/Exerc%C3%ADcio%201.jpg?raw=true)

## Exercício 2
![](https://github.com/estevaoweiss/ELN22104_2020_2/blob/main/Estev%C3%A3o%20Weiss/Atividade%201/Exerc%C3%ADcio%202.jpg?raw=true)

## Exercício 3
![](https://github.com/estevaoweiss/ELN22104_2020_2/blob/main/Estev%C3%A3o%20Weiss/Atividade%201/Exerc%C3%ADcio%203.jpg?raw=true)

## Exercício 4
![](https://github.com/estevaoweiss/ELN22104_2020_2/blob/main/Estev%C3%A3o%20Weiss/Atividade%201/Exerc%C3%ADcio%2004.jpg?raw=true)



## Exercício 5 - Tutorial básico sobre as operações e ferramentas do Spice

* NETLIST - Resumo

É a apresentação do(s) circuito(s) na forma de texto onde os componentes e fontes do(s) circuito(s) são representados e analisados através de nós.

* LABEL - Resumo

A ferramenta label serve para que os nós sejam nomeados e também é utilizada como uma conexão com o nó em questão, sem que seja necessário ligar um fio ao nó.

* Componentes Básicos

Os componentes mais utilizados no Spice são os resistores, diodos, capacitores e indutores.

* Subcircuito (SUBCKT)

Os subcircuitos são circuitos transformados num espécie de caixa preta para serem utilizados com bastante frequência. Um exemplo de subckt são os amplificadores operacionais (AMPOP) que são compostos por diversos componentes mas no Spice aparecem como uma "caixa preta" de 5 terminais.  

Como incluir novos modelos de componentes em um simulador SPICE?

* Simulação transiente (.trans)

Esta simulação é utilizada quando o intuito é analisar os comportamentos transitórios dos componentes. Abaixo o exemplo desta simulação em um circuito RC.
![](https://github.com/estevaoweiss/ELN22104_2020_2/blob/main/Estev%C3%A3o%20Weiss/Atividade%201/.trans.JPG?raw=true)

* Simulação DC operating point (.op)

Esta simulação é utilizado para circuitos que não terão variações ao longo do tempo (sem transitórios). Abaixo o exemplo do circuito do exercício 3 desta atividade.

![](https://github.com/estevaoweiss/ELN22104_2020_2/blob/main/Estev%C3%A3o%20Weiss/Atividade%201/.op.jpg?raw=true)

* Diretiva .step

Esta função serve para variar determinado parâmetro (valor de resistência, indutância, capacitância, etc) dentro de uma mesma simulação sem que seja preciso fazer várias simulações separadas. 

* Diretiva .meas

Esta função serve para analisar parâmetros em intervalos de tempos determinados. Por exemplo o comportamento transitório de um circuito RC num intervalo de 3u segundos.

* Simulação DC Sweep (.dc)

Está simulação é utilizada quando se quer variar valores de tensão de uma fonte CC. Segue o exemplo de uma simulação onde se varia gradativamente, de 0 a 10V, a tensão de uma fonte em um circuito puramente resistivo.

![](https://github.com/estevaoweiss/ELN22104_2020_2/blob/main/Estev%C3%A3o%20Weiss/Atividade%201/dc%20sweep.JPG?raw=true)

* Variação de temperatura em uma só simulação

Esta funcão é uma extensão da diretiva .step (citada acima), onde adicionamos o parametro de variação de temperatura (temp). 

