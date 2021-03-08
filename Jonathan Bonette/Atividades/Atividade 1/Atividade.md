<table align="center"><tr><td align="center" width="9999"><br>
<img src="../../Imagens/logoifsc.png" align="center" width="150" alt="Logo IFSC">

# Atividade 1

<b>Instituto Federal de Educação, Ciência e Tecnologia de Santa Catarina<br>
Campus Florianópolis<br>
Departamento Acadêmico de Eletrônica<br>
Eletrônica I</b>

*Jonathan Chrysostomo Cabral Bonette*
</td></tr></table>


<b>1. Escreve os valores de tensão Vo para cada uma das associações de fontes abaixo:</b><br>
<p align="center"><img src="../../Imagens/Atividade 1/1.png" align="center"><br></p>

*No LTSpice podemos ver que batem as afirmações teóricas para o Exercício 1a*

<p align="center"><img src="../../Imagens/Atividade 1/1alt.png" align="center"><br></p>
<p align="center"><img src="../../Imagens/Atividade 1/ex1a.png" align="center"><br></p>

*No LTSpice podemos ver que batem as afirmações teóricas para o Exercício 1b*

<p align="center"><img src="../../Imagens/Atividade 1/1blt.png" align="center"><br></p>
<p align="center"><img src="../../Imagens/Atividade 1/ex1b.png" align="center"><br></p>

---

<b>2. Para o circuito abaixo, determine as tensões e correntes nodais, o valor da tensão Vo e o equivalente de thevenin. Considere: V1 = 5V, V2 = 10V, R1 = 10kΩ e R2 = 5k1Ω.</b>
<p align="center"><img src="../../Imagens/Atividade 1/2.png" align="center"><br></p>

*No LTSpice podemos ver que batem as afirmações teóricas, porém como mostrado pelo LTSpice no resultado final já temos o valor com seu sinal trocado, pela polaridade do circuito*

<p align="center"><img src="../../Imagens/Atividade 1/2lt.png" align="center"><br></p>
<p align="center"><img src="../../Imagens/Atividade 1/ex2.png" align="center"><br></p>

---

<b>3. Qual o valor da corrente I para o circuito abaixo? Considere: V1 = 12V, V2 = 10V, R1 = 10kΩ, R2 = 5k1Ω, R3 = 3k3Ω e R4 = 22kΩ.</b>
<p align="center"><img src="../../Imagens/Atividade 1/3.png" align="center"><br></p>

*No LTSpice podemos ver que batem as afirmações teóricas, o valor real da corrente I1 tem seu sinal trocado pela polaridade do circuito*

<p align="center"><img src="../../Imagens/Atividade 1/3lt.png" align="center"><br></p>
<p align="center"><img src="../../Imagens/Atividade 1/ex3 (correntes trocadas).png" align="center"><br></p>

---

<b>4. Qual o valor da queda de tensão sobre o resistor R3? Considere: V1 = 9V, R1= 3K3Ω, R2 = 1k2Ω, R3 = 10kΩ e gm = 10mA/V</b>
<p align="center"><img src="../../Imagens/Atividade 1/4.png" align="center"><br></p>

*No LTSpice podemos ver que batem as afirmações teóricas, vemos que o valor real da tensão e da corrente tiveram seus sinais trocados pela polaridade do circuito*

<p align="center"><img src="../../Imagens/Atividade 1/4lt.png" align="center"><br></p>
<p align="center"><img src="../../Imagens/Atividade 1/ex4.png" align="center"><br></p>

---

<b>5. Aprendendo a simular com o simuladores SPICE.</b>

<b>a) Faça um resumo em forma de tutorial sobre o como funciona o SPICE e responda:</b><br>
<b>1. O que é o NETLIST?</b><br>
  *Uma NETLIST spice é uma representação baseada em texto de um circuito.*<br><br>
<b>2. Como descrever o NETLIST de um circuito?</b><br>
*Descrevemos com letras, palavras, simbolos ou números.*<br><br>
<b>3. Como é representado cada um dos componentes? Explique com um exemplo.</b><br>
*Cada componente é representado por uma letra ou símbolo que armmazena um valor. Ex: V1=12.*<br><br>
<b>4. O que é o “LABEL” de um nó e qual a vantagem de usar o mesmo?</b><br>
*Label é usualmente usado como um tipo de malha especial, onde os pontos definidos possuem o mesmo valor. Sua vantagem é que a recuperação de dados é muito mais rápida.*<br><br>
<b>5. Quais os componentes básicos implementados no SPICE? (resistor, capacitor etc)</b><br>
*Resistores, capacitores, indutores, entre outros.*<br><br>
<b>6. O que é um “SUBCKT”? Faça um exemplo.</b><br>
*É um subcircuito que envolve um bloco de texto do circuito e permite conexões externas a este circuito apenas através dos nós do subcircuito.*<br><br>
<b>7. Como incluir novos modelos de componentes em um simulador SPICE?</b>
*Abra o arquivo netlist que contém as definições de subcircuito no LTspice (Arquivo > Abrir ou arraste o arquivo para o LTspice). Edite o símbolo se necessário e salve.*<br><br>


<b>b) Faça um resumo em forma de tutorial sobre o como funciona os parâmetros de simulação do SPICE, respondendo:</b><br>
<b>1. O que é simulação transiente (.trans)? Quando usar? Faça um exemplo.<br></b>
 *Uma simulação em função do tempo.*<br><br>
<b>2. O que é simulação “ DC operating point” (.op)? Quando usar? Faça um exemplo</b><br>
 *Uma simulação de corrente contínua.*<br><br>
<b>3. Quando usar .trans ou .op no SPICE?</b><br>
 *Quando quisermos analisar um circuito pela função do tempo ou uma em corrente contínua.*<br><br>
<b>4. O que faz a diretiva “.step”? Forneça exemplos de utilização.</b><br>
 *Determina qual o valor da constante que vai ser multiplicada a um valor de componente de tempos em tempos.*<br><br>
<b>5. O que faz a diretiva “.means”? Forneça exemplos de utilização.</b><br>
 *Mostra qual o valor médio de alguma variável.*<br><br>
<b>6. O que é a simulação “DC sweep” (.dc)? Quando usar? Faça um exemplo.</b><br>
 *Simulação feita ao analisar um período determinado.*<br><br>
<b>7. Como simular um circuito em diferentes temperaturas de funcionamento?</b><br>
*Usando .temp na simulação.*<br><br>
