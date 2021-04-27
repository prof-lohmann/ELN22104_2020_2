# Atividade 2
Aluno: 
* Guilherme da Costa Franco

## Exercício 1

<b>Resumo sobre Amplificadores Operacionais.</b><br>

<b>a) Faça um resumo em forma de tutorial sobre o os Amplificadores Operacionais. Este
resumo deve responder as seguintes perguntas:</b><br>


### <b>1. O que é o AmpOp?</b><br>
  *Resposta:* Basicamente, um AmpOp é um circuito integrado capaz de amplificar sinais elétricos fracos.</b><br>
  
### <b>2. Mostre os simbolos e as características do AmpOp IDEAL?</b><br>
  *Resposta:* 
  
  ![imagem1](https://user-images.githubusercontent.com/61738767/115885309-392e9a00-a426-11eb-87bb-e7fc54085abf.png)</b><b>
  
<b>Como visto na imagem acima, os terminais VCC e VEE são utilizados para alimentação do componente, usualmente utiliza-se a mesma tensão para ambos (simétricos). Os terminais V+ e V- são utilizados para a entrada do sinal e, por fim, o terminal V0 é saída do componente por onde passa o sinal amplificado.</b><br>  
<b>A fim de obter-se o sinal de saída do AmpOp, utiliza-se a seguinte equação:</b><br>
```
V0 = A(V+ - V-)
```
<b>No qual, **A** representa o **ganho diferencial** ou ganho de malha aberta. Em um AmpOp ideal, este ganho diferencial é infinito.</b><br>
<b>Outra informação que pode ser abstraida da equação é a de que o AmpOp responde apenas à diferença de sinal, descartando, assim, entradas de valores iguais. Este fenômeno recebe o nome de *Rejeição de Modo Comum*. Em um AmpOp ideal, por sua vez, não apresenta corrente na entrada, isto é, sua impedância de entrada é infinita, enquanto que a impedância de saída é nula, para que não haja desvios de corrente quando houver uma carga conectada ao AmpOp.</b><br>

### <b>3. O que significa **Malha Aberta** e **Malha fechada**?</b><br>
  *Resposta:* Malha aberta trata-se de uma configuração de circuito na qual o AmpOp não apresenta realimentação. Algumas características desta configuração são o ganho **A** tendendo ao infinito e a tensão de saída, V0, tendendo aos valores da alimentação VEE ou VCC. Por outro lado, Malha Fechada ocorre quando, na configuração de circuito, o AmpOp apresenta realimentação, geralmente no terminal negativo do componente.</b><br>

### <b>4.Exemplifique como resolver e calcular circuitos com AmpOps em Malha Fechada.</b><br>
<b>*Resposta:* Para circuitos de malha fechada, a equação é similar a de malha aberta, porém depende das características do circuito. Para este tipo de circuito, a saída do AmpOp pode ser obtida a partir da seguinte equação:
```
 V0= G(V+ - V-)
``` 
 <b>No qual G é o ganho diferencial em malha fechada, cuja equação para mensurá-lo varia de acordo com o circuito projetado. Por exemplo, na configuração inversora, o ganho G é dado pela equação:
  ```
  G= -R1/R2
  ```
  ### <b>5.Descreva as principais características das topologias:</b><b>
  <b> a) **Seguidor de Tensão (Buffer)**</b><b>
  
  ![image](https://user-images.githubusercontent.com/61738767/115919005-a22a0800-a44e-11eb-9814-7039a5355704.png)

<b> Nesta configuração, o ganho diferencial é 1, portanto não amplificação do sinal. Dessa forma, o sinal de saída é o mesmo que o sinal de entrada.
   
  <b> b) **Amplificador Inversor**</b><b>
 
 ![image](https://user-images.githubusercontent.com/61738767/115918148-896d2280-a44d-11eb-9a90-09c9408cea89.png)</b><b>
 
 <b> Nesta configuração, o AmpOp desempenha a função de amplificar a saída e invertê-la. </b><b>
 
 <b> c) **Amplificador Não Inversor**

![image](https://user-images.githubusercontent.com/61738767/115919729-9b4fc500-a44f-11eb-8177-618573b68d33.png)</b><b>
 
 <b> Nesta configuração. a tensão de saída assume o mesmo sentido da tensão de entrada, atenuando-a. Esta configuração obedece a seguinte equaçãe:

```
V0 = G * V
```
E o ganho pode ser obtido a partir de:
```
G = 1 + (R2/R1)
```

<b> d) **Amplificador Somador Inversor**
 
 ![image](https://user-images.githubusercontent.com/61738767/115921252-9ee44b80-a451-11eb-978c-464d58f638d3.png)

<b> Esta configuração recebe este nome devido sua saída ser a soma ponderada dos sinais de entrada. Sua equação geral é:
 ```
 V0 = - (Rf/R1 * V1 + Rf/R2 * V2 + ... + Rf/Rn * Vn
 ```
 
 <b> e) **Amplificador Somador Não Inversor**
 
 ![image](https://user-images.githubusercontent.com/61738767/115921996-ace69c00-a452-11eb-92e6-62f1d4ebf82b.png)
 
 <b> f) **Subtrator**

![image](https://user-images.githubusercontent.com/61738767/115924503-2fbd2600-a456-11eb-98a9-492c81fcb7fa.png)

<b> Nesta configuração, há a subtração dos sinais que entram nas saídas inversora e não inversora e joga a tensão resultante na saída amplificado ou atenuado. Esta obedece a seguinte equação (seja R1=R2 e R3=R4):
 ```
 V0 = (V2-V1) * (R3/R1)
 ```
 E o ganho pode ser obtido a partir de:
 ```
 G = (R3/R1)
 ```
 
 <b> g) **Amplificador de instrumentação**
 
 ![image](https://user-images.githubusercontent.com/61738767/116251167-cb93ae00-a744-11eb-8559-0a807dc25b74.png)

<b>Nesta configuração, há um incremento quanto ao incoveniente do Amplificador Subtrator no que diz respeito entre o ganho de tensão e a resistência de entrada vista por cada uma das fontes de sinal. A saída do circuito é dada pela sequinte equação:
 ```
 V0 = (V1-V2)(1+2Rx/R)R4/R3
 ```
 ### 6. Explique o efeito do ganho em MALHA ABERTA FINITO, para as topologias Amplificador Inversor e Amplificador não inversor
<b>*Resposta:* Em termos ideais, o ganho de um AmpOp em malha aberta é infinito. No entanto, na prática, seu ganho é finito com seu valor bem elevado. Com isso, deve-se considerar os diferente fatores que influenciam no ganho para as diferente topologias de circuito, como por exemplo tensão de offset, corrente de polarização, tensão de modo comum e outros.<b></b>
 
<b>Considerando um ganho finito, a equação para o sinal de saída da topologia inversora segue a seguinte forma:
 ```
 G = v0/v1 = (-R2/R1)/ 1 + (1 + R2/R1)/A
 ```
 <b>Para a topologia não inversora, tem-se:
  ```
  G = v0/v1 = (1 +  R2/R1)/ (1 + (1 + (R2/R1))/A)
  ```

### 7.Explique o que é a tensão de modo comum(VCM) e quais os efeitos desta tensão nas topologias estudadas.
<b>*Resposta:* Em linhas gerais, VCM é a tensão média entre os sinais de entrada do AmpOp multiplicado por um ganho de modo comum. Idealmente, VCM é zero, porém, na prática, isso não ocorre, o que ocasiona no surgimento de um acréscimo não desejado de tensão no sinal de saída.
 
<b> A tensão de saída nesta ocorrência obedece a seguinte equação:
 ```
 V0 = A*(V+ - V-) + ACM(VCM)
 ```
 
 ### 8.O que é **CMRR**?
 <b>*Resposta:* CMRR é o acrônimo para Common Mode Rejection Ratio ou Relação de Rejeição em Modo Comum. Trata-se de uma característica dos amplificadores operacionais. Quando dois sinais da mesma amplitude, frequência e fase são aplicados às entradas (inversora e não inversora) de um operacional eles devem se cancelar e nenhuma saída deve ocorrer.
 
 ### 9.Utilizando o Amplificador Subtrator com ganho 1000V/V, demonstre o efeito da tensão de modo comum (VCM), indicando:
 
 ### 10.Faça um resumo explicando as limitações de tensão de entrada e saída de um AmpOp. De exemplos, utiliza-se valores de datasheet.
 
 <b>a) Defina o que é um AmpOp Rail-to-rail.
 *Resposta:* Em linhas gerais, trata-se de um Amplificador Operacional cuja tensão na saída se aproxima dos valores de tensões de sua alimentação.
 
 ### 11.O que é tensão de offset? Como calcular o efeito resultante na tensão de saída de um amplificador inversor?
 *Resposta:* O offset é definido como uma tensão residual que aparece na saída do AmpOp quando as entradas inversora e não inversora são iguais a 0. Esta tensão residual pode ser prejudicial em aplicações de instrumentação, influenciando diretamente na precisão dos amplificadores.
 
 Calcula-se o efeito resultante da saída de um aplificador inversor simples utilizando a seguinte equação:
 ```
 V0= -(R2/R1)V1 + (1 + R2/R1)Vos
 ```
 
 ### 12.Como minimizar o efeito da tensão de offset?
 *Resposta:* Além dos terminais de compensação de tensão de desvio localizados no próprio AmpOp, pode-se utilizar componentes passivos como resistores e potênciometros.
 
 ### 13.O que é a variação da tensão de offset pela temperatura?
 *Resposta:* Esta variação quer dizer que o valor de offset varia de acordo com a mudança de temperatura.
 
 <b> a) Como verificar esse parâmetro no datasheet?
 *Resposta:* Existe uma seção do datasheet no qual são apresentadas tabelas de operação do componente em questão, junto delas valores como valor típico e outro que é dado junto com uma faixa de temperatura.
 
 ### 14.O que são as correntes de polarização(Ibias) de AmpOp?
<b> *Resposta:* Independentemente do facto de os amplificadores operacionais apresentarem uma resistência de entrada não infinita, característica que se associa apenas aos sinais dinâmicos aplicados, a natureza própria dos transístores obriga à existência de correntes não nulas através dos terminais de entrada, IB+ e IB-, designadas correntes de polarização, as quais, por ação do desemparelhamento inexorável entre componentes, são, também, distintas entre si (estas correntes associam-se à corrente na base dos transístores bipolares, e às correstes de fuga ou de saturação inversa nos transístores de efeito de campo).
 
 <b> a)Como minimizar o efeito destas correntes? Descreva as aproximações e os possíveis circuitos para mitigar o problema.
 <b> *Resposta:* A existência das correntes de polarização obriga à utilização de componentes externos adicionais, tipicamente resistências, como forma de compensar os erros de tensão induzidos na saída.
