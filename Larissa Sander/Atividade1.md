# Atividade 1
## Resoluções questões circuitos
![Resolução1](https://github.com/larissasander/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/IMG%201%20-%20Atividade%201.jpeg)
![Resolução2](https://github.com/larissasander/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/IMG%202%20-%20Atividade%201.jpeg)

## Resoluções questões teóricas

### a)  Faca um resumo em forma de tutorial sobre o como funciona o SPICE e responda:
### Questão 1) O que é o NETLIST?
A NETLIST é um texto que representa o circuito a ser simulado, ver a NETLIST ajuda na compreensão da linguagem do SPICE e suas simulações, pode ajudar também na identificação de erros na simulação e questões de convergência. 

### Questão 2) Como descrever o NETLIST de um circuito?
Para descrever a NETLIST de um circuito basta utilizar qualquer editor de texto que crie um arquivo ASCII. Para ver a NETLIST no LTSPICE é só utilizar o comando VIEW e depois SPICE NETLIST, é possível então copiar a NETLIST para a tela onde fica o circuito ou então copiar a NETLIST do SPICE para algum editor de texto. O SPICE reconhece o texto como uma NETLIST se o arquivo tiver a extensão “.cir”.

### Questão 3) Como e representado cada um dos componentes? Explique com um exemplo.
No asterisco é um comentário, mostra onde o arquivo está salvo dentro do meu computador, nas linhas seguintes está descrito o circuito. Os resistores estão representados por R1, R2 e R3, mostrando em qual nó eles estão localizados e quais são seus valores e as fontes estão representadas por V1 e V2, também mostrando o nó e seus valores. 
* C:\LARISSA\ENGENHARIA ELÉTRICA\ELETRÔNICA I\Exemplo Atividade 1.asc
+ R1 A N001 1k
+ R2 N002 A 2k
+ R3 0 A 1k
+ V1 N001 0 20
+ V2 N002 0 30
+ .backanno
+ .end

### Questão 4) O que é o “LABEL” de um nó e qual a vantagem de usar o mesmo?
Com o LABEL é possível dar “nome” aos nós, a vantagem de se utilizar ele é que você pode deixar o circuito mais genérico e organizado, ficando mais fácil também para identificar o nó na NETLIST.

### Questão 5) Quais os componentes básicos implementados no SPICE? (resistor, capacitor etc)
Os componentes básicos implementados no SPICE são: resistores, capacitores, diodos, amplificadores operacionais e transistor.

### Questão 6) O que e um “SUBCKT”? Faca um exemplo.
SUBCKT é um subcircuito, o SPICE possui os componentes básicos citados acima, já uma porta lógica, por exemplo, é feito da junção de alguns componentes básicos. Então, este subcircuito seria um bloco formado pelos componentes básicos. 

### Questão 7) Como incluir novos modelos de componentes em um simulador SPICE?
Primeiro você procura na internet o componente desejado no modelo SPICE, de preferência do site do fabricante do componente. Depois é só baixar o arquivo de texto fornecido no site, neste arquivo estão citados os componentes, subcircuitos, fontes, etc. Após é só copiar o texto do arquivo, clicar em “.op”, colocar o texto do arquivo e colocar do lado do circuito. Com o botão Ctrl+direto do mouse em cima do componente que você deseja que tenha o novo modelo, irá aparecer uma tela, na caixa de value, você insere o nome que está no texto que foi copiado. Então este componente estará sendo representado pelo subcircuito desejado. 

### b)Faca um resumo em forma de tutorial sobre o como funciona os parâmetros de simulação do SPICE, respondendo:

### Questão 1) O que é simulação transiente (.trans)? Quando usar? Faca um exemplo.
Uma simulação transiente é uma simulação onde o tempo é um parâmetro, ela pode ser utilizada para analisar o valor de uma carga em função tempo. Um exemplo de simulação transiente seria a simulação de uma fonte que varia com o tempo controlando um circuito.

### Questão 2) O que e simulação “DC operating point” (.op)? Quando usar? Faca um exemplo
Esta simulação analisa um circuito em corrente contínua.

### Questão 3) Quando usar .trans ou .op no SPICE?
.op deve ser utilizado em simulações em que os parâmetros não variam com o tempo, sendo assim, em corrente contínua. .trans deve ser utilizada em simulação onde o tempo é um parâmetro do circuito.

### Questão 4) O que faz a diretiva “.step”? Forneça exemplos de utilização.
.step é uma simulação em que as variáveis de um componente muda aumentando ou diminuindo a cada ciclo. A variável pode ser temperatura, um parâmetro do modelo, uma fonte independente. A variação pode ser linear, logarítmica ou através de uma lista de valores específicos. 

### Questão 5) O que faz a diretiva “.means”? Forneça exemplos de utilização.
.means faz uma análise em um componente do circuito, sendo útil para medir um intervalo sobre a abscissa. 


### Questão 6) O que e a simulação “DC sweep” (.dc)? Quando usar? Faca um exemplo.
A simulação DC sweep serve para calcular as correntes e tensões contínuas de um circuito  para alguma variável presente no circuito.

### Questão 7) Como simular um circuito em diferentes temperaturas de funcionamento?
Para simular um circuito em diferentes temperaturas de funcionamento basta utilizar a diretiva .temp e definir uma temperatural geral em graus Celsius e é possível também utilizar a diretiva .step para variar a temperatura geral do circuito.
