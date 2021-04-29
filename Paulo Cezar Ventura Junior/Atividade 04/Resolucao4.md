# Atividade 4
Aluno:
* Paulo Cezar Ventura Junior - <paulo.cvj@aluno.ifsc.edu.br>

Professores:
* Daniel Lohmann

## Integração de blocos de uma fonte linear

## Parte 01: Entendendo um regulador linear

![Circuito_01](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2004/Exemplos/Circuito_01.png)

#### Qual a relação entre a tensão de alimentação do ampop e a tensão de saída?

R: A tensão de saída possui relação com a alimentação do AmpOp juntamente com as resistências, que nesse caso são R2 e R3, de tal forma que ficaria: Vout = Vin*(R2+R3)/R3. Quando a tensão de saída sai do nosso range, o AmpOp desliga o MOSFET e temos 0V na saída.

#### O que devemos considerar para esse circuito operar como um LDO?

R: Devemos considerar uma baixa queda de tensão no MOSFET, e garantir também que a tensão de alimentação do AmpOp e MOSFET seja maior do que a tensão na saída.

#### Como obter as tensões de alimentação para o AmpOp (VCC e VEE)?

R: Já que as tensões de alimentação do AmpOp devem ser maiores do que o de saída, devemos encontrar uma forma de regulação desse tipo (como por exemplo uma fonte simétrica).

#### Utilizando o circuito dobrador de tensão, qual valor de VCC você obtêm para um sinal Vin+ de 12Vrms?

R: Temos:
```
Vp = 12*(2/√2)
Vp = 16,97V

Vcc = 2*Vp - 2*Vd
Vcc = 2*(16,97) - 2*(0,7)
Vcc = 32,54V
```

#### Quais problemas apresentam esse circuito?

R: Esse circuito apresenta tensão de ripple na realimentação do AmpOp, o que por consequência gera um alto ruído na saída do circuito.

#### Podemos melhorar?

R: Sim, podemos adicionar um regulador linear de tensão para já eliminar os ruídos. Também podemos evitar a ondulação escolhendo corretamente o capacitor para o circuito, mas ele não pode ser de um valor nem muito alto nem muito baixo, por conta de um longo tempo de carga se for um valor muito alto, e uma baixa eficácia em anular a ondulação se o valor for baixo.

### Circuito proposto (02) para a alimentação do AmpOp:

![Circuito_02](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2004/Exemplos/Circuito_02.png)

#### Considere: AmpOp LM324, MOSFET IRF540, VOUT = 15V, IOUT = 1A, vin+ = 12Vrms, vripple_pós_retificador = 1V, considere as quedas de tensão nos diodos de 0,7V.

#### Qual a tensão Vgs? Descreva como obter o valor

R: A tensão Vgs pode ser obtida diretamente pelo gráfico localizado no datasheet do componente. Considerando Iout = 1A, localizamos a informação de que Vgs para 1A é 4,5V.

![VGS_IRF540](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2004/Exemplos/VGS_IRF540.png)

#### Qual a corrente de alimentação do AmpOp?

R: Conforme o datasheet, temos que a corrente de alimentação do LM324 é:

![Datasheet_LM324](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2004/Exemplos/Datasheet_LM324.png)

Ou seja, Icc possui valores entre 1,5mA e 3,0mA no máximo.

#### Qual a tensão de alimentação do AmpOp?

R: Conforme o datasheet, temos que a tensão de alimentação do LM324 é:

![LM324_Voltage](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2004/Exemplos/LM324_Voltage.png)

Ou seja, Vcc possui 32V de alimentação no máximo.

#### Qual fator devo considerar para escolher o transistor Q1?

R: Devemos utilizar um transistor Q1 com um beta bem elevado.

#### Qual o valor da tensão do diodo zener D6?

R: Como Vout = 15V e Vgs = 4,5V, então VoutU1 = 19,5V. Para o zener D6 temos que utilizar uma tensão maior que esse valor, algo em torno dos 21V já seria suficiente.

#### Como escolher o diodo zener D6, maximizando a eficiência energética e minimizando os ruídos no circuito?

R: O ideal a se fazer seria utilizar um diodo zener com baixa corrente, e por consequência baixa resistência, para minimizar a variação da tensão no circuito.

#### Considere que, por alterações futuras no circuito, o AmpOp poderá ter uma aumento de 10mA na corrente de alimentação, o circuito proposto continuará funcionando?

R: Sim, mesmo se a corrente passar da mínima requisitada pelo AmpOp ainda irá funcionar normalmente.

### Projete o circuito de alimentação do AmpOp com as especificações acima.

![LDO_01](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2004/Exemplos/LDO_01.png)

Vale notar que o Amplificador utilizado (LM324) não foi possível de ser utilizado no LTSpice, porém foi criado um novo modelo no LTSpice, onde seus bornes são o seguinte:

```
1: Entrada não inversora;
2: Entrada inversora;
3: Alimentação positiva;
4: Alimentação negativa;
5: Vout;
```

Portanto, para o resto desse relatório, deve-se considerar essas entradas para o Amplificador em questão.

Para esse circuito, foram simulados os dados comparando o nó Vin com o nó Vout, como segue na imagem abaixo:

![VinxVout](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2004/Exemplos/VinxVout.png)

Verificamos também no seguinte gráfico a comparação junto a alimentação do AmpOp, que não chega ao seu Vcc máximo especificado pelo Datasheet.

![Vcc_Ampop](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2004/Exemplos/Vcc_Ampop.png)

## Parte 02: Calculando e dimensionando os componentes

### a)

#### Para o primeiro bloco (D1, D2 e C1) considere vin+ = 12Vrms, vripple_pós_retificador = 1V e I_carga = 1,1A. Justifique a escolha dos componentes.

R: É fato que D1 e D2 influenciam na tensão final do circuito. Portanto, podemos considerar que os diodos terão queda de tensão de 0,7V (Diodo de silício). Para o capacitor C1, consideramos o retificador de onda e sua tensão reversa, que é de 53Vrms.

```
I_carga = 1,1A
Vrp = 1V
freq = 60

C = I_carga/2*freq*Vrp
C = 1,1/2*60*1 = 0,0092 = 9,2 mF
```

### b) Circuito referência de tensão zener (R1 e D3):

#### Quais fatores devo considerar para escolher o diodo zener para essa aplicação?

R: Rz precisa ser pequeno para apresentar o mínimo ruído na saída.

#### Qual a influência da regulação de linha e da regulação de carga para este circuito?

R: Como a regulação de linha e de carga mede a efetividade do circuito, precisamos de uma mínima variação em sua saída.

#### Qual o impacto da regulação linha / carga do circuito com o diodo zener na tensão de saída do regulador linear?

R: Para que tenhamos uma tensão de saída estável, nosso circuito deve ter uma baixa variação da tensão de carga e de linha. Como o zener regula a tensão de entrada do AmpOp, podemos considerar que nosso Vout tende a 0, portanto:

```
Regulação de linha = ΔVout/ΔVin = 0/ΔVin = 0
Regulação de carga = ΔVout/ΔIout = 0/ΔIout = 0
```
De tal forma que mesmo que nossa carga passe a variar, como possuímos regulação, ainda teremos o mesmo valor.

#### Podemos melhorar esse circuito? Quais problemas podemos identificar nesta topologia?

R: Sim, podemos agir de forma que a nossa corrente se mantenha constante no circuito, para que a tensão no zener não fique variando.

O circuito abaixo foi projetado com o bloco para deixar a corrente constante no circuito.

![Segundo_bloco](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2004/Exemplos/Segundo_bloco.png)

#### Podemos melhorar mais ainda? Que tal deixar essa fonte com valor ajustável? Como fazer isso?

R: Podemos melhorar acrescentando um potenciômetro para ajuste fino em paralelo com a tensão de referência de saída, juntamente com alguns resistores em série ao potenciômetro justamente para liberar ele para um ajuste fino, visto que se utilizar somente ele, a sua variação de resistência afetaria muito mais o circuito do que se utilizasse resistores em série.

### c) Escolhendo o transistor M1 e calculando R2 e R3

#### Qual a corrente contínua necessária?

R: No transistor M1, como especificado no projeto, devemos ter uma corrente de 1A.

#### Quais os limites de tensão para este circuito?

R: As tensões se limitam pela entrada, que estará entre 15V a 17V. Nosso VGS terá a limitação da nossa regulação de tensão zener * ganho. A tensão VDO, no nosso transistor MOS, deve ser de menor valor possível. E por fim, nos resistores que contribuem ao ganho teremos a limitação de Vout, que deve ser de 15V.

### Ao escolher o transistor obtenha:

#### Quais os parâmetros L, W, u0, C0x, VA e Vt?

R: Temos:
```
L = 100uH;
W = 100 uW;
u0 = 600 cm^2/V/s;
C0x = 41,68 mF/m^2;
VA = 343,61V;
Vt = 3,56V;
```

#### Calcule o valor de RDS para as tensões VGS de 2V, 3V, 4V, 5V e 10V

VGS (V) | Vt (V) | RDS teórico (Ohm) | RDS Simulado (Ohm)
--------|--------|-------------------|-------------------
2       | 3,56   |  Infinito         |  4 Meg
3       | 3,56   |  Infinito         |  4 Meg
4       | 3,56   |  0,137            |  0,156
5       | 3,56   |  0,073            |  0,074
10      | 3,56   |  0,051            |  0,051

#### Quais as tensões máximas de operação deste componente?

R: Vgs máximo no IRF540 é +-20V, e sua VDS máxima é 100V.

#### Obtenha as curvas ID x VDS para esse componente para as tensões VGS de 2V, 3V, 4V, 5V e 10V e compare os resultados com as curvas presentes no Datasheet.

R: Todas as simulações ocorreram de acordo com o datasheet.

#### Qual o valor de capacitância do gate?

R: Cgs = Ciss - Crss = 1,7u - 0,12u = 1,58uF.

#### Justifique a escolha dos resistores R2 e R3.

R: Como estamos utilizando uma configuração não inversora no AmpOp, e temos como requisito uma tensão de saída de 15V, e uma de entrada de 12,5V, precisamos de um pequeno ganho para nos adequar as tensões corretas. A relação entre R2 e R3 nos permite ter esse ganho correto, e como o resistor está na casa dos kOhm, a corrente que passa no circuito é na casa dos mA.

## Parte 03: Adicionando um circuito de proteção de sobre corrente ao regulador linear

#### Primeiramente reflita e pesquise sobre o que é sobrecorrente?

R: Sobrecorrente é um fenômeno que ocorre quando temos uma corrente acima do permitido circulando em nosso circuito, ocorrida seja por um surto elétrico ou por qualquer outro motivo, e que tem chance de danificar os componentes visto que eles foram dimensionados para uma tensão menor do que a de sobrecorrente.

#### Quais os impactos neste circuito?

R: Uma sobrecarga de corrente pode danificar a maioria dos componentes presentes no circuito da fonte, dessa forma estragando todo o projeto.

#### O que deve fazer um circuito de proteção de sobrecorrente?

R: O circuito deve impedir que essa sobrecorrente se propague no circuito, seja por meio de uma interrupção geral na corrente ou também por quaisquer outros métodos, mas sempre impedindo que a corrente acima do nominal chegue nos componentes do circuito.

#### O que é a proteção foldback?

R: O foldback tem como princípio a questão de que, quando a resistência da carga se aproxima de 0, a corrente se limita e a tensão cai, podendo causar danos aos componentes. O foldback age justamente para impedir isso de acontecer, de forma que, quando a tensão cai, o limite de corrente também vai cair, dessa forma mantendo os componentes seguros no circuito.

#### Pesquise as topologias disponíveis, caso deseja-se fazer um circuito LDO, o que devemos levar em consideração para o regulador?

R: Foi utilizado o circuito exemplo para o terceiro bloco do projeto da fonte, como segue na imagem abaixo:

![Terceiro_bloco](https://github.com/paulocvj/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Paulo%20Cezar%20Ventura%20Junior/Atividade%2004/Exemplos/Terceiro_bloco.png)
