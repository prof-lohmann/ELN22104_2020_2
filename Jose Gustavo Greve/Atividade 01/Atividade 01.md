
# Exercícios 1 -4

![exercícios 1 -4](https://github.com/JoseGustavoGreve/ELN22104_2020_2/upload/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Atividade%2001)
# Aprendendo a simular com o simuladores SPICE
## a) Faça um resumo em forma de tutorial sobre o como funciona o SPICE e responda:
### 1) O *netlist* é um documento de texto que faz a listagem dos componentes de um circuito e dos nós pelos quais estes componentes estão conectados.
### 2) Há uma formatação específica para a descrição de uma *netlist* e também símbolos que devem ser usados para representar cada componente.(resistores, capacitores, etc.)
### 3) No Netlist cada componente é representado por uma letra e um índice.
### 4) O LABEL serve para identificar pontos chave do circuito em que está sendo utilizado.
### 5) Resistores, indutores, capacitores,fontes.
### 6) É um subcircuito feito de componentes simples, para representar componentes mais complexos.
### 7) Procurando o modelo SPICE do componente que desejar.
## b)
### 1)É uma simulação não linear levando em consideração o tempo.
![tran](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Atividade%2001/tran.PNG)
### 2) É uma simulação para analisar uma corrente contínua.
![op](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Atividade%2001/op.PNG)
### 3) .trans se utiliza quando quiser fazer uma simulação em função do tempo, e o .op quando queremos fazer uma analise de corrente continua.
### 4) Serve para determinar qual constante que vai multiplicar um valor de um resistor em cada aumento.
### 5) Estabelece os valores médios de uma variavel
### 6) .dc é utilizada somente com fontes, analisando a variação da tensão da fonte.
![dc](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Atividade%2001/dc.PNG)
### 7) Utilizando .TEMP para se definir uma temperatura.
