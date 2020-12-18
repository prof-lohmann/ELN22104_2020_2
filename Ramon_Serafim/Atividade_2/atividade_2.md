
 Curso de Engenharia Eletrônica

Unidade Curricular: Eletrônica I

Professor: Daniel Lohmann

Aluno: Ramon Busiquia Serafim

 

# Atividade 2

 

1. ##### O que é o **AmpOp**?

   ​		Amplificador Operacional é um Circuito Integrado (CI), capaz de manusear o sinal de entrada e realizar operações matemáticas como soma, subtração, multiplicação. Apesar de parecer um componente simples por ter uma estrutura externa simples, internamente possui uma composição de muitos componentes como resistores, capacitores e transistores.
<br />

2. ##### Simbolos e as características do **AmpOp IDEAL**?

 
Correntes nulas nas entradas V+ e V- . Impedância de entrada do Amp Op é supostamente infinita;

Impedância de saída do Amp Op ideal é supostamente zero;

Como o amplificador responde a diferença de sinais, caso o v1=v2= 1V, a saída será (teoricamente) zero, sem oscilações.
<br />
<br />


3. ##### O que significa **Malha Aberta** e **Malha Fechada**?

   ​	A ação de controle da malha aberta independe da saída, já na malha fechada é o contrário, o controle depende da saída sendo feita por realimentação do sistema.
<br />
<br />


4. ##### Exemplifique como resolver e calcular circuitos com AmpOps em Malha Fechada.

   ​	Para resolver e calcular os circuitos em malha fechada, análise nodal é a melhor forma, pois a entrada do AmpOp é teoricamente zero, portanto, toda corrente passaria para o resistor de realimentação. Muitos circuitos já foram simplificados possuindo suas próprias topologias e formulas deduzida. Caso ocorra de ter 2 fontes ou mais, é possível separar por analise de sobreposição facilitando o cálculo.
<br />
<br />

5. ##### Descreva as principais características das topologias: 

 

###### a) Seguidor de Tensão (Buffer)
 
 

FIGURA 2.12 PAG 48



​      Segue o sinal de entrada, utilizado em situações que o ganho da potencia importa. Com a resistência de entrada muito grande e a de saída muito baixa é “isolar” partes do circuito, como uma fonte de tensão e uma carga sem haver atenuação no sinal. Possui ganho unitário.

<br />

###### b) Amplificador Inversor

  


FIGURA 2.5 PAG 42


​      Sinal de entrada v1 é colocado na entrada inversora, um resistor fica entre a fonte e o AmpOp, possui realimentação negativa. O ganho nesta topologia é negativo, invertendo o sinal.

<br />

<a href="https://www.codecogs.com/eqnedit.php?latex=G=\frac{Vo}{Vi}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?G=\frac{Vo}{Vi}" title="G=\frac{Vo}{Vi}" /></a>
<br />

###### c) Amplificador Não Inversor



 FIGURA 2.12 PAG 48



​       Sinal de entrada v1 é aplicado diretamente no terminal positivo do AmpOp, enquanto o outro terminal é conectado ao terra com realimentação negativa. O ganho nesta configuração é positivo, não invertendo o sinal. 

<br />
<a href="https://www.codecogs.com/eqnedit.php?latex=G=\left(1&plus;\frac{R2}{R1}\right)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?G=\left(1&plus;\frac{R2}{R1}\right)" title="G=\left(1+\frac{R2}{R1}\right)" /></a>
<br />

###### d) Amplificador Somador Inversor

 

FIGURA 2.10 PAG 47

 

​      Possui realimentação negativa, vários sinais de entrada com um resistor correspondente os quais estão conectados ao terminal inversor do AmpOp. A entrada não inversora é aterrada.

              
<br />
<a href="https://www.codecogs.com/eqnedit.php?latex=Vo=-\left(\frac{Rf}{R1}V1\:&plus;\:\frac{Rf}{R2}V2\:&plus;\:\cdot&space;\cdot&space;\cdot&space;\:&plus;\:\frac{Rf}{Rn}Vn\right)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?Vo=-\left(\frac{Rf}{R1}V1\:&plus;\:\frac{Rf}{R2}V2\:&plus;\:\cdot&space;\cdot&space;\cdot&space;\:&plus;\:\frac{Rf}{Rn}Vn\right)" title="Vo=-\left(\frac{Rf}{R1}V1\:+\:\frac{Rf}{R2}V2\:+\:\cdot \cdot \cdot \:+\:\frac{Rf}{Rn}Vn\right)" /></a>
<br />
        

###### e) Amplificador Somador Não Inversor





​		Possui quase a mesma topologia do amplificador somador inversor, é invertido as conexões de entrada onde se localiza os sinais troca a entrada inversora pela não inversora. Ainda possui realimentação negativa.


<br />
<a href="https://www.codecogs.com/eqnedit.php?latex=Vo=\left(1&plus;\frac{Rf}{R}\right)\left(\frac{\frac{V1}{R1}&plus;\frac{V2}{R2}&plus;\cdot&space;\cdot&space;\cdot&space;&plus;\frac{Vn}{Rn}}{\frac{1}{R1}&plus;\frac{1}{R2}&plus;\cdot&space;\cdot&space;\cdot&space;&plus;\frac{1}{Rn}}\right)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?Vo=\left(1&plus;\frac{Rf}{R}\right)\left(\frac{\frac{V1}{R1}&plus;\frac{V2}{R2}&plus;\cdot&space;\cdot&space;\cdot&space;&plus;\frac{Vn}{Rn}}{\frac{1}{R1}&plus;\frac{1}{R2}&plus;\cdot&space;\cdot&space;\cdot&space;&plus;\frac{1}{Rn}}\right)" title="Vo=\left(1+\frac{Rf}{R}\right)\left(\frac{\frac{V1}{R1}+\frac{V2}{R2}+\cdot \cdot \cdot +\frac{Vn}{Rn}}{\frac{1}{R1}+\frac{1}{R2}+\cdot \cdot \cdot +\frac{1}{Rn}}\right)" /></a>
<br />


###### f) Subtrator





Responde à diferença de dois sinais que aplicados em suas entradas e idealmente rejeita sinais ue sao comuns às duas entradas. Para encontrar o valor na saída é feito sobreposição de fontes para encontrar o resultado.


<br />
<a href="https://www.codecogs.com/eqnedit.php?latex=Vo=GdVd\:&plus;GcmVcm" target="_blank"><img src="https://latex.codecogs.com/gif.latex?Vo=GdVd\:&plus;GcmVcm" title="Vo=GdVd\:+GcmVcm" /></a>
<br />


###### g) Amplificador de Instrumentação

 
<br />
<br /> 

6. ##### Explique o efeito do ganho em MALHA ABERTA FINITO, para as topologias Amplificador Inversor e Amplificador não inversor.

 

PAG 43 - 44

 

###### a) Exemplifique com circuitos com ganhos em malha fechada elevado (Ex. 1000V/V e -1000V/V) e com ganhos menores (Ex. 10V/V e -10V/V ), faça a comparação com erros percentuais e utilize uma variação de ganho em malha aberta entre 120dB e 20dB.

 

b) Dica veja o problema 2.20 pg 83 do livro texto.
<br />
<br /> 

7. ##### Explique o que é a tensão de modo comum (VCM) e quais os efeitos desta tensão nas topologias estudadas.

​      É a diferença potencial entre os sinais de sua entrada, saída inversora e não inversora. Em alguns circuitos pode ocasionar problemas, faixa de tensão do modo comum e a taxa de rejeição do modo comum (CMRR) são descritas para que possíveis erros de medidas não ocorram. A faixa de tensão do modo comum é definida como a máxima variação de tensão permitida em cada entrada. Caso não esteja dentro da faixa não apenas pode causar um erro de medição, mas também em possível dano aos componentes circuito.
<br />
<br /> 

8. ##### O que é CMRR?

A eficácia de um amplificador diferencial é medida pelo grau de sua rejeição a sinais de modo comum, caso o mesmo sinal de mesma amplitude, frequência e fase sejam colocados em ambas entradas. Normalmente quantificado por uma medida conhecida como razão de rejeição de modo comum (CMRR). Teoricamente esse diferencial deveria ser zero, mas na prática ainda é visto um sinal. 

Valores altos de CMRR podem ocasionar em um erro grande na medida no sinal de saída. Rejeição do modo comum pode ser medido desta forma:

 
<br />
<a href="https://www.codecogs.com/eqnedit.php?latex=CMRR=20\log&space;_{&space;}\left(\frac{\left|Ad\right|}{\left|Acm\right|}\right)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?CMRR=20\log&space;_{&space;}\left(\frac{\left|Ad\right|}{\left|Acm\right|}\right)" title="CMRR=20\log _{ }\left(\frac{\left|Ad\right|}{\left|Acm\right|}\right)" /></a>
<br /> 

9. ##### Utilizando o Amplificador Subtrator com ganho 1000V/V, demonstre o efeito da tensão de modo comum (VCM), indicando: 

###### a) o impacto na tensão de saída com relação a tolerância dos resistores no circuito; 

###### b) Qual erro na tensão de saída com relação CMRR do AmpOp. 

###### c) Dica de exemplos com valores diferentes de tensão de modo comum (VCM) . Faça o mesmo circuito com resistores com tolerâncias bem distintas, ex. 1% e 5%.
<br />
<br /> 

10. ##### Faça um resumo explicando as limitações de tensão de entrada e saída de um AmpOp. De exemplos, utiliza-se valores de datasheet. 

    ​	Afim de evitar distorção e/ou erros de leitura, existe um limite de tensão na entrada de acordo com a sua alimentação. Um exemplo é o LM324, seus limites de tensão de alimentação vão de 3 a 26V, mas para tensão de entrada vai de 0 a VCC-2V. Caso alimente um AmpOp com ±15V, sua saída vai ser saturada em ±13V.

 





###### a) Defina o que é um AmpOp Rail-to-rail.

Um amplificador preciso cuja tensão na saída tende alcançar o mesmo nível que as tensões de alimentação do AmpOp. A maioria dos amplificadores possui uma saída limitada entre a alimentação negativa e a positiva a partir de 0,2V.
<br />
<br /> 

11. ##### O que é tensão de *offset*? Como calcular o efeito resultante na tensão de saída de um amplificador inversor?

​      É um desequilíbrio nas entradas do AmpOp, devido ao alto ganho CC. Esse valor é fornecido em datasheets. Nos circuitos é visto como uma fonte de tensão na entrada não inversora do circuito.

​      Para calcular o efeito sobre a tensão de saída pelo teorema de superposição, anulando as fontes uma por uma e vendo seus efeitos no sinal de saída. Exemplo mostrado abaixo.

 
<br />
<a href="https://www.codecogs.com/eqnedit.php?latex=Vo=Vos\:\left[1&plus;\frac{R2}{R1}\right]" target="_blank"><img src="https://latex.codecogs.com/gif.latex?Vo=Vos\:\left[1&plus;\frac{R2}{R1}\right]" title="Vo=Vos\:\left[1+\frac{R2}{R1}\right]" /></a>
<br />
FIGURA 2.29  PAG53
<br />
<br />

12. ##### Como minimizar o efeito da tensão de *offset*?

​      É possível acoplar um capacitor na entrada inversora, mas somente em aplicações que não exijam uma amplificação de sinais cc ou frequências muitos baixas ou procurando outro AmpOp com tensão de offset menor.
<br />
<br />

13. ##### O que é a variação da tensão de *offset* pela temperatura?

    ​	Alguns circuitos podem ser postos em temperaturas extremas como uma fundição ou um frigorifico, a tensão de offset pode ser afetada pela temperatura mudando o valor para os circuitos. Softwares podem simular essas diferenças.

###### a)   Como verificar esse parâmetro no *datasheet*?

É um dos parâmetros mais fáceis de visualizar no datasheet, pois a unidade de medida referida a esse parâmetro é V/**°**C.
<br />
<br />

14. ##### O que são as **correntes de polarização(Ibias)** de AmpOp? 

    ​	Para o AmpOp operar, deve ter uma corrente para fazer o funcionamento dos componentes como transistores, uma corrente medida com o AmpOp em repouso. Correntes de polarização de entrada significa fontes de correntes cc ligadas ao AmpOp. O fabricantes especifica o valor média de Ibias, bem como sua diferença, corrente de offset.

###### a)  Como minimizar o efeito destas correntes? Descreva as aproximações e os possíveis circuitos para mitigar o problema.

​		Introduzir um resistor em série com o terminal de entrada inversora. Para o sinal o resistor é desprezível. Como visto na figura abaixo, o resitor em série deve ser igual à associação em paralelo de R1 e R2. Outra forma de minimizar o efeito caso o resistor não seja suficiente é procurando outro AmpOp com corrente de *offset* menor.

 

FIGURA 2.34 PAG 66

 

###### b)  Descreva a corrente de offset na polarização dos AmpOp.

​		É a diferença entre as correntes de polarização de entrada, dada por

<br />
 <a href="https://www.codecogs.com/eqnedit.php?latex=Ios=\left|Ib1-Ib2\right|" target="_blank"><img src="https://latex.codecogs.com/gif.latex?Ios=\left|Ib1-Ib2\right|" title="Ios=\left|Ib1-Ib2\right|" /></a>
<br />
