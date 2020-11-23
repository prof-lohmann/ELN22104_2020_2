# Atividade 1
Aluno:
* Paulo Cezar Ventura Junior - <paulo.cvj@aluno.ifsc.edu.br>

Professores:
* Daniel Lohmann

## Exercício 01.

Figura 01 - Exercício 01.
No primeiro temos uma soma das tensões das duas fontes, ocasionando em 24V em Vo.
No segundo temos uma subtração pelo fato das fontes estarem em direções opostas, ocasionando 4V em Vo.

![ex01](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2001/Exerc%C3%ADcio01.png)

## Exercício 02.

Para descobrir Vo, fazemos o método nodal para encontrar a tensão nodal. Aplicando o método chegamos em Vo = -4,93V.
Para fazer o método de Thevenin, abrimos o circuito em Vo, fazendo com que o resistor de 5k1 Ohm não seja considerado.

Figura 02 - Exercício 02.

![ex02](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2001/Exerc%C3%ADcio02.png)

## Exercício 3.

Para calcular a corrente I no circuito, foi aplicado o método das malhas. Com ele chegamos a conclusão que I = i2 - i3 (de acordo com a orientação proposta na imagem).
Resolvendo o sistema de i1, i2 e i3, chegamos nas correntes i2 = 2,49 mA e i3 = 0,62 mA. Portanto I = 1,86 mA.

Figura 03 - Exercício 03.

![ex03](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2001/Exerc%C3%ADcio03.png)

## Exercício 04.

Para calcular a queda de tensão sobre R3, encontramos a corrente que passa na malha. Para encontrar essa corrente, encontramos o valor da corrente na fonte dependente (gm).
Com isso, é possível aplicar a primeira lei de Ohm e encontrar a queda de tensão em R3.

Figura 04 - Exercício 04.

![ex04](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2001/Exerc%C3%ADcio04.png)

## Exercício 05.

### O que é o NETLIST?
R: NETLIST é a descrição do circuito no SPICE, onde mostra os nós do circuito e os componentes que estão entre os nós.

### Como descrever o NETLIST de um circuito?
R: Em cada linha é apresentado um componente, os dois nós que estão entre ele e o valor do componente em questão.
Por exemplo, na imagem abaixo:

![NETLIST](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2001/Exemplos/ntlst.jpg)

O **NETLIST** fica da seguinte maneira:

```
V1 N1 N3 V
R1 N1 N2 R
R2 N2 N3 R
```

### Como é representado cada um dos componentes? Explique com um exemplo.
R: Cada componente vai ser representado por uma letra, junto com um índice. Por exemplo, na imagem anterior, o resistor R1 é representado da maneira: (Nome do resistor) (Nó de entrada) (Nó de saída) (Valor).

### O que é o “LABEL” de um nó e qual a vantagem de usar o mesmo?
R: O LABEL serve para identificar pontos chave do circuito em que está sendo utilizado. Por exemplo, é utilizado o LABEL para identificar um nó específico, e depois para comparar suas mudanças no NETLIST.
Também é possível utilizar LABEL para separar as conexões dos componentes, como pode ser visto na imagem abaixo:

![LABEL](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2001/Exemplos/lbl_ex01.jpg)

### Quais os componentes básicos implementados no SPICE? (resistor, capacitor etc)
R: Tem-se no SPICE os componentes resistor, capacitor, indutor, diodo e fonte.

### O que é um “SUBCKT”? Faça um exemplo.
R: Um SUBCKT é um subcircuito de um componente eletrônico, utilizando os componentes base para dar sentido a ele. Por exemplo, um Amplificador Operacional implementado no SPICE não vai ser naturalmente um componente só, nele terá que ter um subcircuito ordenando seu funcionamento de forma que no SPICE ele seja visualizado como um AmpOp.

### Como incluir novos modelos de componentes em um simulador SPICE?
R: É possível incluir procurando o modelo SPICE do componente em questão, ou criando o seu próprio componente. Por exemplo, fazer a criação de portas lógicas utilizando somente transistores.

## Exercício 06.

### O que é simulação transiente (.trans)? Quando usar? Faça um exemplo.
R: Simulação transiente é uma simulação não linear tendo em vista o tempo, utilizada em circuitos não lineares. Podemos utilizar para observar a carga em um capacitor variando no tempo.
Um possível exemplo é visto na imagem abaixo, onde uma fonte de tensão que varia com o tempo controla o circuito:

![simulação_cap](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2001/Exemplos/cir_tran.jpg)

Onde com a simulação transiente definimos o tempo inicial, tempo final da simulação e o espaçamento de tempo entre cada checagem do capacitor. Ficaria portanto um gráfico dessa maneira, visualizando tensão e corrente no capacitor em questão:

![grafico_sim1](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2001/Exemplos/graf_tran.jpg)

### O que é simulação “ DC operating point” (.op)? Quando usar? Faça um exemplo
R: A simulação .op analisa o circuito em corrente contínua, podendo ser utilizada em circuitos onde não há nada variando no tempo ou para analisar o estado inicial de um circuito em questão.
Por exemplo, podemos analisar o seguinte circuito:

![cir_op](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2001/Exemplos/cir_op.jpg)

Ao aplicar a simulação .op nesse circuito, recebemos esses valores de tensão e corrente no circuito:

![op1](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2001/Exemplos/op1.jpg)

### Quando usar .trans ou .op no SPICE?
R: A diretiva .trans deve ser utilizada em circuitos que variam com o tempo, enquanto a diretiva .op deve ser utilizada em circuitos em que não temos variação de nenhum componente (circuito CC) ou quando queremos analisar o estado inicial de um circuito elétrico.

### O que faz a diretiva “.step”? Forneça exemplos de utilização.
R: A diretiva .step realiza uma análise modificando um parâmetro de componente em cada repetição da diretiva. Podemos verificar o funcionamento de acordo com o exemplo a seguir:

![step_01](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2001/Exemplos/cir_step.jpg)

Neste exemplo, possuímos uma fonte onde estaremos modificando seu valor V de 3.3V para 12V, com um incremento de 0.1V por vez. Isto é possível utilizando o comando:

``
.step param V 3.3 12 0.1
``

Com isso, obtemos o gráfico.

![graf_step](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2001/Exemplos/graf_step.jpg)

### O que faz a diretiva “.meas”? Forneça exemplos de utilização.
R: A diretiva .meas faz uma análise específica de um ponto no circuito em certas condições.
Por exemplo, em um circuito em .trans podemos utilizar o .meas para verificar qual a tensão de um resistor em um determinado tempo.
A imagem a seguir mostra um exemplo:

![cir_meas](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2001/Exemplos/cir_meas.jpg)

Nele utilizamos uma fonte variando no tempo, e pedimos para medir a tensão no nó VC quando o tempo for 30ms.

Ao abrir o log do SPICE (Ctrl + L), recebemos a seguinte mensagem:

![log_spice](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2001/Exemplos/log_meas.jpg)

Indicando que a tensão em VC quando 30ms é 10.2311 V.

### O que é a simulação “DC sweep” (.dc)? Quando usar? Faça um exemplo.
R: A simulação .dc é bem parecida com a diretiva .step, porém é utilizada somente com fontes, onde é feito uma análise variando a tensão da fonte e apresentando os valores em um certo intervalo de tempo.
No exemplo da diretiva .step foi feito uma variação da fonte. A simulação .dc pode ser feita da seguinte maneira:

![sim_dc](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2001/Exemplos/cir_dc.jpg)

Dessa forma, temos que a fonte V1 vai variar de 0 a 12V, com incremento de 1V por vez, de acordo com o comando:

``
.dc V1 0 12 1
``

Assim obtemos o seguinte gráfico da tensão em V1:

![graf_dc](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2001/Exemplos/graf_dc.jpg)

### Como simular um circuito em diferentes temperaturas de funcionamento?
R: Pode ser feito utilizando a diretiva .TEMP para definir uma temperatura global em ºC, da seguinte maneira:

``
.TEMP 40
``

Dessa maneira definimos que a temperatura global do circuito vai ficar em 40ºC.
Também podemos utilizar a diretiva .STEP para variar a temperatura do circuito da maneira como quisermos.

``
.STEP temp 0 70 5
``

O comando acima varia a temperatura global de 0ºC a 70º em um passo de 5ºC por vez.

Outra opção seria variar localmente a temperatura de um componente, definindo ela no valor do componente em si.
Por exemplo, para um resistor, na opção de indicar seu valor podemos utilizar o seguinte:

``
100k temp = 100
``

Dessa forma, o resistor de 100k Ohm vai estar a 100ºC.

Por último, é possível também variar localmente a temperatura de um componente, utilizando uma variável ao invés de um valor em temp.

``
100k temp = {T1}
``

Assim a temperatura do resistor vai ser T1, onde pode-se variar em um comando .step.

``
.STEP PARAM T1 0 70 5
``

Onde T1 vai ser o valor da temperatura do resistor, que vai variar de 0ºC a 70ºC em um passo de 5ºC.
