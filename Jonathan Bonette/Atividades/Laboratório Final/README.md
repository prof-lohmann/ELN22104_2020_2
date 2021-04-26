<table align="center"><tr><td align="center" width="9999"><br>
<img src="../../Imagens/logoifsc.png" align="center" width="150" alt="Logo IFSC">

# Laboratório Final

<b>Instituto Federal de Educação, Ciência e Tecnologia de Santa Catarina<br>
Campus Florianópolis<br>
Departamento Acadêmico de Eletrônica<br>
Eletrônica I</b>

*Jonathan Chrysostomo Cabral Bonette*
</td></tr></table>

## Objetivos

Integração dos blocos de uma fonte linear

## Introdução
Neste roteiro iremos integrar os circuitos estudados anteriormente, para isso, revise os conceitos de reguladores LDO.

## Parte 01: Entendendo um regulador linear  
Conceitos importantes:<br>
• Princípios de regulação de tensão;<br>
• Tensão de saída e tensão de ripple;<br>
• Regulação de linha;<br>
• Regulação de Carga;<br>
• Conceito de LDO – Low Dropout Voltage<br><br>

Considerando o circuito da figura 01 que representa uma fonte linear com regulador MOSFET, temos o seguinte problema: Qual relação entre a tensão de alimentação do ampop e a tensão de saída? O que devemos considerar para esse circuito operar como um LDO? Como obter as tensões de alimentação para o AmpOp (VCC e VEE)?

<p align="center"><img src="../../Imagens/Laboratório Final/imagem1.png" align="center"><br></p>
<p align="center"><img src="../../Imagens/Laboratório Final/imagem2.png" align="center"><br></p>

### Circuito proposto (01) para a alimentação do AmpOp:

Utilizando o circuito dobrador de tensão, qual valor de VCC você obtêm para um sinal Vin+ de 12Vrms? Quais problemas apresentam esse circuito? Podemos melhorar?

### Circuito proposto (02) para a alimentação do AmpOp:

<p align="center"><img src="../../Imagens/Laboratório Final/imagem3.png" align="center"><br></p>

### Vamos projetar esse circuito de alimentação do AmpOp?
Considere: AmpOp LM324, MOSFET IRF540, VOUT = 15V, IOUT = 1A, vin+ = 12Vrms, vripple_pós_retificador = 1V, considere as quedas de tensão nos diodos de 0,7V.<br>
Pontos Importantes para iniciar o projeto responda justificando as escolhas.<br>
• Qual a Tensão VGS? Descreva como obter o valor.<br>
• Qual a corrente de alimentação do AmpOp?<br>
• Qual a tensão de alimentação do AmpOP?<br>
• Qual fator devo considerar para escolher o transistor Q1?<br>
• Qual valor da tensão do diodo zener D6?<br>
• Como escolher o diodo zener D6, maximizando a eficiência energética e minimizando os ruídos no circuito?<br>
• Considere que, por alterações futuras no circuito, o AmpOp poderá ter uma aumento de 10mA na corrente de alimentação, o circuito proposto continuará funcionando?<br><br>
Projete o circuito de alimentação do AmpOp com as especificações acima.

## Parte 02
Calculando e dimensionando os componentes<br>
a) Para o primeiro bloco (D1, D2 e C1) considere vin+ = 12Vrms, vripple_pós_retificador = 1V e I_carga = 1,1A. Justifique a escolha dos componentes.<br>
b) Circuito referência de tensão zener (R1 e D3):<br>
• Quais fatores devo considerar para escolher o diodo zener para essa aplicação?<br>
• Qual a influência da regulação de linha e da regulação de carga para este circuito?<br>
• Qual o impacto da regulação linha / carga do circuito com o diodo zener na tensão de saída do regulador linear?<br>
Podemos melhorar esse circuito? Quais problemas podemos identificar nesta topologia?<br>
Sugestão de melhoria:<br>

<p align="center"><img src="../../Imagens/Laboratório Final/imagem4.png" align="center"><br></p>

No qual o circuito com R1, R5, Q2 e Q3 é uma fonte de corrente constante para polarizar o diodo zener D3. Vamos projetar?

<p align="center"><img src="../../Imagens/Laboratório Final/imagem5.png" align="center"><br></p>

Podemos melhorar mais ainda? Que tal deixar essa fonte com valor ajustável? Como fazer isso?

c)Escolhendo o transistor M1 e calculando R2 e R3.<br>
• Qual a corrente contínua necessária?<br>
• Quais os limites de tensão para este circuito?<br>
Ao escolher o transistor obtenha:<br>
Quais os os parâmetros L, W, uo, Cox, VA e Vt?<br>
Calcule o valor de RDS para as tensões VGS de 2V, 3V, 4V, 5V e 10V.<br>
Quais as tensões máximas de operação deste componente?<br>
Obtenha as curvas ID x VDS para esse componente para as tensões VGS de 2V, 3V, 4V, 5V e 10V e compare os resultados com as curvas presentes no Datasheet.<br>
Utilizando a curva ID x VDS obtenha os valores RDS e compare com os valores teóricos.<br>
Qual o valor da capacitância de gate?<br>
Justifique a escolha dos resistores R2 e R3.<br>

## Parte 03
Adicionando um circuito de proteção de sobre corrente ao regulador linear.
Primeiramente reflita e pesquise sobre o que é sobrecorrente? Quais os impactos neste circuito?
O que deve fazer um circuito de proteção de sobrecorrente? O que é a proteção foldback?
Pesquise as topologias disponíveis, caso deseja-se fazer um circuito LDO, o o que devemos levar em consideração para o regulador?
Exemplo de circuito: (Vide roteiro 01)

<p align="center"><img src="../../Imagens/Laboratório Final/imagem6.png" align="center"><br></p>
