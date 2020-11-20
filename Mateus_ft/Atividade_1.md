**Questão 1, 2 e 3:**
![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/images/WhatsApp%20Image%202020-11-16%20at%2016.47.29.jpeg)

**Questão 3 e 4:**

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/images/WhatsApp%20Image%202020-11-16%20at%2016.50.10.jpeg)

Para comprovar os resultados obtidos nos cálculos manuais utilizou-se do simulador ltspice.

**Questão 1 a**
![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/images/simu%20Vo.png)

**Questão 1 b**
![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/images/simu%20Vo_b.png)

**Questão 2**
![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/images/simu%20Q2%20th.png)

Ainda, com o propósito de comprovar o cálculo nodal feito manualmente segue a imagem do resultado na calculador **HP**:
![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/images/hp%20prime%20comprov%20conta%20nodal.png)

**Questão 4**
![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/images/q4.png)

Observa-se que na verdade a tensão sobre R3 é de -240 Volts invertendo a polaridade. Pois a fonte de corrente controlada está no sentido contrário do usual.

***
**Questão 5**
**a**
1. O que é o **NETLIST**? 

Para acessar a netlist de um circuito é necessário acessar na barra superior o ícone *view*
![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/images/tutorial_ntelist.png)

Após acessar a netlist do circuito é possivel observar como o programa codifica a parte gráfica em texto.
![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/images/tutorial_ntelist2.png)
Na primeira coluna é apresentado o nome do componente ou fonte; na segunda observa-se o nome do nó em que o componente está conectado; na terceira o outro nó em que o componente está conectado; na última coluna está o valor do componente ou fonte.

2. Como descrever o **NETLIST** de um circuito?

Deve-se identificar os nós do circuito e a referência ground, após é importante observar em que nó cada componente está conectado, para então apontar na última coluna do netlist qual o valor dos componentes e das fontes.
3. Cada componente é identificado pelo seu nome da parte gráfica. Exemplo, se no resistor está definido na front end como R1. No NETLIST estará representado como R1 também.
![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/images/netlist_r.png)

4. Label de um nó é uma forma de nomear o nó, para deixar o circuito mais organizado. Para fazer isso basta apertar f4 que abrirá a janela *Net Name* nesse local deve-se nomear a label.

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/images/label.png)

Após nomear a label basta apertar no ok e coloca-la no nó onde desejar.

7. Para incluir componentes externos é necessário utilizar bibliotecas externas, essas são disponibilizadas pelos fabricantes e encontradas em seus sites.
Por exemplo o amplificador operacional TL082 da texas instruments:
Para adicionar esse componente ao LTSPICE é necessário ir até o site do fabricante e buscar pelo modelo spice:
![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/images/adc_tl082%20model%20spice.png)
![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/images/adc_tl082%20model%20spice%202.png)

Após fazer o download é necessário adicioná-lo ao circuito dessa forma:

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/images/bibext.png)

Para adicionar a biblioteca externa, após baixar o arquivo disponibilizado pelo fabricante é necessário indicar qual o caminho que o LTSPICE deve fazer para encontra-lo através de uma diretiva. Apontando o caminho. Após basta renomear o componente opamp2 para o nome do arquivo baixado.



**b**

1. A simulação transiente .tran analisa o circuito em função do tempo e descreve seu comportamente graficamente.
Exemplo:
![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/images/simu%20.tran%205.png)

É interessante usá-la em circuitos alternados. Que alteram os parametros de tensão e corrente ao longo do tempo.

2. A simulação DC operating point .op identifica os nós do circuito e resolve usando o método dos nós.
Exemplo:

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/images/simu%20.op.png)

É importante utiliza-la quando se está analisando um circuito de corrente contínua.










