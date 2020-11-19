# Atividade 1 
## Exercicio 5
### Tutorial Basico de LTSpice

#### Sobre o LTSpice:

O LTSpice é um simulador ideal para testar a integridade e funcionamento de circuitos AC e DC de forma pratica, possuindo as seguintes caracteristicas:

* Possui editor de Esquematicos e componentes;
* Possui uma biblioteca de componentes passivos (R, L, C);
* Possui biblioteca de componentes lineares;
* Simulador e visualizador de curvas e sinais;
* Transiente, análise AC e DC, estado estacionário e pontos de operação DC.

#### LTSpice Download e instalação:

O LTSpice é um simulador gratuito, sendo possivel ser baixado [aqui](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html). 

#### Utilizando o LTSpice:

Depois de instalar o programa e executá-lo, você verá uma tela como esta abaixo:

![Imagem 1](https://user-images.githubusercontent.com/12564754/99699183-6b4f6080-2a70-11eb-8c01-83b15cfb577e.PNG)

Para realmente começar a desenhar um esquema, você precisará clicar no menu File e em seguida Nem Schematic (tela abaixo). Será criado um novo arquivo
com a extensão .asc.

![Imagem 2](https://user-images.githubusercontent.com/12564754/99699402-abaede80-2a70-11eb-949d-efef638d3932.png)

A partir daqui, você pode começar a inserir e editar componentes, mas primeiro vamos examinar alguns atalhos de teclado. Você pode encontrar a maioria deles na barra de ferramentas acima da janela do circuito, ou também nos menus Edit e View, se preferir acessá-los dessa forma. Se você ficar preso ao trabalhar com o LTSpice, há um conjunto bastante abrangente de recursos disponíveis no menu Help, incluindo mais exemplos relacionados ao uso. 

##### Aqui está uma lista de algumas teclas de atalho para criar seu esquema:

**R:** Inserir Resistor

**C:** Inserir Capacitor

**L:** Inserir Indutor

**D:** Inserir Diodo

**G:** Inserir Aterramento

**F2:** Menu do Componente

**F3:** Inserir Linha

**F4:** Etiqueta de Linha

**F5:** Delete (aperte F5 quando clicar no componente)

**F6:** Copiar

**F7:** Mover sem as Linhas

**F8:** Mover e segurar com as Linhas

**F9:** Desfazer (shift + F9 para refazer)

**CTRL+R:** Rotacionar (com o componente selecionado)

**CTRL+E:** Espelhar (com o componente selecionado)

Para alterar as propriedades dos componentes selecionados, basta clicar com o botao esquerdo do mouse sobre o componente desejado.


##### Execucao de Simulacoes e Sinais Senoidais:

Para rodar a simulacao do circuito feito, basta clicar no botao Run, como na imagem a baixo:

![Imagem 4](https://user-images.githubusercontent.com/12564754/99699495-bf5a4500-2a70-11eb-82fc-5a3271268024.PNG)

Note que aparecera uma janela para inserir as informacoes de como sera realizada a execucao. Apos configurar e mandar executar a simulacao, uma nova janela com o título “Draft1.raw” se abrirá (imagem abaixo). Nela serão mostrados os resultados da simulação.

![Imagem 5](https://user-images.githubusercontent.com/12564754/99699525-cbde9d80-2a70-11eb-83e0-234eb91abc01.PNG)

A partir de agora, se aproximarmos o mouse de alguma linha ou componente, aparecesera uma ponta de medida de tensao ou corrente. Se clicar sobre a linha ou componente, automamticamente aparecera o sinal na janela com o título “Draft1.raw”.

### Topicos avancados sobre o LTSpice:

### Questões Propostas (a):

1. O que é NETLIST?

> Uma netlist é uma representação baseada em texto de um circuito. Ela é utilizada para aprender sobre a sintaxe e simulação do SPICE. Também pode ajudar na identificação de erros de simulação e problemas de convergência.

2. Como descrever o NETLIST de um circuito?

> O netlist pode ser gerado pelo programa EDFIL, a partir do diagrama esquemático. Primeira linha: Comentário (o editor EDFIL coloca o número de nós nesta linha).Linhas seguintes: Descrição do circuito, com um elemento por linha. A primeira letra determina o tipo de elemento.

3. Como é representado cada um dos componentes? Exemplo.

> * Resistor: R<nome> <nó1> <nó2> <Resistência>
> * Indutor: L<nome> <nó1> <nó2> <Indutância>
> * Capacitor: C<nome> <nó1> <nó2> <Capacitância>
> * Fonte de tensão controlada a tensão: E<nome> <nóV+> <nóV-> <nóv+> <nóv-> <Av>
> * Fonte de corrente controlada a corrente: F<nome> <nóI+> <nóI-> <nói+> <nói-> <Ai>
> * Fonte de corrente controlada a tensão: G<nome> <nóI+> <nóI-> <nóv+> <nóv-> <Gm>
> * Fonte de tensão controlada a corrente: H<nome> <nóV+> <nóV-> <nói+> <nói-> <Rm>
> * Fonte de corrente: I<nome> <nó+> <nó-> <parâmetros>
> * Fonte de tensão: V<nome> <nó+> <nó-> <parâmetros>
> * Amplificador operacional ideal: O<nome> <nó saída+> <nó saída-> <nó entrada+> <nó entrada->
> * Resistor linear por partes: N<nome> <nó+> <nó-> <4 pontos vi ji >
> * Transformador ideal: K<nome> <nó a> <nó b> <nó c> <nó d> <n>
> * Chave: $<nome> <nó a> <nó b> <nó controle c> <nó controle d> <gon> <goff> <vref>
> * Comentário: *<comentário>

4. O que é o LABEL de um nó e qual a vantagem de usar o mesmo?

> É a atribuicao de uma identificação à um fio, dando qualquer nome que se queira a ele. Assim em qualquer outra parte do circuito que for inserido o mesmo nome, o simulador entenderá que trata-se do mesmo ponto. 

5. Quais os componentes  básicos  implementados  no Spice?

> Biblioteca de componentes passivos ( como R, L, C)e biblioteca de componentes lineares.

6. O que é um SUBCKIT? Exemplo.

> É a criacao automaticamente de um símbolo para um modelo customizado, ou você pode associar um subcircuito a um símbolo intrínseco LTspice, desde que o modelo .SUBCKT desejado e o símbolo intrínseco compartilhem uma lista de rede de pinos / portas de idêntica ordem.
> Exemplo:
>

7. Como incluir novos modelos de componentes em um simulador Spice.

> resposta

### Questões Propostas (b):

l. O que é simulação transiente (trans)? Quando usar? Faça um exemplo.

> resposta

2. O que é simulação “ DC operating point” (.0p)? Quando usar? Faça um exemplo.

>resposta

3. Quando usar .trans ou .op no SPICE

>resposta

4. O que faz a diretiva “.step"? Forneça exemplos de utilização.

>resposta

5. O que faz a diretiva “means”? Forneça exemplos de utilização.

>resposta

6. O que é a simulação “DC sweep” (dc)? Quando usar? Faça um exemplo.

>resposta

7. Como simular um circuito em diferentes temperaturas de funcionamento?

>resposta


