# Integração dos blocos de uma fonte linear

# Parte 01: Entendendo um regulador linear # 


![figura01](https://github.com/joananana/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Joana%20Wasserberg/ANP_04/figura%201.PNG)

### Considerando o circuito da figura 01 que representa uma fonte linear com regulador MOSFET, temos o seguinte problema: Qual relação entre a tensão de alimentação do ampop e a tensão de saída?

A tensão de alimentação deve ser consultada no datasheet dos AmpOps para que a tensão de saída não sature no AmpOp. Para o Mosfet trabalhar como chave fechada, ele precisa estar na tensão de saturaçãoO AmpOp, no caso a tensão Vgs.

### O que devemos considerar para esse circuito operar como um LDO? 

O LDO (Low Dropout Voltage) é um regulador de tensão que ameniza a Tensão de Ripple do sinal, para operar como um LDO a tensão de saída deve ter uma diferença mínima da tensão de entrada.

### Como obter as tensões de alimentação para o AmpOp (VCC e VEE)?

O AmpOp deve ter na entrada um circuito dobrador de tensão, cujo funciona como um multiplicador de tensão.

![figura02](https://github.com/joananana/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Joana%20Wasserberg/ANP_04/figura%202.PNG)

### Circuito proposto (01) para a alimentação do AmpOp: Utilizando o circuito dobrador de tensão, qual valor de VCC você obtêm para um sinal Vin+ de 12Vrms? Quais problemas apresentam esse circuito? Podemos melhorar?

Dado o valor eficaz da tensão 12V, a tensão de pico é 17, como o dobrador de tensão multiplica o valor de tensão, VCC será em torno de 32V. 
Um dos problemas apresentado é o ripple do sinal de entrada, para melhorar teriamos que inserir um retificador de sinal.


![figura 03](https://github.com/joananana/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Joana%20Wasserberg/ANP_04/figura%203.PNG)

### Projetando o circuito de alimentação do AmpOp? Considere: AmpOp LM324, MOSFET IRF540, VOUT = 15V, IOUT = 1A, vin+ = 12Vrms, vripple_pós_retificador = 1V, considere as quedas de tensão nos diodos de 0,7V.

+ Qual a Tensão VGS? Descreva como obter o valor.

Para obter esse valor, verificamos no datasheet. A tensão VGS para uma corrente de 1A é de 4V.

+ Qual a corrente de alimentação do AmpOp?

Corrente de alimentação de 1.4mA até 3mA

+ Qual a tensão de alimentação do AmpOP?

Tensão de alimentação  +/- 16V  até 32V

+ Qual fator devo considerar para escolher o transistor Q1?

O valor de Beta do transistor precisa ser alto, para possuir uma corrente de emissor


+ Qual valor da tensão do diodo zener D6?

A tensão no diodo zener precisa ser maior que a tensão de saída do AmpOp. Considerando a tensão de saída de 19V, a do diodo precisa ser maior.


+ Como escolher o diodo zener D6, maximizando a eficiência energética e minimizando os ruídos no circuito?

Escolhendo um Diodo zener que possua uma resistência baixa, para ter a menor corrente possível, minimizando os ruídos.


+ Considere que, por alterações futuras no circuito, o AmpOp poderá ter uma aumento de 10mA na corrente de alimentação, o circuito proposto continuará
funcionando?

Sim, o circuito continuara operando quando a corrente de entrada for maior que a mínima corrente citada no datasheet.

# Parte 02: Calculando e dimensionando os componentes

## a) Para o primeiro bloco (D1, D2 e C1) considere vin+ = 12Vrms, vripple_pós_retificador = 1V e I_carga = 1,1A. 

Utilizando um capacitor retificador de onda completa, utilizamos a fórmula:

```
C1 = Icarga/ 2 * F * Vripple = 9.2 mF
```
Para o díodo devemos analisar corrente de pico, tensão reversa

## b) Circuito referência de tensão zener (R1 e D3):

+ Quais fatores devo considerar para escolher o diodo zener para essa aplicação?

A resistência do zener deve ser baixa para não possuir muito ruído.

+ Qual a influência da regulação de linha e da regulação de carga para este circuito?

Nesse circuito, não temos regulação de carga.

+ Qual o impacto da regulação linha / carga do circuito com o diodo zener na tensão de saída do regulador linear?

A regulação de linha e carga definem a eficiência do regulador, para a regulação de linha a resistência de zener tem de ser baixa e para regulação de carga a tensão de zener tem de ser baixa.

+ Podemos melhorar esse circuito? Quais problemas podemos identificar nesta topologia?

Podemos melhor o circuito colocando uma fonte de corrente, mantendo uma corrente constante sobre o zener. Deixando a tensão mais estável possível.


## c) Escolhendo o transistor M1 e calculando R2 e R3.

+ Qual a corrente contínua necessária?

A corrente contínua necessária é de 1A

+ Quais os limites de tensão para este circuito?

A tensão VGS será limitada pela saída do AmpOp menos a tensão de saída. E a maior tensão aplicada nos resistores é a tensão de saída, sendo que para projeto vale 15 V



# Parte 03: Adicionando um circuito de proteção de sobre corrente ao regulador linear.



+ O que é sobrecorrente? Quais os impactos neste circuito? O que deve fazer um circuito de proteção de sobrecorrente? 

Sobreccorente é a circulação de excesso de corrente no circuito. Quando o circuito suporta até uma certa corrente, precisamos de uma proteção caso haja correntes superiores ao que o circuito suporta entrando ele tenha uma proteção para não queimar o circuito. Dessa forma, podemos 

+ O que é a proteção foldback?

A proteção foldback faz com que quando a tensão do circuito cai, o limite de corrente também cai de maneira linear. Isso fornece uma proteção segura contra curtos-circuitos.


