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

#### Aqui está uma lista de algumas teclas de atalho para criar seu esquema:

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


#### Execucao de Simulacoes e Sinais Senoidais:

Para rodar a simulacao do circuito feito, basta clicar no botao Run, como na imagem a baixo:

![Imagem 4](https://user-images.githubusercontent.com/12564754/99699495-bf5a4500-2a70-11eb-82fc-5a3271268024.PNG)

Note que aparecera uma janela para inserir as informacoes de como sera realizada a execucao. Apos configurar e mandar executar a simulacao, uma nova janela com o título “Draft1.raw” se abrirá (imagem abaixo). Nela serão mostrados os resultados da simulação.

![Imagem 5](https://user-images.githubusercontent.com/12564754/99699525-cbde9d80-2a70-11eb-83e0-234eb91abc01.PNG)

A partir de agora, se aproximarmos o mouse de alguma linha ou componente, aparecesera uma ponta de medida de tensao ou corrente. Se clicar sobre a linha ou componente, automamticamente aparecera o sinal na janela com o título “Draft1.raw”.

### Topicos avancados sobre o LTSpice:

### Questões Propostas (a):

1. O que é NETLIST?
> O NETLIST é a organizacao em lista dos componentes de um circuito e dos nós presentes em formato de texto. Ela é utilizada para aprender sobre a sintaxe e simulação do SPICE. Também pode ajudar na identificação de erros de simulação e problemas de convergência.

2. Como descrever o NETLIST de um circuito?

> O netlist pode ser gerado pelo programa EDFIL, a partir do diagrama esquemático. Primeira linha: Comentário (o editor EDFIL coloca o número de nós nesta linha).Linhas seguintes: Descrição do circuito, com um elemento por linha. A primeira letra determina o tipo de elemento. Exemplo para visualizacao está na imagem abaixo:
>
> ![imagem 6](https://user-images.githubusercontent.com/12564754/99992759-89310400-2d95-11eb-942f-26aea9776421.PNG)

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

> Biblioteca de componentes passivos (como R, L, C)e biblioteca de componentes lineares.

6. O que é um SUBCKIT? Exemplo.

> É a criacao automaticamente de um símbolo para um modelo customizado, ou você pode associar um subcircuito a um símbolo intrínseco LTspice, desde que o modelo .SUBCKT desejado e o símbolo intrínseco compartilhem uma lista de rede de pinos / portas de idêntica ordem.
> Exemplo de SUBCKT que descreve um AmpOp::
>```
> .SUBCKT LM324    1 2 3 4 5
> *
>  C1   11 12 5.544E-12
>  C2    6  7 20.00E-12
>  DC    5 53 DX
>  DE   54  5 DX
>  DLP  90 91 DX
>  DLN  92 90 DX
>  DP    4  3 DX
>  EGND 99  0 POLY(2) (3,0) (4,0) 0 .5 .5
>  FB    7 99 POLY(5) VB VC VE VLP VLN 0 15.91E6 -20E6 20E6 20E6 -20E6
>  GA    6  0 11 12 125.7E-6
>  GCM   0  6 10 99 7.067E-9
>  IEE   3 10 DC 10.04E-6
>  HLIM 90  0 VLIM 1K
>  Q1   11  2 13 QX
>  Q2   12  1 14 QX
>  R2    6  9 100.0E3
>  RC1   4 11 7.957E3
>  RC2   4 12 7.957E3
>  RE1  13 10 2.773E3
>  RE2  14 10 2.773E3
>  REE  10 99 19.92E6
>  RO1   8  5 50
>  RO2   7 99 50
>  RP    3  4 30.31E3
>  VB    9  0 DC 0
>  VC 3 53 DC 2.100
>  VE   54  4 DC .6
>  VLIM  7  8 DC 0
>  VLP  91  0 DC 40
>  VLN   0 92 DC 40
> .MODEL DX D(IS=800.0E-18)
> .MODEL QX PNP(IS=800.0E-18 BF=250)
> .ENDS
>```

7. Como incluir novos modelos de componentes em um simulador Spice.

> É possivel baixar um novo componente em repositorios online e anexar na pasta do projeto. (continuar) 

### Questões Propostas (b):

 l. O que é simulação transiente (trans)? Quando usar? Faça um exemplo.

> A simulação transiente é uma simulação não linear no domínio de tempo. É possivel a partir desta funcionalidade defenir o tempo de execucao da simulacao. 
> Exemplo:
>
> ![imagem 7](https://user-images.githubusercontent.com/12564754/99994752-30169f80-2d98-11eb-9460-90c390ec5925.png)

2. O que é simulação “ DC operating point” (.0p)? Quando usar? Faça um exemplo.

> É a opcao para simulacao de circuitos de corrente continua, ideal para circuitos que nao tenham dependencia de transicao de tempo. Exemplo:
> 
> ![imagem 8](https://user-images.githubusercontent.com/12564754/99996298-4aea1380-2d9a-11eb-8fa9-54717d51f724.png)

3. Quando usar .trans ou .op no SPICE

> O transiente (.trans) é recomendado para circuitos que possuem dependencia temporal. Ponto de operação (.op) é recomendado para circuito sem dependencia tempora.

4. O que faz a diretiva “.step"? Forneça exemplos de utilização.

> O comando .step repete uma análise de circuito alterando o parâmetro de um componente em cada repetição. Exemplo a baixo:
>
>![imagem 9](https://user-images.githubusercontent.com/12564754/100117971-218dbe00-2e54-11eb-8355-f692dac39657.png)
>
> Para que o componente se torne uma variavel a ser analisada com valores variaveis deve-se clicar nela (ctrl + botao esquerdo mouse) e nomea-la com a variavel desejada.
>
>![imagem 10](https://user-images.githubusercontent.com/12564754/100118306-77fafc80-2e54-11eb-966d-f7191d6919a8.png)
>
> Configure a variacao desejada escrevendo da seguinte forma em forma de passo:
>``` .step param (variavel) (valor inicial) (valor final) (passo de transição)```

5. O que faz a diretiva “means”? Forneça exemplos de utilização.

> A diretiva .means serve para analizar um parametro especifico dentro da analise do circuito. Ela possui os seguintes parametros como possibilidade de analise:
``` 
 A seguinte sintaxe é usada:

.MEAS[SURE] [AC|DC|OP|TRAN|TF|NOISE] <name> [<FIND|DERIV|PARAM> <expr>] [WHEN <expr> | AT=<expr>]] [TD=<val1>] [<RISE|FALL|CROSS>=[<count1>|LAST]]```

>Exemplo de utilizacao: Analise do valor de tensao do resistor R1 em t=30m
>
>![imagem 13](https://user-images.githubusercontent.com/12564754/100128996-bba73380-2e5f-11eb-8a62-53509365fa5f.png)


6. O que é a simulação “DC sweep” (dc)? Quando usar? Faça um exemplo.

> O DC Sweep funciona de forma semelhante ao .step, o simulador repete a análise do circuito variando a tensão das fontes em corrente contínua do circuito. Este tipo de análise pode ser usado para avaliar o comportamento de um transistor
>Exemplo de utilizacao:
>
>![imagem 12](https://user-images.githubusercontent.com/12564754/100122620-5865d300-2e58-11eb-9777-f2597d13af4c.png)

7. Como simular um circuito em diferentes temperaturas de funcionamento?

>Para simular um circuito em diferentes temperaturas, basta utilizar a diretiva .step temp conforme as imagens abaixo:
>
>![imagem 11](https://user-images.githubusercontent.com/12564754/100120252-8518eb00-2e56-11eb-95d4-327972aa7344.png)
>
> Configure a variacao desejada escrevendo da seguinte forma em formato de lista:
>``` .step temp list (valor inicial) (proximo valor) ... (valor final)```

