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
<p align="center"><img src="../../Imagens/Atividade 3/2a.png" align="center"><br></p>

<b>◦ Tensão de modo comum</b><br>
<p align="center"><img src="../../Imagens/Atividade 3/2b5.png" align="center"><br></p>
<p align="center"><img src="../../Imagens/Atividade 3/2b3.png" align="center"><br></p>

<b>◦ CMRR</b><br>
<p align="center"><img src="../../Imagens/Atividade 3/2c5.png" align="center"><br></p>
<p align="center"><img src="../../Imagens/Atividade 3/2c3.png" align="center"><br></p>

<b>◦ Máxima e mínima tensão de entrada</b><br>
<p align="center"><img src="../../Imagens/Atividade 3/2d.png" align="center"><br></p>

<b>◦ Tensão de offset</b><br>
<p align="center"><img src="../../Imagens/Atividade 3/2e.png" align="center"><br></p>

<b>◦ Corrente de polarização</b><br>
<p align="center"><img src="../../Imagens/Atividade 3/2f.png" align="center"><br></p>

<b>◦ Consumo de corrente</b><br>
<p align="center"><img src="../../Imagens/Atividade 3/2g.png" align="center"><br></p>

<b>◦ Ganho em malha aberta</b><br>
<p align="center"><img src="../../Imagens/Atividade 3/2i.png" align="center"><br></p>

<b>◦ Impedância de entrada</b><br>
``Não presente no datasheet.``

***Analog Devices: https://www.analog.com/media/en/technical-documentation/data-sheets/AD8538_8539.pdf***

---

## Para todas simulações abaixo utilize a alimentação simétrica recomendada no datasheet

<b>2. Simule um circuito seguidor de tensão com cada um dos ampops indicados e verifique os efeitos decorrentes da máxima e mínima tensão de entrada.</b><br>
<b>1. Dica utilize um sinal senoidal de 1kHz para auxiliar na visualização.</b><br>
### 8040
<p align="center"><img src="../../Imagens/Atividade 3/q2a.png" align="center"><br></p>

### 8539
<p align="center"><img src="../../Imagens/Atividade 3/q2a 8539.png" align="center"><br></p>

<b>2. Responda quais os valores das tensões de saturação?</b><br>
``Podemos ver que para o circuito seguidor de tensão ``**8040**``, a saturação apresenta o valor da alimentação de ``**±5V**`` e para o circuito seguidor de tensão ``**8539**``, a saturação apresenta o valor da alimentação de ``**±2.5V**``.``

---

<b>3. Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual -100V/V.</b><br>
*Sendo **G = -100V/V** e **R1 = 1kΩ**, e como **G = -Rf/R1**, assim **Rf = 100kΩ**.*<br>
<b>1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.</b><br>

### 8040
``Aplicando 0V na entrada do nosso circuito inversor, podemos ver uma saída de aproximadamente -168mV, isso se dá pelo Voff presente no circuito, podemos ver o Voff aplicando alguns cálculos:
Vimos que, ``**Vo = G1xV3 + G2xVoff**``, como ``**G1 = 0**``, então, ``**Vo = G2xVoff**``, sendo`` **G2 = (Rf/R1 + 1)**``. Assim ``**Voff = Vo/G2**``, então, ``**Voff = 1.68mV**``. Como a Voff máxima é 6mV, então nosso circuito está dentro do ideal.``

<p align="center"><img src="../../Imagens/Atividade 3/q3 8040 a.png" align="center"><br></p>

### 8539
``Aplicando 0V na entrada do nosso circuito inversor, podemos ver uma saída de aproximadamente 1.386591mV, isso se dá pelo Voff presente no circuito, podemos ver o Voff aplicando alguns cálculos:
Vimos que, ``**Vo = G1xV3 + G2xVoff**``, como ``**G1 = 0**``, então,`` **Vo = G2xVoff**``, sendo ``**G2 = (Rf/R1 + 1)**``. Assim ``**Voff = Vo/G2**``, então,`` **Voff = 0.0137mV**``. Como a Voff máxima é 6mV, então nosso circuito está dentro do ideal.``

<p align="center"><img src="../../Imagens/Atividade 3/q3 8539 a.png" align="center"><br></p>

<b>2. Aplique um sinal senoidal de 10mVpp@1kHz na entrada e verifique o sinal de saída. Explique o resultado.</b><br>

### 8040
<p align="center"><img src="../../Imagens/Atividade 3/q3 8040 b.png" align="center"><br></p>

### 8539
<p align="center"><img src="../../Imagens/Atividade 3/q3 8539 b.png" align="center"><br></p>

---

<b>4. Simule um circuito amplificador não inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual 10V/V.</b><br>
*Sendo **G = 10V/V** e **R1 = 10kΩ**, e como **G = (1 + Rf/R1)**, assim **Rf = 90kΩ**.*<br>
<b>1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.</b><br>

### 8040
<p align="center"><img src="../../Imagens/Atividade 3/q4 8040 a.png" align="center"><br></p>

### 8539
<p align="center"><img src="../../Imagens/Atividade 3/q4 8539 a.png" align="center"><br></p>

<b>2. Aplique um sinal continuo de 5mV, 50mV, 200mV e 500mV na entrada e verifique o sinal de saída. Qual o erro com relação ao ganho calculado? Explique o resultado.</b><br>

### 8040
<p align="center"><img src="../../Imagens/Atividade 3/q4 8040 b.png" align="center"><br></p>

| Vnin(V)| Vteórico(V) | Vsimulado(V) | Erro(%) |
|:--:|:--:|:--:|:--:|
| 5m | 50m | 34.7m | 30,6 |
| 50m | 500m | 484.7m | 3,06 |
| 200m | 2 | 1.98 | 0,78 |
| 500m | 5 | 4.96 | 0,68 |

### 8539
<p align="center"><img src="../../Imagens/Atividade 3/q4 8539 b.png" align="center"><br></p>

| Vnin(V)| Vteórico(V) | Vsimulado(V) | Erro(%) |
|:--:|:--:|:--:|:--:|
| 5m | 50m | 50.1m | 0,2 |
| 50m | 500m | 500.1m | 0,02 |
| 200m | 2 | 2.0002 | 0,01 |
| 500m | 5 | 2.4762 | 50,47 |

``O erro de 50% do Vnin é por causa da saturação do sinal, pois as tensões de alimentação são de ±2.5V.``

---

<b>Caso deseja-se projetar um amplificador subtrator com ganho de 100V/V, para sinais muito pequenos com variação de +/-10uV até +/-30mV de muito baixa frequência, qual desses ampops você utilizaria? Justifique a sua resposta.</b><br>
``Seria considerado o uso do AmpOp AD8539, pois o mesmo, nas simulações se comportou melhor quando foi aplicado baixas tensões de entrada do que o AmpOp 8040.``
  
<b>Escolha um terceiro ampop com características melhores que os ampops acima para uma aplicação
como subtrator</b><br>
``Um AmpOp que poderiamos utilizar é o ``**TLV4333**``, pois as tensões de entrada são baixas.``
