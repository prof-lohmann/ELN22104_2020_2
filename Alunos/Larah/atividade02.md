# 1. Resumo sobre Amplificadores Operacionais.

## O que é o AmpOp?
O amplificador operacional é um dispositivo semicondutor extremamente versátil, possui características próximas as ideais.
É composto por dezenas de transistores, resistores e um capacitor interno. 
Inicialmente será tratado como um bloco construtivo para que possamos analisar suas características elétricas e aplicações.

### O AmpOp ideal:
Pode-se considerar inicialmente que o AmpOp tem três terminais: dois de entrada e um de saída, na figura os terminais 1 e 2 são de entrada e o terminal 3 de saída.

![AmpOp](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/amp.op.ideal.simbolo.JPG)

Contudo se for se considerar a alimentação teremos a configuração a seguir, onde os terminais 4 e servem como +VCC e -VEE, 
sendo que esta alimentação deve ser simétrica na maioria dos casos:

![AmpOp](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/amp.op.ideal.alimentacao.JPG)

### Características do Amp Op ideal:
* Impedância de entrada infinita;
* Impedância de saída nula;
* Ganho de modo comum nulo ou rejeição de modo comum infinita;
  * Se as tensões de entrada forem iguais a tensão de saída será zero.
* Ganho de malha aberta infinito;
* Largura de faixa de resposta em frequência infinita.


### O que significa Malha Aberta e Malha Fechada?
Malha **aberta** é quando o circuito do amp op possui uma configuração **sem realimentação** do retorno da saída do amp-op à sua entrada.
Já a malha **fechada** é uma configuração que tem um caminho de **realimentação negativa ou positiva** do retorno de saída do amp-op à sua entrada.

![](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/amp.op.ideal.realimentacao.negativa.JPG)

A figura acima mostra um amp op com configuração de realimentação negativa.

### Exemplifique como resolver e calcular circuitos com AmpOps em Malha Fechada.

### Descreva as principais características das topologias:
#### a) Seguidor de Tensão (Buffer)
![](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/amp.op.buffer.simbolo.JPG)

Possui ganho unitário G=1 o que implica em ter Vo igual a Vin e pode ser utilizado, por exemplo, em conjunto com multiplexadores, quando se desejar selecionar determinada entrada e não alterar o seu valor na saída. Em um ampop ideal o buffer terá impedância de saída nula e impedÂncia de entrada infita, sendo que em um modelo real buscasse aproximar ao máximo destas características.

#### b) Inversor

Possui ganho G = -R2/R1, com alta impedância de entrada, baixa impedancia de saída, ganho estável e tensão de saída amplificada defasada de 180 graus em relação a tensão de entrada.

#### c) Não Inversor

Possui ganho G = 1 + R2/R1, com alta impedancia de entrada, baixa impedância de saída e ganho estável.

#### d) Somador inversor
Possui ganho G = -Rf*(V1/R1 + V2/R2+...+Vn/Rn), usando da realimentação negativa e do terra virtual consegue-se obter o inverso de uma soma ponderada das entradas como resultado na saída.

#### e) Somador não inversor


#### f)Subtrator

#### g) Amplificador de instrumentação

### Explique o efeito do ganho em MALHA ABERTA FINITO, para as topologias Amplificador Inversor e Amplificador não inversor.

#### a) Exemplifique com circuitos com ganhos em malha fechada elevado (Ex. 1000V/V e -1000V/V) e com ganhos menores (Ex. 10V/V e -10V/V ), faça a comparação com erros percentuais e utilize uma variação de ganho em malha aberta entre 120dB e 20dB.

### 7. Explique o que é a tensão de modo comum(VCM) e quais os efeitos desta tensão nas topologias estudadas.

### 8. O que é CMRR?

### 9. Utilizando o Amplificador Subtrator com ganho 1000V/V, demonstre o efeito da tensão de modo comum (VCM), indicando:

#### a) o impacto na tensão de saída com relação a tolerância dos resistores no circuito;

#### b) Qual erro na tensão de saída com relação CMRR do AmpOp.

#### c) Dica de exemplos com valores diferentes de tensão de modo comum (VCM) . Faça o mesmo circuito com resistores com tolerâncias bem distintas, ex. 1% e 5%. Atividade 01 2/2

### 10. Faça um resumo explicando as limitações de tensão de entrada e saída de um AmpOp. De exemplos, utiliza-se valores de datasheet.

#### a) Defina o que é um AmpOp Rail-to-rail.

### 11. O que é tensão de offset? Como calcular o efeito resultante na tensão de saída de um amplificador inversor?

### 12. Como minimizar o efeito da tensão de offset?

### 13. O que é a variação da tensão de offset pela temperatura?

#### a) Como verificar esse parâmetro no datasheet?

### 14. O que são as correntes de polarização(Ibias) de AmpOp?

#### a) Como minimizar o efeito destas correntes? Descreva as aproximações e os possíveis circuitos para mitigar o problema.

#### b) Descreva a corrente de offset na polarização dos AmpOp.



