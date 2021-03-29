![logo_ifsc](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade_01/figuras_atividade_01/logo_ifsc.jpg)

# ATIVIDADE_01
## Aluno: Marcos Paulo Pacheco

# PRIMEIRA PARTE: 

## Resolva as questões de 1 à 4 de forma manuscrita e coloque uma imagem da resolução no GIT, conforme indicado pelo professor

1. Escreve os valores de tensão Vo para cada uma das associações de fontes abaixo:
![resolução exercício 01](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade_01/figuras_atividade_01/atv1-questao01.jpg)

2. Para o circuito abaixo, determine as tensões e correntes nodais, o valor da tensão Vo e o equivalente de thevenin. Considere: V1 = 5V, V2 = 10V, R1 = 10kΩ e R2 = 5k1Ω.
![resolução exercício 02](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade_01/figuras_atividade_01/atv1-questao02.jpg)

3. Qual o valor da corrente I para o circuito abaixo? Considere: V1 = 12V, V2 = 10V, R1 = 10kΩ, R2 = 5k1Ω, R3 = 3k3Ω e R4 = 22kΩ.
![resolução exercício 03](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade_01/figuras_atividade_01/atv1-questao03.jpg)

4. Qual o valor da queda de tensão sobre o resistor R3? Considere: V1 = 9V, R1= 3K3Ω, R2 = 1k2Ω, R3 = 10kΩ e gm = 10mA/V.
![resolução exercício 04](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade_01/figuras_atividade_01/atv1-questao04.jpg) OBS: O exercício 4 foi corrigido conforme correção em vídeo aula.


# SEGUNDA PARTE: 

## 5. Aprendendo a simular com o simulador LTSPICE - Atenção: todo o documento deve ser feito em MARKDOWN no GIT.
### a) Faça um resumo em forma de tutorial sobre o como funciona o SPICE e responda: 
________________________________________________________________________________________________________________________________________________________________________________

# FAQ 

## FUNCIONAMENTO DO SPICE
### 1. O que é o NETLIST?
### 2. Como descrever o NETLIST de um circuito?
### 3. Como é representado cada um dos componentes? Explique com um exemplo.
### 4. O que é o “LABEL” de um nó e qual a vantagem de usar o mesmo?
### 5. Quais os componentes básicos implementados no SPICE?
### 6. O que é um “SUBCKT”? Faça um exemplo.
### 7. Como incluir novos modelos de componentes em um simulador SPICE?
##   
## FUNCIONAMENTO DOS PARÂMETROS DE SIMULAÇÃO SPICE
### 1. O que é simulação transiente (.trans)? Quando usar? Faça um exemplo.
### 2. O que é simulação “ DC operating point” (.op)? Quando usar? Faça um exemplo
### 3. Quando usar .trans ou .op no SPICE?
### 4. O que faz a diretiva “.step”? Forneça exemplos de utilização.
### 5. O que faz a diretiva “.means”? Forneça exemplos de utilização.
### 6. O que é a simulação “DC sweep” (.dc)? Quando usar? Faça um exemplo.
### 7. Como simular um circuito em diferentes temperaturas de funcionamento?

________________________________________________________________________________________________________________________________________________________________________________
# RESPOSTAS
## FUNCIONAMENTO DO SPICE

>>1. Uma das funcionalidades mais importantes para se manter a organização e entendimento dos circuitos em análise. O NETLIST é uma descrição de um circuito em forma de texto detalhando todos os componentes que o compõe. Nessa lista, é possível observar além dos componentes, os conectores e nós (desde que devidamente identificados no circuito em simulação pelo próprio usuário). Ao se “setar” o NETLIST, aparecerá uma caixa de texto com todas as declarações realizadas.\
• VISUALIZAÇÃO DO NETLIST:\
           o 1 – clicar em “View” (barra de ferramentas);\
           o 2 – selecionar “SPICE Netlist”.\
![resolução exercício 05_1](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade_01/figuras_atividade_01/atv1-questao05_1.jpg)

>>2. As NETLISTS podem ser descritas com letras (exemplo: resistor = R1, R2…), símbolos (Ω, Σ, Δ...) e representação numérica (1, 2, 3…). Muito comum nas diversas descrições são as combinações de letras, números e símbolos, como já indicados.\
• DESCRIÇÃO DAS INFORMAÇÕES NO NETLIST:\
           o 1ª. coluna: declaração dos componentes;\
           o 2ª. e 3ª. colunas: indicação dos nós de conexão do componente;\
           o 4ª. coluna: valor físico do componente.\
 ![resolução exercício 05_2](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade_01/figuras_atividade_01/atv1-questao05_2.jpg)

>>3. Os componentes são representados por uma letra seguido por um índice para valoração do respectivo parâmetro. Por exemplo no circuito ilustrativo:\
• RESISTOR: representado pela letra "R", seguido pelo índice (1,2,3...);\
• CAPACITOR: presentado pela letra "C", seguido pelo índice(1);\
• FONTE: presentado pela letra "V", seguido pelo índice (1)\
• FATOR MÚLTIPLICADOR: caso o valor numérico do parâmetro possua fatores multiplicadores ou divisores de potências de "10", no exemplo tem-se K (x10^3) e m (x10^-3).\
Observa-se que quanto  mais completas forem as informações, mais fácil será a compreensão inicial do circuito, ainda mais naqueles que sejam mais complexos, com mais componentes representados, por exemplo.\
![resolução exercício 05_3](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade_01/figuras_atividade_01/atv1-questao05_3.jpg)

>>4. O LABEL de um nó é uma indicação de pontos com os mesmos parâmetros físicos (valores). A utilização deste recurso além de facilitar a organização de circuitos mais complexos e com muitos componentes, permite a recuperação daqueles valores de forma mais ágil. A figura a seguir indica como esse recurso pode ser interessante, mostrando que partes do circuito com funções específicas, podem "ficar separadas" do circuito principal, porém, mantendo suas funcionalidades, ou seja, o LABEL faz a conexão física entre esses pontos de maneira "virtual".\
![resolução exercício 05_4](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade_01/figuras_atividade_01/atv1-questao05_4.jpg)

>>5. Os componentes mais básicos no SPICE são: resistor, capacitor, indutor e díodo, além do terra. Importante salientar que os componentes podem ser inseridos tanto pela barra de ferramentas, através dos botões dos respectivos símbolos ou por teclas de atalho, pelas letrass R, C, L, D e G, respectivamente.\
![resolução exercício 05_5](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade_01/figuras_atividade_01/atv1-questao05_5.jpg)

>>6. A diretiva “.SUBCKT” é usada para definir um subcircuito que é chamado usando a declaração conforme indicada a seguir:\
                      • .SUBCKT <NOME> [NÓ]*\
           o A declaração ".SUBCKT" inicia a definição de um subcircuito;\
           o A definição termina com uma declaração ".ENDS";\
           o Todas as declarações entre .SUBCKT e .ENDS são incluídas na definição;\
           o Sempre que o subcircuito é chamado por uma declaração "NOME", todas as declarações na definição substituem a declaração de chamada. 
 

>>7. Assistir vídeo com passo-a-passo\
![resolução exercício 05_7](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade_01/figuras_atividade_01/atv1-questao05_7.jpg)\

[! [] (http://img.youtube.com/vi/RWYQ291X_0o/0.jpg)] (http://www.youtube.com/watch?v=RWYQ291X_0o "Inserção novos modelos - LTSPICE")[![Inserção novos modelos - LTSPICE](http://img.youtube.com/vi/RWYQ291X_0o/0.jpg)](http://www.youtube.com/watch?v=RWYQ291X_0o "Inserção novos modelos - LTSPICE")


# RESPOSTAS
## FUNCIONAMENTO DOS PARÂMETROS DE SIMULAÇÃO SPICE

1. A simulação transiente (.trans) é quando ocorre em função do tempo.

2. A simulação (.op) é aquela análise em corrente contínua.

3. A decisão de se usar a função “.trans” ou a “.op”, é quando existe a necessidade de análise em função do tempo ou corrente contínua, respectivamente.

4. A diretiva “.step” indica qual o valor de uma determinada constante que vai ser multiplicada a um componente de tempos em tempos.

5. A diretiva “.means” mostra o valor médio de alguma variável que está sendo analisada.

6. Este comando produz uma "varredura" ou variação da tensão de uma fonte de tensão especificada desde um valor inicial até um valor  final com incrementos sucessivos (o valor do incremento é indicado pelo projetista). 

7. Para se simular um circuito em diferente temperaturas de funcionamento, o projetista deverá utilizar a função “.temp” durante a simulação.
