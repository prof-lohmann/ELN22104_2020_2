<table align="center"><tr><td align="center" width="9999"><br>
<img src="../../Imagens/logoifsc.png" align="center" width="150" alt="Logo IFSC">

# Atividade 3

<b>Instituto Federal de Educação, Ciência e Tecnologia de Santa Catarina<br>
Campus Florianópolis<br>
Departamento Acadêmico de Eletrônica<br>
Eletrônica I</b>

*Jonathan Chrysostomo Cabral Bonette*
</td></tr></table>

## Simulação de circuitos com Amplificadores operacionais AD8040 e AD8539

<b>1. Verifique no datasheet dos Ampops indicados os valores dos itens abaixo:</b><br>

### AD8040
*O datasheet fornece informações para três tensões diferentes **Vs=±5V**, **Vs=5V** e **Vs=3V**. Analisaremos apenas para **Vs=±5V** por hora.*

<b>◦ Máxima e mínima tensão de alimentação</b><br>
<p align="center"><img src="../../Imagens/Atividade 3/1a.png" align="center"><br></p>

<b>◦ Tensão de modo comum</b><br>
<p align="center"><img src="../../Imagens/Atividade 3/1b.png" align="center"><br></p>

*Sendo **Vs=±5V**, **Vs=5V** ou **Vs=3V**.*

<b>◦ CMRR</b><br>
<p align="center"><img src="../../Imagens/Atividade 3/1c+-5.png" align="center"><br></p>

*Sendo **Vs=±5V**.*

<b>◦ Máxima e mínima tensão de entrada</b><br>
<p align="center"><img src="../../Imagens/Atividade 3/1d+-5.png" align="center"><br></p>

<b>◦ Tensão de offset</b><br>
<p align="center"><img src="../../Imagens/Atividade 3/1e.png" align="center"><br></p>

<b>◦ Corrente de polarização</b><br>
<p align="center"><img src="../../Imagens/Atividade 3/1f.png" align="center"><br></p>

<b>◦ Consumo de corrente</b><br>
<p align="center"><img src="../../Imagens/Atividade 3/1g.png" align="center"><br></p>

<b>◦ Ganho em malha aberta</b><br>
<p align="center"><img src="../../Imagens/Atividade 3/1h+-5.png" align="center"><br></p>

<b>◦ Impedância de entrada</b><br>
<p align="center"><img src="../../Imagens/Atividade 3/1i+-5.png" align="center"><br></p>

***Analog Devices: https://www.analog.com/media/en/technical-documentation/data-sheets/AD8029_8030_8040.pdf***

### AD8539
<b>◦ Máxima e mínima tensão de alimentação</b><br>
<p align="center"><img src="../../Imagens/Atividade 3/2a.png" align="center" width="500"><br></p>

<b>◦ Tensão de modo comum</b><br>
<p align="center"><img src="../../Imagens/Atividade 3/2b.png" align="center" width="500"><br></p>

<b>◦ CMRR</b><br>
<p align="center"><img src="../../Imagens/Atividade 3/2c.png" align="center" width="500"><br></p>

<b>◦ Máxima e mínima tensão de entrada</b><br>
<p align="center"><img src="../../Imagens/Atividade 3/2d.png" align="center" width="500"><br></p>

<b>◦ Tensão de offset</b><br>
<p align="center"><img src="../../Imagens/Atividade 3/2e.png" align="center" width="500"><br></p>

<b>◦ Corrente de polarização</b><br>
<p align="center"><img src="../../Imagens/Atividade 3/2f.png" align="center" width="500"><br></p>

<b>◦ Consumo de corrente</b><br>
<p align="center"><img src="../../Imagens/Atividade 3/2g.png" align="center" width="500"><br></p>

<b>◦ Ganho em malha aberta</b><br>
<p align="center"><img src="../../Imagens/Atividade 3/2h.png" align="center" width="500"><br></p>

<b>◦ Impedância de entrada</b><br>
<p align="center"><img src="../../Imagens/Atividade 3/2i.png" align="center" width="500"><br></p>


Analog Devices: https://www.analog.com/media/en/technical-documentation/data-sheets/AD8538_8539.pdf

---

## Para todas simulações abaixo utilize a alimentação simétrica recomendada no datasheet

<b>2. Simule um circuito seguidor de tensão com cada um dos ampops indicados e verifique os efeitos decorrentes da máxima e mínima tensão de entrada.</b><br>
<b>1. Dica utilize um sinal senoidal de 1kHz para auxiliar na visualização.</b><br>
<b>2. Responda quais os valores das tensões de saturação?</b><br>

---

<b>3. Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual -100V/V.</b><br>
<b>1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.</b><br>
<b>2. Aplique um sinal senoidal de 10mVpp@1kHz na entrada e verifique o sinal de saída. Explique o resultado.</b><br>

---

<b>4. Simule um circuito amplificador não inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual 10V/V.</b><br>
<b>1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.</b><br>
<b>2. Aplique um sinal continuo de 5mV, 50mV, 200mV e 500mV na entrada e verifique o sinal de saída. Qual o erro com relação ao ganho calculado? Explique o resultado.</b><br>

---

<b>Caso deseja-se projetar um amplificador subtrator com ganho de 100V/V, para sinais muito
pequenos com variação de +/-10uV até +/-30mV de muito baixa frequência, qual desses ampops
você utilizaria? Justifique a sua resposta.
Escolha um terceiro ampop com características melhores que os ampops acima para uma aplicação
como subtrator</b><br>
