# atividade01

## Resolva as questões de 1 à 4 de forma manuscrita e coloque uma imagem da resolução no GIT, conforme indicado pelo professor

1. Escreve os valores de tensão Vo para cada uma das associações de fontes abaixo:
![resolução exercício 01](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/atv1-questao01.jpg)

2. Para o circuito abaixo, determine as tensões e correntes nodais, o valor da tensão Vo e o equivalente de thevenin. Considere: V1 = 5V, V2 = 10V, R1 = 10kΩ e R2 = 5k1Ω.
![resolução exercício 02](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/atv1-questao02.jpg)

3. Qual o valor da corrente I para o circuito abaixo? Considere: V1 = 12V, V2 = 10V, R1 = 10kΩ, R2 = 5k1Ω, R3 = 3k3Ω e R4 = 22kΩ.
![resolução exercício 03](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/atv1-questao03.jpg)

4. Qual o valor da queda de tensão sobre o resistor R3? Considere: V1 = 9V, R1= 3K3Ω, R2 = 1k2Ω, R3 = 10kΩ e gm = 10mA/V.
![resolução exercício 04](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/atv1-questao04.jpg)

5. Aprendendo a simular com o simulador LTSPICE 
## Atenção: Todoo o documento deve ser feito em MARKDOWN no GIT.

### a) Faça um resumo em forma de tutorial sobre o como funciona o SPICE e responda: 
1. O que é o NETLIST?
Uma das funcionalidades mais importantes para se manter a organização e entendimento dos circuitos em análise são as NETLIST, que são representações de textos e símbolos.
 
2. Como descrever o NETLIST de um circuito? 
As NETLISTS podem ser descritas com letras (exemplo: resistor = R1, R2…), símbolos (Ω, Σ, Δ...) e representação numérica (1, 2, 3…). Muito comum nas diversas descrições são as combinações de letras, números e símbolos, como já indicados.

3. Como é representado cada um dos componentes? Explique com um exemplo. 
Existem diversas formas de se representar os componentes num circuito, o mais comum é uma representação com: letra + índice + valor + símbolo. Porém, cada utilizados do simulador pode ter uma representação própria omitindo algumas informações. Por exemplo:
•	Para se representar um resistor:
o	R2=5Ω
o	R2=5
o	R=5
Observa-se que quanto  mais completos forem as informações, mais fácil será a compreensão inicial do circuito.

4. O que é o “LABEL” de um nó e qual a vantagem de usar o mesmo? 
O LABEL de um nó é uma indicação de pontos com os mesmos parâmetros físicos (valores). A utilização deste recurso além de facilitar a organização de circuitos mais complexos e com muitos componentes, permite a recuperação de daqueles valores de forma mais ágil.

5. Quais os componentes básicos implementados no SPICE? (resistor, capacitor etc) 
Os componentes mais básicos no SPICE são: resistor, capacitor, indutor e díodo.

6. O que é um “SUBCKT”? Faça um exemplo. 
A diretiva “.SUBCKT” é usada para definir um subcircuito que é chamado usando a declaração  adequada descrita anteriormente.

7. Como incluir novos modelos de componentes em um simulador SPICE?
### Assistir vídeo com passo-a-
[! [Inclusão de novos modelos de componentes - LTSPICE] (http://img.youtube.com/vi/RWYQ291X_0o/0.jpg)] (http://www.youtube.com/watch?v=RWYQ291X_0o "Inclusão de novos modelos de componentes - LTSPICE ")
 
### b) Faça um resumo em forma de tutorial sobre o como funciona os parâmetros de simulação do SPICE, respondendo: 
1. O que é simulação transiente (.trans)? Quando usar? Faça um exemplo. 
A simulação transiente (.trans) é quando ocorre em função do tempo.

2. O que é simulação “ DC operating point” (.op)? Quando usar? Faça um exemplo 
A simulação (.op) é aquela análise em corrente contínua.

3. Quando usar .trans ou .op no SPICE?
A decisão de se usar a função “.trans” ou a “.op”, é quando existe a necessidade de análise em função do tempo ou corrente contínua, respectivamente.

4. O que faz a diretiva “.step”? Forneça exemplos de utilização. 
A diretiva “.step” indica qual o valor de uma determinada constante que vai ser multiplicada a um componente de tempos em tempos.

5. O que faz a diretiva “.means”? Forneça exemplos de utilização. 
A diretiva “.means” mostra o valor médio de alguma variável que está sendo analisada.

6. O que é a simulação “DC sweep” (.dc)? Quando usar? Faça um exemplo. 
Este comando produz uma "varredura" ou variação da tensão de uma fonte de tensão especificada desde um valor inicial até um valor  final com incrementos sucessivos (o valor do incremento é indicado pelo projetista). 

7. Como simular um circuito em diferentes temperaturas de funcionamento?
Para se simular um circuito em diferente temperaturas de funcionamento, o projetista deverá utilizar a função “.temp” durante a simulação.
