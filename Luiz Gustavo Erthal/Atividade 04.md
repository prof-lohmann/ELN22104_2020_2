#### Atividade 04

## Aluno: Luiz Gustavo Erthal

### PARTE I: ENTENDENDO UM REGULADOR LINEAR

**CONCEITOS IMPORTANTES**

#### Princípios de regulação de tensão

Um regulador de tensão é um circuito cujo objetivo é proporcionar uma tensão *CC* constante em seus terminais de saída.¹ 

#### Tensão de saída e tensão de ripple

Exige-se que a **tensão de saída** seja mantida constante apesar das variações na corrente da carga drenada dos terminais de saída do regulador e das variações na tensão *cc* da fonte de alimentação que alimenta o circuito regulador.¹

A **tensão de ripple** é uma ondulação de tensão fornecida pela fonte, que é dependente do valor da capacitância do capacitor e da corrente consumida pela carga.²

#### Regulação de linha

A **regulação de linha** tem como principal objetivo não deixar com que a tensão de alimentação varie. É definida como a relação entre a variação da tensão de saída com a da corrente. 
$$
Reg. de Linha = ∆Vout / ∆Vin
$$

#### Regulação de Carga

Ao contrário do anterior, o **regulador de carga** é quem regula a variação de tensão de saída com a variação da corrente consumida pela carga.
$$
Reg.deCarga = ∆Vout/∆Icarga
$$

#### Conceito de LDO – Low Dropout Voltage

Um LDO é um regulador de tensão linear *cc* que pode regular a tensão de saída mesmo quando a tensão de alimentação está muito próxima da tensão de saída. É definido como:
$$
Vldo = Vin - Vout
$$

#### Qual relação entre a tensão de alimentação do AmpOp e a tensão de saída?

A tensão de saída (Vout) estará sempre limitada pela alimentação do AmpOp. Porém, é importante verificar no datasheet do AmpOp suas limitações, já que atuará no campo da saturação uma vez que o valor de tensão se aproximar do valor da alimentação.

#### O que devemos considerar para esse circuito operar como um LDO?

Como visto anteriormente nos conceitos acima, um LDO é definido pela tensão de entrada (Vin) menos a tensão de saída (Vout). Analisando o circuito, podemos perceber que Vin será limitado ao diodo zener D3 ligado e sua Vout será limitado pelos valores de alimentação do amplificador operacional escolhido.

#### Como obter as tensões de alimentação para o AmpOp (VCC e VEE)?

A tensão de alimentação do amplificador operacional deve ser maior do que a tensão que o circuito oferece, pois o AmpOp não pode saturar o sinal.



##### CIRCUITO PROPOSTO 01

#### Utilizando o circuito dobrador de tensão, qual valor de VCC você obtêm para um sinal Vin+ de 12Vrms? Quais problemas apresentam esse circuito? Podemos melhorar?
$$
Vout = 2 * Vpp - Vd1 - Vd2
$$

$$
Vout = 12 * 2 * √2 - 0,7 - 0,7
$$

$$
Vout = 32,541V
$$

Os maiores problemas deste circuito são devidos a tensão de ripple - aquela tensão parasita explicada anteriormente - proveniente das escolhas dos capacitores, que deve-se levar em conta o tempo da carga total do componente. Para melhorar, pode-se fazer um bom redimensionamento dos valores dos capacitores ou adicionar um regulador linear de tensão.



##### CIRCUITO PROPOSTO 02

#### Considere: AmpOp LM324, MOSFET IRF540, VOUT = 15V, IOUT = 1A, vin+ = 12Vrms, vripple_pós_retificador = 1V, considere as quedas de tensão nos diodos de 0,7V.

- Qual a Tensão VGS? Descreva como obter o valor.

A tensão Vgs para uma corrente de 1A é de aproximadamente 4V. 

Podemos obter o valor ao procurar no datasheet do AmpOp considerado - LM324.

https://www.vishay.com/docs/91021/91021.pdf

![i01](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%204%20-%20Image%2001.png)

- Qual a corrente de alimentação do AmpOp?

Temos uma corrente mínima de 1mA e máxima de 3mA.

![i02](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%204%20-%20Image%2002.png)

- Qual a tensão de alimentação do AmpOp?

Vcc máximo de 32V.

![I03](https://github.com/LGErthal/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Luiz%20Gustavo%20Erthal/Images/Atividade%204%20-%20Image%2003.png)

- Qual fator devo considerar para escolher o transistor Q1?

Deve-se ser necessário a escolha de um transistor com o BETA bem elevado, para que a corrente de base de Q1 seja menor que a corrente do zener.

- Qual valor da tensão do diodo zener D6?

Aproximadamente 24V.

- Como escolher o diodo zener D6, maximizando a eficiência energética e minimizando os ruídos no circuito?

A escolha de um zener com uma resistência baixa, para que se passe o menor valor de corrente possível e assim, o sistema terá mais estabilidade e sofrerá menos com variações.

- Considere que, por alterações futuras no circuito, o AmpOp poderá ter uma aumento de 10mA na corrente de alimentação, o circuito proposto continuará funcionando?

Sim, desde que a corrente de alimentação seja maior que a mínima necessária.