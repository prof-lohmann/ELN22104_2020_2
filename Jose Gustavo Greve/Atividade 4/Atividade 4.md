## Nome: José Gustavo dos Santos Greve 
## Professor: Daniel Lohmann 

## Objetivos
## Integração dos blocos de uma fonte linear.

## Introdução 
### Neste roteiro iremos integrar os circuitos estudados anteriormente, para isso, revise os conceitos de reguladores LDO e tenha em mãos os roteiros anteriores. 

## Parte 1: Entendendo um regulador linear
## 1.1) a)	Qual relação entre a tensão de alimentação do ampop e a tensão de saída? 
### Sabe-se que o ampop tem um limite de saturação, por isso a tensão de saída do ampop esta diretamente relacionada a tensão de alimentação, uma vez que a tensão máxima de saída será levemente menor que a tensão de alimentação do ampop.
### b) O que devemos considerar para esse circuito operar como um LDO? Como obter as tensões de alimentação para o AmpOp (VCC e VEE)?
### Para que possa operar como LDO a queda de tensão na saída deve ser baixa, geralmente, 0,1V a 0,5V. A tensão de saída está diretamente ligada a tensão de referência e a relação dos resistores, logo Vout=Vref(1+R1/R2). as características elétricas do ampop devem ser retiradas do DATASHEET e para o amplificador em questão, LM324 a alimentação pode ser de +-16V ou 0 a 32Vcc. para se obter a tensão desejada se utilizou da tipologia dobrador de tensão, sendo assim a tensão será de VP = (2*12*2^1/2)-0,7=33,3 V.
## 1.2) Circuito proposto (01) para a alimentação do AmpOp:
### a) Considerando a queda de tensão nos diodos D4 e D5, em 0,7 V, cada componente.
### Vcc=2*Vinp-VD4-VD5
### Vcc=(12*2√2)-1,4
### Vcc=32,54 V
### b)Quais problemas apresentam esse circuito? 
### No circuito temos dois capacitores indicados, C2 e C3. Dessa forma para escolher seus valores,devemos levar em consideração os efeitos de ripple que irá ser inserido no sinal da tensão. 
### Ainda, conforme calculado anteriormente o circuito é um dobrador de tensão, ou seja, pequenas variações do sinal de entrada Vin, pode provocar efeitos graves no funcionamento do AmpOp,
### pois esse mesmo sinal será aplicado no VCC do AmpOp (podendo saturar o sinal saída ou mesmo danificá-lo permanentemente).
### c) Podemos melhorar?
### Para melhorar o circuito podemos fazer o balanço correto na escolha do capacitor, também podemos adicionar um regulador linear de tensão na saída do dobrador, limitando a tensão de saída que irá alimentar o ampop.
## Parte 1.3)
### Sabendo que o ampop possui um limite de saturação, desta forma a tensão de saída do ampop está diretamente relacionada à tensão de alimentação. A tensão máxima de saída será um pouco menor que a tensão de alimentação  do ampop.
### Se a intenção for que o circuito consiga operar como LDO, precisamos que a queda de tensão na saída seja baixa, como por exemplo entre 0,1V e 0,5 V. Além disto, a tensão de saída está diretamente ligada a tensão de referência e à relação dos resistores, ou seja :
### Vou= Vref (1+ R1/R2)
### Em relação ao ampop, precisamos extrair as características elétricas do DATASHEET, já para o amplificador LM324, a alimentação de ± 16V ou de 0 a 32Vcc. Para encontrar a tensão esperada foi utilizada a tipologia dobrador de tensão, desta forma a tensão será de:
### VP= (2*12*√2) -(0,7) = 33,3 V
### Para saber  qual tensão teremos para um sinal Vin+ de 12Vrms e utilizando o circuito dobrador, quais problemas tem o circuito e como podemos melhorá-lo precisamos inicialmente achar o capacitor para o circuito, considerando sua corrente de 0,5A apenas para alimentação dos ampop, além dos valores abaixo:
### Vp=33, 3V   f= 60Hz   Vr= 10% de Vp
![figura01](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Atividade%204.md/image.png)
![figura2](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Atividade%204/Figura%202%20atividade%204.PNG)
### É possível perceber que o valor obtido, Vr = 3,04 V, está um pouco abaixo do valor calculado, V r= 3,3 V. Desta forma, o circuito precisa ser melhorado para encontrar um valor de tensão mais constante, a fim de reduzir a tensão de ripper na entrada do ampop, já que este é o problema crucial.
### Além disso, devemos ressaltar que a corrente de picos nos diodos, quando o circuito foi ligado, marca aproximadamente 15A, muito abaixo do valor do informado no DATASHEET do  diodo, 30A. A importância disto se dá no caso de acontecer uma elevação excessiva dos capacitores, de forma com que a corrente de pico fique com um valor muito elevado, ficando sujeita a queima dos diodos.
![figura3](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Atividade%204/Figura%203%20atividade%204.PNG)
![figura4](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Atividade%204/image.png)
## Circuito proposto (02) para a alimentação do AmpOp:
### Considere: AmpOp LM324, MOSFET IRF540, VOUT = 15V, IOUT = 1A, vin+ = 12Vrms, vripple pós-retificador =1V, considere as quedas de tensão nos diodos de 0,7V.
![figura5](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Atividade%204/Figura%205%20atividade%204.PNG)
### Tensão de saída(Vout) após inclusão de alguns componentes.
![figura6](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Atividade%204/Figura%206%20atividade%204.PNG)
### Observa-se que a tensão Vout está com um pequeno ripper na saída de aproximadamente 20uV. A alimentação do amplificador pode ser melhorada colocando os capacitores C2 E C3 de maior valor no dobrador de tensão o que diminuirá consideravelmente o ripper, mas com valores cada vez maior o tempo para entrarem regime permanente também aumenta tornando-se elevado demais. outra forma é incluir um transistor com alto ganho E com um pequeno capacitor o que deverá deixar a tesão com menor ripper, além de incluir um potenciômetro em paralelo com D6 para regular a fonte de 0 a 27V.
## Parte 02 Calculando e dimensionando outros componentes.
### a) Para o primeiro bloco (D1, D2 e C1) considere vin+ = 12Vrms, vripple_pós_retificador = 1V e I_carga =1,1A. (Vide roteiro 02)
### b) Circuito referência de tensão zener (R1 e D3): Ver roteiro 03. Podemos melhorar esse circuito?
![figura7](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Atividade%204/Figura%207.PNG)
![figura8](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Atividade%204/Figura8.PNG)
### Tensão e Corrente de saida.
![figura9](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Atividade%204/Figura%209.PNG)
### Foram escolhidos os transistores PNP 2SA1774 para a fonte de corrente por possuírem um hfe de 300 e com a potência devida pelo circuito.
### Tensão de saída do regulador após inserção dos componentes.
![figura10](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Atividade%204/Figura%2010.PNG)
### Tensão de saída do regulador após inserção de uma carga de 15 Ohms para simular uma I=1A.
![figura11](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Atividade%204/Figura11.PNG)
### Podemos verificar que corrente de saída realmente está próxima a 1A e Vr está em, aproximadamente, 7,5uV. o que permite verificar que a tensão RMS quase não sofreu alteração com a inclusão da carga.
### Quais problemas podemos identificar nesta topologia? Sugestão de melhoria:
### O principal problema da fonte de corrente do circuito está em depender do hfe e nas pequenas diferenças características de cada transistor fazendo com que possa haver uma leve variação de tensão VCE. Uma forma de melhorar o circuito seria usar um potenciômetro em paralelo com o diodo D3 o que permitiria ter um melhor controle sobre a tensão de saída.

## Parte 03
### Adicionando um circuito de proteção de sobre corrente ao regulador linear.
### a) Primeiramente reflita e pesquise sobre o que é sobrecorrente?
### Sobrecorrente é definida como sendo qualquer corrente elétrica que flui por um equipamento com magnitude acima da qual o equipamento foi projetado para funcionar. As sobrecorrentes podem ser sob a forma de uma sobrecarga ou curto-circuito.
### b) Quais os impactos neste circuito?
### Uma elevada corrente num circuito certamente queimará alguns componentes podendo ser os diodos, transistores, resistores ou até mesmo o transformador que outrora fora projetado para um limite máximo de 2A, mas com a concepção feita no circuito com proteção de sobrecorrente a queima dificilmente ocorrerá, uma vez que foi feito um circuito para proteção da fonte e caso haja elevação na carga ou um curto circuito na saída da fonte está ira diminuir a tensão de saída para que não aconteça nenhum problema.
### c) O que deve fazer um circuito de proteção de sobrecorrente?
### Como diz a nomenclatura o circuito deve ser capaz de atuar quando a corrente na saída seja maior que a projetada para o circuito seja por sobrecarga ou por curto circuito. Para o projeto em questão a fonte foi projetada para 15W, 1A tendo seu limite de atuação quando a corrente do circuito ultrapassar 1,2A.
### d) O que é a proteção foldback? Pesquise as topologias disponíveis, caso deseja-se fazer um circuito LDO, o que devemos levar em consideração para o regulador?
### Foldback é o método usado em fontes de alimentação para protegê-las de situações atuais, como curto-circuito na saída com um fio ou conexão de muitos equipamentos à fonte de alimentação.
### Com a corrente normal (lado alto) limitando, há uma tampa de corrente dura que o suprimento é limitado para protegê-lo. À medida que a resistência da carga se aproxima de 0, a corrente é limitada a um valor fixo e a tensão começa a cair. Isso pode causar uma grande quantidade de dissipação de energia no suprimento.
### Com a proteção foldback, quando a tensão cai, o limite de corrente também cai de maneira bastante linear. Isso fornece proteção mais segura contra curtos-circuitos, pois um curto-circuito "muito ruim" resultará em muito pouco consumo de corrente, para que o suprimento não fique sentado assando na corrente máxima.






