<table align="center"><tr><td align="center" width="9999"><br>
<img src="../../Imagens/logoifsc.png" align="center" width="150" alt="Logo IFSC">

# Atividade 2

<b>Instituto Federal de Educação, Ciência e Tecnologia de Santa Catarina<br>
Campus Florianópolis<br>
Departamento Acadêmico de Eletrônica<br>
Eletrônica I</b>

*Jonathan Chrysostomo Cabral Bonette*
</td></tr></table>

<b>a) Faça um resumo em forma de tutorial sobre o os Amplificadores Operacionais. Este resumo deve responder as seguintes perguntas:<br></b><br>
<b>1. O que é o AmpOp?</b><br>

*O amplificador operacional, também chamado por alguns de amp-op, nada mais é do que um circuito integrado (CI), capaz de amplificar um sinal de entrada e como próprio nome sugere, o amplificador operacional também é capaz de realizar operações matemáticas, como por exemplo soma, subtração, derivação. integração e multiplicação.*

---

<b>2. Mostre os simbolos e as características do AmpOp IDEAL?</b><br>
*Um AmpOp ideal possui cinco terminais, dois de entrada (inversora (-) e não inversora (+)), dois de alimentação (fonte (+Vcc) e (-Vcc) e um de saída (Vo).*

---

<b>3. O que significa Malha Aberta e Malha Fechada?</b><br>
*O modo de Amplificador Operacional sem realimentação é conhecido como operação em malha aberta, por utilizar o ganho do amplificador que estipulado pelo fabricante, ou seja, não é possível controlar o ganho do amplificador. Este tipo de operação é comumente usado em circuitos comparadores.*<br>
*O modo de realimentação positiva é uma operação em malha fechada, quando a entrada positiva é ligada na saída do amplificador operacional, através de RF. O ganho do amplificador operacional é obtido através de que está projetando e possui como desvantagem uma instabilidade ao circuito, por isso é muito aplicado em circuitos osciladores.*

---

<b>4. Exemplifique como resolver e calcular circuitos com AmpOps em Malha Fechada.</b><br>

<b>Amplificador Inversor</b>
<p align="center"><img src="../../Imagens/Atividade 2/mf_inv - exemplo.png" align="center" width="500"><br></p>

`Como não temos corrente passando (em vermelho) para o ampop, então a corrente que passa pelo` **Rf** `é a mesma que passa em` **R1** `(trajetória em azul), logo` **If = I1**`,`
`também podemos observar que pelo comportamento do circuito, o valor do terra do ponto não inversor passará para o ponto inversor (em amarelo),`
`portanto utilizando o método de nós podemos análisar que `**If = (Vo - 0)/Rf**`, da mesma forma,` **I1 = (0 - V1)/R1**` e como, `**If = I1**` substituindo e colocando Vo em evidência, temos que `**Vo = (-Rf/R1)V1**`. sendo o ganho `**G = (-Rf/R1)**`.`


<b>Amplificador Não-Inversor</b>
<p align="center"><img src="../../Imagens/Atividade 2/mf_ninv - exemplo.png" align="center" width="500"><br></p>

`Como não temos corrente passando (em vermelho) para o ampop, então a corrente que passa pelo` **Rf** `é a mesma que passa em` **R1** `(trajetória em azul), logo` **If = I1**`,`
`também podemos observar que pelo comportamento do circuito, o valor do` **V1**` do ponto não inversor passará para o ponto inversor (em amarelo),`
`portanto utilizando o método de nós podemos análisar que `**If = (Vo - V1)/Rf**`, da mesma forma,` **I1 = (V1 - 0)/R1**` e como, `**If = I1**` substituindo e colocando Vo em evidência, temos que `**Vo = (1+(Rf/R1))V1**`. sendo o ganho `**G = (1+(Rf/R1))**`.`

---

<b>5. Descreva as principais características das topologias:</b>

<b>a) Seguidor de Tensão (Buffer)</b><br>
<p align="center"><img src="../../Imagens/Atividade 2/buffer.png" align="center" width="500"><br></p>

*A ideia de um buffer, ou seguidor de tensão, é a de um circuito que apresente na saída exatamente a entrada aplicada*<br><br>

<b>b) Amplificador Inversor</b><br>
<p align="center"><img src="../../Imagens/Atividade 2/mf_inv.png" align="center" width="500"><br></p>

*Este amplificador é chamado de inversor porque, além de amplificar o sinal de entrada, o sinal de saída possui polaridade invertida, ou seja, valores positivos na entrada se tornam valores negativos na saída e vice-versa.*<br><br>

<b>c) Amplificador Não Inversor</b><br>
<p align="center"><img src="../../Imagens/Atividade 2/mf_ninv.png" align="center" width="500"><br></p>

*Este amplificador é chamado de não-inversor porque o sinal de saída possui mesma polaridade do sinal de entrada*<br><br>

<b>d) Amplificador Somador Inversor</b><br>
<p align="center"><img src="../../Imagens/Atividade 2/somador.png" align="center" width="500"><br></p>

*O amplificador somador é um circuito com AMPOP que permite realizar a soma de dois ou mais sinais.*<br><br>

<b>e) Amplificador Somador Não Inversor</b><br>
<p align="center"><img src="../../Imagens/Atividade 2/somador ninv.png" align="center" width="500"><br></p>

*A diferença entre o somador inversor é de que as tensões de entrada serão aplicadas ao terminal inversor do ampop.*<br><br>

<b>f) Subtrator</b><br>
<p align="center"><img src="../../Imagens/Atividade 2/sub.png" align="center" width="500"><br></p>

*O amplificador subtrator realiza um resultado na saída de uma tensão igual à diferença entre os sinais aplicados, multiplicada por um ganho (G).*<br><br>

<b>g) Amplificador de Instrumentação</b>
<p align="center"><img src="../../Imagens/Atividade 2/instrumentação.png" align="center" width="500"><br></p>

*Os amplificadores de instrumentação são conhecidos por terem uma entrada diferencial e uma elevada impedância de entrada.*<br>

---

<b>6. Explique o efeito do ganho em MALHA ABERTA FINITO, para as topologias Amplificador Inversor e Amplificador não inversor.</b><br>
<p align="center"><img src="../../Imagens/Atividade 2/ex6 inversor.png" align="center" width="500"><br></p>

`A impedância de entrada infinita do amplificador operacional força a corrente `**I1** `a fluir inteiramente através de `**R2**`. A tensão de saída` **Vo**` pode, portanto, ser determinada a partir das equações que já vimos anteriormente, fazendo por nós, temos que,` **I1 = ((V1 - (-Vo/A))/R1)** `e como,` **Vo = -Vo/A - I1xR2**,` sendo nosso ganho definido por` **G = Vo/V1**`, substituindo e isolando, temos que `**G = (-R2/R1)/(1 + (1 + R2/R1)/A)**`. Notamos que conforme A se aproxima de ∞, G se aproxima do valor ideal de `**-R2/R1**`. Além disso, a partir da figura, vemos que conforme A se aproxima de ∞, a tensão no terminal de entrada inversor se aproxima de` **zero**`.`

<p align="center"><img src="../../Imagens/Atividade 2/ex6 ninversor.png" align="center" width="500"><br></p>

`Como fizemos para a configuração de inversão, agora consideramos o efeito do ganho de malha aberta A do amp op finito no ganho da configuração de não inversão. Supondo que o amplificador operacional seja ideal, resumindo as operações, e usando as mesmas análises por nós, chegamos que `**G = (1 + (R2/R1))/(1 + ((1 + R2/R1)/A))**`. Observamos que o denominador é idêntico ao da configuração inversora. Isso não é coincidência, pois é a prova de que ambas as configurações de inversão e não inversora têm o mesmo loop, que pode ser facilmente visto se a fonte do sinal de entrada for eliminada (ou seja, em curto-circuito). Os numeradores, no entanto, são diferentes, pois o numerador fornece o ganho de malha fechada ideal ou nominal (para a configuração inversora e para a configuração não inversora). Finalmente, notamos que a expressão de ganho na figura se reduz ao valor ideal para A = ∞.`

<b>a) Exemplifique com circuitos com ganhos em malha fechada elevado (Ex. 1000V/Ve -1000V/V) e com ganhos menores (Ex. 10V/V e -10V/V), faça a comparação com erros percentuais e utilize uma variação de ganho em malha aberta entre 120dB e 20dB.<br></b>

<b>Inversor</b>
|Av | G (em módulo) | Erro (dado pela expressão do livro) | 
| :------------: | :------------: | :------------: |
| 10000  | 909 | 9,1 |
| -10000 | 90,83 | 90,9 |
| 10 | 9,98 | 0,2 |
| -10 |  9,01 | 9,8 |

<b>Não-Inversor</b>
|Av | G (em módulo) | Erro (dado pela expressão do livro) | 
| :------------: | :------------: | :------------: |
| 10000 | 909 | 9,1 |
| -10000 | 90,88 | 90,9 |
| 10 | 9,9 | 0,12 |
| -10 | 9,09 | 9,3 |

<b>b) Dica veja o problema 2.20 pg 83 do livro texto.</b><br>

---

<b>7. Explique o que é a tensão de modo comum(VCM) e quais os efeitos desta tensão nas topologias estudadas</b><br>
*A tensão comum é basicamente a tensão média nos pinos de entrada inversora e não inversora. Se a tensão do modo comum ficar muito alta ou muito baixa, as entradas serão fechadas para baixo e a operação adequada irá parar.*<br>
 
 ---
 
<b>8. O que é CMRR?</b><br>
*CMRR trata-se de uma característica dos amplificadores operacionais. Quando dois sinais da mesma amplitude, freqüência e fase são aplicados às entradas (inversora e não inversora) de um operacional eles devem se cancelar e nenhuma saída deve ocorrer.*<br>
 
 ---
 

<b>9. Utilizando o Amplificador Subtrator com ganho 1000V/V, demonstre o efeito da tensão de modo comum (VCM), indicando:</b><br>
<b>a) o impacto na tensão de saída com relação a tolerância dos resistores no circuito</b><br>

**Ampop: OPA2991 da Texas instruments.**

*Olhando seu datasheet vimos qual a faixa de operação para as tensões de alimentação e a tensão de modo comum (Vcm).*

<p align="center"><img src="../../Imagens/Atividade 2/9.1.png" align="center"><br></p>

*O circuito foi montado dentro das especificações do fabricante, como mostra a figura abaixo:*

<p align="center"><img src="../../Imagens/Atividade 2/9.2.png" align="center"><br></p>

*Para analisar o efeito dos resistores, foi montado dois circuitos subtratores com ganhos 1000V/V. Percebeu-se que a diferença pelo efeito da Vcm, offset e CMRR.*

<b>b) Qual erro na tensão de saída com relação CMRR do AmpOp</b><br>

*Olhando no datasheet, podemos observar os erros do CMRR.*

<p align="center"><img src="../../Imagens/Atividade 2/9.3.png" align="center"><br></p>

<b>c) Dica de exemplos com valores diferentes de tensão de modo comum (VCM). Faça o mesmo circuito com resistores com tolerâncias bem distintas, ex. 1% e 5%</b><br>

*O datasheet demonstra em algumas situações, que podemos aliviar as limitações apenas modificando as tensões de alimentação e as resistências do ampop que estamos trabalhando.*

---

<b>10. Faça um resumo explicando as limitações de tensão de entrada e saída de um AmpOp. De exemplos, utiliza-se valores de datasheet.</b><br>

*Vejamos como a tensão de modo comum e as oscilações de tensão de entrada e saída são normalmente definidas em uma planilha de dados.
A faixa de tensão de modo comum é definida aqui com os limites mínimo e máximo dados em relação às fontes de alimentação. A alimentação negativa, V-, é zero volts neste caso, portanto, zero volts menos 0,1 V nos dá -0,1 V para a limitação mínima do modo comum. A alimentação positiva, V +, é de 5 V, então 5 V menos 3,5 V nos dá 1,5 V para a limitação máxima do modo comum. Portanto, a aplicação de uma tensão de modo comum de entrada abaixo de -0,1 V ou acima de 1,5 V resultará em uma saída não linear.
A oscilação de saída é dada aqui, e é o mesmo tipo de definição que é relativa às tensões de alimentação. A tensão de saída mínima é V-/+ 0,2 V, ou 0,2 V neste caso, e a tensão de saída máxima é V+/- 0,2 V ou 4,8 V. Conduzir a saída abaixo de 0,2 V ou acima de 4,8 V fará com que a saída se torne não linear.*

<p align="center"><img src="../../Imagens/Atividade 2/10.png" align="center"><br></p>

<b>a) Defina o que é um AmpOp Rail-to-rail.</b><br>
*Este componente tem como principal característica a capacidade de aproveitar praticamente todo o range de alimentação em sua saída, na prática contando com apenas alguns mV de perda entre os limites de alimentação*<br>

---

<b>11. O que é tensão de offset? Como calcular o efeito resultante na tensão de saída de um amplificador inversor?</b><br>
*A tensão de offset faz com que apareça um deslocamento no nível CC do sinal de saída, poderiamos calcular aplicando um ground em ambas de suas entradas.*<br>

---

<b>11. O que é tensão de offset? Como calcular o efeito resultante na tensão de saída de um amplificador inversor?</b><br>
*Este componente tem como principal característica a capacidade de aproveitar praticamente todo o range de alimentação em sua saída, na prática contando com apenas alguns mV de perda entre os limites de alimentação*<br>

---

<b>12. Como minimizar o efeito da tensão de offset?</b><br>
*A utilização de um potenciômetro nos pinos de ajuste de offset em qualquer AmpOp*<br>

---

<b>13. O que é a variação da tensão de offset pela temperatura?</b><br>
*É a forma de encontrar o setpoint pela temperatura do AmpOp.*<br>
<b>a) Como verificar esse parâmetro no datasheet?</b><br>
*Podemos achar na aba de Offset Voltage.*<br>

**Modelo: OPA2991**

<p align="center"><img src="../../Imagens/Atividade 2/13.png" align="center"><br></p>

---

<b>14. O que são as correntes de polarização(Ibias) de AmpOp?</b><br>
*É o valor médio de duas correntes IB+ e IB_ , na presença de uma tensão na entrada, Vcc e Gnd (Vo=0).*<br>
<b>a) Como minimizar o efeito destas correntes? Descreva as aproximações e os possíveis circuitos para mitigar o problema.</b><br>
*Podemos utilizar componentes externos adicionais, como resistores, como modo de contornar os erros de tensão na saída.*<br>
<b>b) Descreva a corrente de offset na polarização dos AmpOp.</b><br>
*A diferença das correntes de fuga e correntes da porta dos transistores, é chamada de corrente de "offset" de entrada.*<br>
