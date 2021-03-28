<table align="center"><tr><td align="center" width="9999"><br>
<img src="../../Imagens/logoifsc.png" align="center" width="150" alt="Logo IFSC">

# Atividade 2

<b>Instituto Federal de Educação, Ciência e Tecnologia de Santa Catarina<br>
Campus Florianópolis<br>
Departamento Acadêmico de Eletrônica<br>
Eletrônica I</b>

*Jonathan Chrysostomo Cabral Bonette*
</td></tr></table>

<p align=center>OBS: por contratempos de dispositivos, as imagens serão editadas e colocadas aqui posteriormente, todos os exercícios terão uma imagem representativa.</p>

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
*Usando o método de nós, I1=I2-I_ => I1=I2, assim I1=(Vo-0)/R1 e I2=(0-V+)/R2, logo Vo=(-R1/R2)*V+, e seu amplificador será G=(-R1/R2)*

---

<b>5. Descreva as principais características das topologias:</b>

<b>a) Seguidor de Tensão (Buffer)</b><br>
*A ideia de um buffer, ou seguidor de tensão, é a de um circuito que apresente na saída exatamente a entrada aplicada*<br><br>
<b>b) Amplificador Inversor</b><br>
*Este amplificador é chamado de inversor porque, além de amplificar o sinal de entrada, o sinal de saída possui polaridade invertida, ou seja, valores positivos na entrada se tornam valores negativos na saída e vice-versa.*<br><br>
<b>c) Amplificador Não Inversor</b><br>
*Este amplificador é chamado de não-inversor porque o sinal de saída possui mesma polaridade do sinal de entrada*<br><br>
<b>d) Amplificador Somador Inversor</b><br>
*O amplificador somador é um circuito com AMPOP que permite realizar a soma de dois ou mais sinais.*<br><br>
<b>e) Amplificador Somador Não Inversor</b><br>
*A diferença entre o somador inversor é de que as tensões de entrada serão aplicadas ao terminal inversor do ampop.*<br><br>
<b>f) Subtrator</b><br>
*O amplificador subtrator realiza um resultado na saída de uma tensão igual à diferença entre os sinais aplicados, multiplicada por um ganho (G).*<br><br>
<b>g) Amplificador de Instrumentação</b>
*Os amplificadores de instrumentação são conhecidos por terem uma entrada diferencial e uma elevada impedância de entrada.*<br>

---

<b>6. Explique o efeito do ganho em MALHA ABERTA FINITO, para as topologias Amplificador Inversor e Amplificador não inversor.</b><br>
<b>a) Exemplifique com circuitos com ganhos em malha fechada elevado (Ex. 1000V/Ve -1000V/V) e com ganhos menores (Ex. 10V/V e -10V/V), faça a comparação com erros percentuais e utilize uma variação de ganho em malha aberta entre 120dB e 20dB.<br></b>
*Imagem será colocada.*<br>
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
*Imagem será colocada.*<br>
<b>b) Qual erro na tensão de saída com relação CMRR do AmpOp</b><br>
*Imagem será colocada.*<br>
<b>c) Dica de exemplos com valores diferentes de tensão de modo comum (VCM). Faça o mesmo circuito com resistores com tolerâncias bem distintas, ex. 1% e 5%</b><br>
*Imagem será colocada.*<br>
 
---

<b>10. Faça um resumo explicando as limitações de tensão de entrada e saída de um AmpOp. De exemplos, utiliza-se valores de datasheet.</b><br>
*Imagem será colocada.*<br>
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
*Podemos achar na aba de Offset Voltage. (Imagem será colocada).*<br>

---

<b>14. O que são as correntes de polarização(Ibias) de AmpOp?</b><br>
*É o valor médio de duas correntes IB+ e IB_ , na presença de uma tensão na entrada, Vcc e Gnd (Vo=0).*<br>
<b>a) Como minimizar o efeito destas correntes? Descreva as aproximações e os possíveis circuitos para mitigar o problema.</b><br>
*Podemos utilizar componentes externos adicionais, como resistores, como modo de contornar os erros de tensão na saída.*<br>
<b>b) Descreva a corrente de offset na polarização dos AmpOp.</b><br>
*A diferença das correntes de fuga e correntes da porta dos transistores, é chamada de corrente de "offset" de entrada.*<br>