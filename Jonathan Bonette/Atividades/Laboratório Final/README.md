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
<b>Conceitos importantes:<br></b>
<b>• Princípios de regulação de tensão;<br></b>
`Geralmente formado por semicondutores, tem por finalidade a manutenção da tensão de saída de um circuito elétrico. Sua função principal é manter a tensão produzida pelo gerador dentro dos limites exigidos pela bateria ou sistema elétrico que está alimentando.`

<b>• Tensão de saída e tensão de ripple;<br></b>
`A tensão de saída deve ser contínua em relação ao tempo. Ripple geralmente está associada a uma tensão retificada e filtrada por um capacitor, possui uso bastante importante quando o usuário pretende converter uma tensão alternada em uma tensão contínua. É é dado pela subtração da tensão superior menos a tensão inferior, depois de filtrada e retificada. Funciona como uma ondulação na tensão fornecida pela fonte.`

<b>• Regulação de linha;<br></b>
`A regulação de linha mede a variação da tensão de saída sobre a tensão de entrada.`

<b>• Regulação de Carga;<br></b>
`O regulador de carga, regula a tensão de saída quando diferentes cargas são conectadas, é dado pela variação da tensão de saída pela corrente de saída.`

<b>• Conceito de LDO – Low Dropout Voltage<br></b>
`Os reguladores lineares de baixa queda (LDO) são uma maneira simples e barata de regular uma tensão de saída que é alimentada por uma entrada de tensão mais alta em uma variedade de aplicações. Os LDO são diferenciados por sua capacidade de manter a regulação com pequenas diferenças entre a tensão de alimentação e a tensão de carga.`

<b>Considerando o circuito da figura 01 que representa uma fonte linear com regulador MOSFET, temos o seguinte problema:<br></b>
<b>Qual relação entre a tensão de alimentação do ampop e a tensão de saída?<br></b>
`Pelo circuito AmpOp, a tensão de saída será limitada pela alimentação do circuito, assim como todas seus parâmetros. Dependendo das suas limitações os valores podem ser restringidos à um valor menor que as tensões de alimentação.`

<b>O que devemos considerar para esse circuito operar como um LDO?<br></b>
`Devemos considerar as tensões de entrada e saída, analsiando podemos ver que a tensão de entrada ela será limitada pela escolha do diodo e a tensão de saída será limitada pelos limites impostos pelo AmpOp.`

<b>Como obter as tensões de alimentação para o AmpOp (VCC e VEE)?<br></b>
`Podemos obter analisando a simulação, onde os modos aparecerão nantes da saturação do sinal, da mesma forma utilizando um dobrador de tensão, podemos obter os valores de VCC e VEE`

------------------

<p align="center"><img src="../../Imagens/Laboratório Final/imagem1.png" align="center"><br></p>
<p align="center"><img src="../../Imagens/Laboratório Final/imagem2.png" align="center"><br></p>

### Circuito proposto (01) para a alimentação do AmpOp:

<b>Utilizando o circuito dobrador de tensão, qual valor de VCC você obtêm para um sinal Vin+ de 12Vrms?</b><br>
`Como a queda de tensão para VD4 e VD5 é de 0,7V, e Vin+ = 12Vrms, então: `

<p align="center"><img src="../../Imagens/Laboratório Final/1.png" align="center"><br></p><br>

<b>Quais problemas apresentam esse circuito?</b><br>
`Sua tensão de ripple na realimentação do circuito do AmpOp, onde quando utilizado dessa forma, apresenta rúidos na saída. Então precisamos tomar cautela na escolha do capacitor, pois precisamos levar em conta o tempo de carga, que será longo se caso o capacitor for de alta capacitância.`<br>

<b>Podemos melhorar?</b><br>
`Alguns macetes podem ser aplicados como, adicionar no nosso circuito um regulador linear de tensão na saída do dobrador, fazendo a limitação da tensão de saída que irá alimentar o AmpOp e também escolhendo os componentes corretos para a operação, como por exemplo do capacitor.`<br>

### Circuito proposto (02) para a alimentação do AmpOp:

<p align="center"><img src="../../Imagens/Laboratório Final/imagem3.png" align="center"><br></p>

### Vamos projetar esse circuito de alimentação do AmpOp?
Considere: AmpOp LM324, MOSFET IRF540, VOUT = 15V, IOUT = 1A, vin+ = 12Vrms, vripple_pós_retificador = 1V, considere as quedas de tensão nos diodos de 0,7V.<br>
Pontos Importantes para iniciar o projeto responda justificando as escolhas.<br>
<b>• Qual a Tensão VGS? Descreva como obter o valor.</b><br>
`Pelo datasheet, Vgs para 1A é de 4,5V.`

<p align="center"><img src="../../Imagens/Laboratório Final/2.png" align="center"><br></p><br>

`Podemos obteresse valor fazendo a subtração da tensão de saída do AmpOp U1 e a tensão de saída da fonte (Vout). Olhando para o datasheet, podemos fazer VoutU1 = 4,5V + 15V, assim VoutU1 = 19,5V. O datasheet apresenta 20V, logo vemos que possui uma pequena variação do resultado teórico o que é completamente normal.`<br>

<b>• Qual a corrente de alimentação do AmpOp?</b><br>
`O datasheet apresenta um valor de de 3 mA.`

<p align="center"><img src="../../Imagens/Laboratório Final/3.png" align="center"><br></p><br>

<b>• Qual a tensão de alimentação do AmpOP?</b><br>
`Pelo datasheet podemos ver que pode ser alimentado até 32V.`

<p align="center"><img src="../../Imagens/Laboratório Final/4.png" align="center"><br></p><br>

<b>• Qual fator devo considerar para escolher o transistor Q1?</b><br>
`O beta a ser utilizado precisa ser de um valor consideravelmente alto.`

<b>• Qual valor da tensão do diodo zener D6?</b><br>
`Como VoutU1 = 19,5V, então precisamos utilizar uma tensão para o diodo zener D6 maior que esse valor, uma tensão na segunda dezena seria bom para trabalhar.`

<b>• Como escolher o diodo zener D6, maximizando a eficiência energética e minimizando os ruídos no circuito?</b><br>
`Teremos que ter em mente um diodo zener que tenha uma baixíssima corrente, então devemos usar um que tenha uma baixa resistência, utilizando dessa forma não haverá muito problema de variação de tensão.`

<b>• Considere que, por alterações futuras no circuito, o AmpOp poderá ter uma aumento de 10mA na corrente de alimentação, o circuito proposto continuará funcionando?</b><br>
`Sim, se na minha alimentação possuir uma corrente maior que a mínima corrente que passa no AmpOp, o curcuito proposto funcionará adequadamente.`

<b>Projete o circuito de alimentação do AmpOp com as especificações acima.</b><br>

<p align="center"><img src="../../Imagens/Laboratório Final/p1.png" align="center"><br></p><br>

## Parte 02
<b>Calculando e dimensionando os componentes</b><br>
<b>a) Para o primeiro bloco (D1, D2 e C1) considere vin+ = 12Vrms, vripple_pós_retificador = 1V e I_carga = 1,1A. Justifique a escolha dos componentes.</b><br>
`Analsando podemos ver que certamente D1 e D2 influenciarão diretamente na tensão final do meu circuito, para que não cause grande efeito, seria bom que essa queda de tensão não passasse de 1V, para não consumir a tensão do meu circuito, outras análises podem ser feitas analisando o datasheet. Para o C1, precisariamos olhar com base no retificador de onda, levando em consideração o período, olhando para o datasheet vemos que a Vr (reserva) = 53Vrms, assim, temos que: C = 9,17 mF`

<p align="center"><img src="../../Imagens/Laboratório Final/5.png" align="center"><br></p><br>

<b>b) Circuito referência de tensão zener (R1 e D3):</b><br>
<b>• Quais fatores devo considerar para escolher o diodo zener para essa aplicação?</b><br>
`Precisa ter um valor de Rz baixo para apresentar menores ruídos na saída.`

<b>• Qual a influência da regulação de linha e da regulação de carga para este circuito?</b><br>
`Como ela mede a efetividade, temos que ter uma baixa variação na saída do circuito, ou seja, teremos que ter uma variação quase nula.`

<b>• Qual o impacto da regulação linha / carga do circuito com o diodo zener na tensão de saída do regulador linear?</b><br>
`O zener vai estar limirtando a tensão de saída, por esse modo teremos que Vout tendendo a 0, então teremos que:`

`Regulação de linha = ΔVout/ΔVin = 0/ΔVin = 0 V/V`

`Dessa forma mesmo o valor da tensão sendo variado a saída terá pouca variação.`

`Olhando para a outra regulação, vemos que:`

`Regulação de carga = ΔVout/ΔIout = 0/ΔIout = 0 V/A`

`Dessa forma mesmo que a carga varie, dado a regulação, permanecerá com o mesmo valor.`

<b>Podemos melhorar esse circuito? Quais problemas podemos identificar nesta topologia?</b><br>
`Se pudermos fazer algo para que as correntes não interfiram na regulação, poderemos melhorar esse circuito, algo para deixar a corrente constante já serviria.`

<b>Sugestão de melhoria:</b><br>
***Colocar a imagem da simulação do LtSpice***

<p align="center"><img src="../../Imagens/Laboratório Final/imagem4.png" align="center"><br></p>

No qual o circuito com R1, R5, Q2 e Q3 é uma fonte de corrente constante para polarizar o diodo zener D3. Vamos projetar?

<p align="center"><img src="../../Imagens/Laboratório Final/imagem5.png" align="center"><br></p>

Podemos melhorar mais ainda? Que tal deixar essa fonte com valor ajustável? Como fazer isso?

<b>c)Escolhendo o transistor M1 e calculando R2 e R3.</b><br>
<b>• Qual a corrente contínua necessária?</b><br>
`Para o M1, é necessário que seja uma corrente de cerca de 1A (lembrando que Vgs = 4,5V).`

<b>• Quais os limites de tensão para este circuito?</b><br>
`Tendo em mente o valor do Vgs, sabemos que ela será limitada pela Rtensão*Ganho, da mesma forma temos que ter em mente que pela tensão de entrada, esse circuito estará na casa dos 15V e 16V. Então o valor da subtração da tensão de saída do AmpOp pela tensão Vout, teremos um valor ideal para usar sobre o Vgs. `

<b>Ao escolher o transistor obtenha:</b><br>
<b>Quais os os parâmetros L, W, uo, Cox, VA e Vt?</b><br>
`Pelo datasheet do mosfet apresentado, podemos obter:`

`L = 100uH, W= 100uW, u0 (Valor Padrão) = 600cm²/V/s, C0x = KP/u0 = 41,68mF/m², VA = 1/λ = 343,61V, Vt = 3.56362V.`

<b>Calcule o valor de RDS para as tensões VGS de 2V, 3V, 4V, 5V e 10V.</b><br>
`Para:`<br>
`• Vgs = 2V; VtInicial = 3,56362V; RDS teórico = ∞Ω; RDS simulado = 4MΩ;`<br>
`• Vgs = 3V; VtInicial = 3,56362V; RDS teórico = ∞Ω; RDS simulado = 4MΩ;`<br>
`• Vgs = 4V; VtInicial = 3,56362V; RDS teórico = 0,137Ω; RDS simulado = 0,156Ω;`<br>
`• Vgs = 5V; VtInicial = 3,56362V; RDS teórico = 0,073Ω; RDS simulado = 0,074Ω;`<br>
`• Vgs = 10V; VtInicial = 3,56362V; RDS teórico = 0,051Ω; RDS simulado = 0,051Ω;`<br>

<b>Quais as tensões máximas de operação deste componente?</b><br>
`Pelo datasheet, vemos que: Vgs(máx) = ±20V e Vds(máx) = 100V.`

<b>Obtenha as curvas ID x VDS para esse componente para as tensões VGS de 2V, 3V, 4V, 5V e 10V e compare os resultados com as curvas presentes no Datasheet.</b><br>
`Pelo datasheet, viu-se que os valores estão coerentes, dentro do esperado.`

<b>Utilizando a curva ID x VDS obtenha os valores RDS e compare com os valores teóricos.</b><br>
`Pelo datasheet, viu-se que os valores estão coerentes, dentro do esperado.`

<b>Qual o valor da capacitância de gate?</b><br>
`O valor pode ser determinado fazendo um simpels equacionamento, Cgs = Ciss - Crss = 1580pF.`

<b>Justifique a escolha dos resistores R2 e R3.</b><br>
`Precisamos verificar quais são minhas tensões de entrada e saída do circuito proposto, como Vin = 12,5V e Vout = 15V (dados definidos antetiormente).`

`Para um amplificador operacional não inversor, usamos as fórmulas pré-estabelecidas, dessa forma: R3 = 2kΩ e R2 = 400Ω.`

## Parte 03
<b>Adicionando um circuito de proteção de sobre corrente ao regulador linear.</b><br>
<b>Primeiramente reflita e pesquise sobre o que é sobrecorrente?</b><br>
`De forma clara, a sobrecorrente é circulação de excesso de corrente no circuito de um aparelho elétrico, ou seja, de uma corrente que excede o valor nominal`

<b>Quais os impactos neste circuito?</b><br>
`Dependendo do excesso, tem alta possibilidade de o dispositivo falhar, apresentar queimas de componentes, etc.`

<b>O que deve fazer um circuito de proteção de sobrecorrente?</b><br>
`O circuito interrompe a corrente para proteger o circuito assim que o valor da corrente exceder os limites normais.`

<b>O que é a proteção foldback?</b><br>
`É um método usado em fontes de alimentação para protegê-las de situações atuais, como curto-circuito na saída com um fio ou conexão de muitos equipamentos à fonte de alimentação.`

<b>Pesquise as topologias disponíveis, caso deseja-se fazer um circuito LDO, o o que devemos levar em consideração para o regulador?</b><br>
`Com a aplicação de um circuito LDO, dependendo de falhas de projeto, condições adversas, o circuito pode sofrer correntes acima do limite além do gasto energético ser maior do que o esperado. Algumas coisas que o peojetista pode levar em consideração é a aplicação de proteções, como a própria foldback citada acima. `

`Procurando na internet vemos que existe um catálogo extenso de LDOs que seguem a topologia juntamente com a proteção. Inclusive alguns alguns da prórpia Texas, muito utilizado por nés durante esse semestre.`

<b>Exemplo de circuito: (Vide roteiro 01)</b><br>

<p align="center"><img src="../../Imagens/Laboratório Final/imagem6.png" align="center"><br></p>

<p align="center"><img src="../../Imagens/Laboratório Final/p2.png" align="center"><br></p>
