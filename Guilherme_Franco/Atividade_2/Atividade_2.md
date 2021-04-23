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
  <b> a) **Seguidor de Tensão (Buffer)**
   
  <b> b) **Amplificador Inversor**</b><b>
 
 ![image](https://user-images.githubusercontent.com/61738767/115918148-896d2280-a44d-11eb-9a90-09c9408cea89.png)</b><b>
 
 <b> Nesta configuração, o AmpOp desempenha a função de amplificar a saída e invertê-la. </b><b>
