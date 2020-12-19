# Atividade 2

## 1) O que é o AmpOp?
AmpOp é um aplificador operacional diferencial com alto ganho, impedância muito na entrada e baixa na saída. AmpOp é um circuito integrado e é formado por resistores, transistores e geralmente também um capacitor interno. Possuem três terminais, dois de entrada e um de saída.

## 2) Mostre os simbolos e as características do AmpOp IDEAL
O AmpOp ideal temos que nenhuma corrente de entrada seja drenada, ou seja a corrente do terminal 1 e do terminal 2 são iguais a zero, sendo assim, a impedância de entrada é supostamente infinita. Possui também ganho de tensão infinito, ganho de modo comum igual a zero, insensibilidade à temperatura, resposta de frequência infinita e  impedância de saída iguala zero. Sua simbologia está representada na figura abaixo:

## 3) O que significa Malha Aberta e Malha Fechada?
O ganho de malha aberta, não há realimentação entre a saída e a entrada, o amplificador operacional diferencial mostra em sua saída um sinal resultante de uma amplificação da diferença entre os potenciais de entrada. No ganho de malha fechada há um caminho de realimentação negativo do retorno de saído do AmpOp à sua entrada. O ganho de malha fechada é sempre inferior ao de malha aberta.

## 4) Exemplifique como resolver e calcular circuitos com AmpOps em Malha Fechada

## 5) Descreva as principais características das topologias:

## a) Seguidor de Tensão (Buffer):
Fornece um meio de isolar um sinal de entrada de uma carga utilizando um ganho unitário de tensão, sem inverter a fase ou polaridade, agindo como um circuito ideal com impedância alta na entrada e baixa na saída. Temos que a tensão de saída é Vo = V1.

## b) Amplificador inversor:
Possui dois resistores de realimentação, amplifica o sinal de entrada e o sinal de saída possui polaridade invertida.

## c) Amplificador não-inversor:
A polaridade do sinal de saída é igual ao do sinal de entrada.

## d) Amplificador somador inversor: 
Permite realizar a soma dois ou mais sinais, é uma variação do amplificador inversor.

## e) Amplificador somador não-inversor: 
Possuem dois sinais ou mais de tensão conectados em paralelo na entrada não-inversora.

## f) Subtrator:  
Permite que seja obtido na saída uma tensão igual à diferença entre os sinais aplicados multiplicados por um ganho.

## g) Amplificador de Instrumentação: 
Possui como características elevado CMR, elevada impedância nas entradas e baixo offset.

## 6) Explique o efeito do ganho em MALHA ABERTA FINITO, para as topologias Amplificador Inversor e Amplificador não inversor.
## a) Exemplifique com circuitos com ganhos em malha fechada elevado (Ex. 1000V/Ve -1000V/V) e com ganhos menores (Ex. 10V/V e -10V/V ), faça a comparaçãocom erros percentuais e utilize uma variação de ganho em malha aberta entre120dB e 20dB.
Temos que a equação do AmpOp ideal seria Vo = Av (V+ - V-), tendo Av como o ganho em malha aberta. Na idealidade, temos que Av é infinito, ou seja, é necessário considerá-lo nas equações.
Para o amplificador inversor: G = Vo/Vi = (-R2/R1)/(1+(R2/R1))/Av
Para o amplificador não inversor: G = Vo/Vi = (1+(R2/R1)/(1+(R2/R1))/Av

## 7) Explique o que é a tensão de modo comum(VCM) e quais os efeitos desta tensão nas topologias estudadas.
Tensão de modo comum é a tensão média nos terminais de entrada não inversora e inversora, se esta tensão for muito baixa ou muito altas, as entradas serão fechada e a operação será encerrada. Na idealidade, a tensão de modo comum é nula e o seu efeito é um acréscimo indesejado na tensão de saída.

## 8) O que é CMRR?
CMRR significa rejeição de Modo Comum, os sinais opostos nas entradas são altamente amplificados, os sinais comuns às entradas são pouco amplificados, a conexão diferencial atenua a entrada indesejada de ruídos que é geralmente comum a ambas as entradas. 

## 9) Utilizando o Amplificador Subtrator com ganho 1000V/V, demonstre o efeito da tensãode modo comum (VCM), indicando:
## a) o impacto na tensão de saída com relação a tolerância dos resistores nocircuito;
## b) Qual erro na tensão de saída com relação CMRR do AmpOp.
## c) Dica de exemplos com valores diferentes de tensão de modo comum (VCM) . Faça o mesmo circuito com resistores com tolerâncias bem distintas, ex. 1% e 5%.

## 10) Faça um resumo explicando as limitações de tensão de entrada e saída de um AmpOp. De exemplos, utiliza-se valores de datasheet.
## a) Defina o que é um AmpOp Rail-to-rail.
AmpOp Rail-to-rail possui tensão na saída que alcança o mesmo nível que as tensões de alimentação do AmpOp, neste amplificador temos que a saturação ocorre somente no limite do valor de alimentação, positiva e negativa.



## 11) O que é tensão de offset? Como calcular o efeito resultante na tensão de saída de um amplificador inversor?
Em um AmpOp ideal, a saída é nula quando suas entradas estão em curto circuito. Já no AmpOp real, a saída pode ser diferente de zero quando as duas entradas estão no potencial zero, isso quer dizer que existe uma tensão CC equivalente na entrada que é chamada de tensão offset, o valor desta tensão está geralmente situada na faixa de 1 a 100mV. Podemos calcular através da seguinte equação Vo (offset) = V10*([R1+Rf)/R1)

## 12) Como minimizar o efeito da tensão de offset?
Para reduzir o efeito da tensão de offset é utilizado um divisor de tensão conectado ao estágio diferencial de entrada, isto vai permitir o balanceamento das correntes de base e de coletor, deve ser feito com as entradas inversora e não-inversora conectadas ao terra.

## 13) O que é a variação da tensão de offset pela temperatura?
## a) Como verificar esse parâmetro no datasheet?

É justamente a intenção de encontrar o setpoint pela temperatura do AmpOp. Como o offset se trata como um "erro" entre medidas desejadas e medidas encontradas, o offset pode variar de acordo com a temperatura. a) Como verificar esse parâmetro no datasheet?

## 14) O que são as correntes de polarização(Ibias) de AmpOp?
## a) Como minimizar o efeito destas correntes? Descreva as aproximações e os possíveis circuitos para mitigar o problema.
## b) Descreva a corrente de offset na polarização dos AmpOp.
Devido aos transistores, existem correntes não nulas através dos terminais de entradas que são as correntes de polarização, essas correntes se associam as correntes na base dos transistores bipolares e as correntes de fuga ou de saturação inversa nos transistores de efeito de campo. Resistores são utilizados para compensar os erros de tensão induzidos na saída. 











