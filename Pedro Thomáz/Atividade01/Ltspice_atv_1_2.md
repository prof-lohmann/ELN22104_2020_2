***************************************** QUESTÃO NÚMERO 5 - LETRA A **********************************************

#1 - É um arquivo de texto que descreve as conexões entre os componentes utilizados e seu nós.

#2 - Antes de tudo é nomeado o projeto, por exemplo(Divisor reistivo, para servir como uma descrição do que está sendo feito) 
e depois é preciso numerar todos os nós do circuito e depois declarar os componentes usados, o qual é identificado 
por uma letra(Um R, por exemplo para um resistor) e o número dos nós que está conectado, por último é descrito suas propriedades.
Ex: R1 1 0  100 --> Resistor 1 ligado entre o terra(Nó 0, referência) e o nó 1 com valor de 100 ohms.

#3 - Como no exemplo anterior para o resistor, podemos generalizar: <nome-do-elemento> <nó+> <nó-> <valor>
Então por exemplo para uma fonte --> V1 0 1 10 --> Fonte V1 entre o terra e o nó  1 com uma tensão de 10 volts

#4 - É a identificação de um fio, portanto você não precisará fazer a conexão de um componente a outro, somente colocar
o fio saindo do componente e nomear a label. É util para projetos grandes, a fim de não ficar um amontoado de fios na tela.

#5 - Resistor, capacitor, diodo, indutor, fonte de tensão(voltage)...

#6 - É a inclusão de uma descrição(parâmetros) de um componente desejado não listado na biblioteca à um componente genérico.
É como se sobrescrevesse o componente genérico e este passa a ter seu nome e suas características. Ex: adicionar a descrição
do modelo spice para o lm741 usando um ampop genérico, se muda o nome do ampop genérico para o nome do circuito lm741 e 
assim, o ampop genérico terá seus parâmetros

#7 - Procura-se o arquivo do modelo Spice do componente desejado(Sua descrição), copia-se e se cola em um arquivo de texto 
e se salva como um arquivo com extensão .lib e depois se adiciona este arquivo na pasta de componentes do Ltspice. 
Já com o programa aberto, adiciona o texto .lib com o nome do componente e por fim, altera-se o nome do componente genérico 
pelo nome do componente e assim está completo. O genérico será referenciado como este incuso.
