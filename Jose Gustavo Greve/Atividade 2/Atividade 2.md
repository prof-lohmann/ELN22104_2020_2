# Instituto Federal de Santa Catarina
## Curso: Engenharia Elétrica
## Aluno: José Gustavo dos Santos Greve
### 1) O amplificador operacional, é um circuito integrado, capaz de amplificar um sinal de entrada, e é capaz de realizar operações matemáticas, como por exemplo soma, subtração, derivação. integração e multiplicação.
### 2) O amplificador operacional ideal tem um ganho infinito em malha aberta, largura de banda infinita, impedância de entrada infinita, impedância de saída nula e nenhum ruído, assim como offset de entrada é zero e nenhuma interferência térmica.
![](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Atividade%202/image.png)
### 3)	Malha aberta: uma configuração sem realimentação do retorno da saída do amp-op à sua entrada. O ganho do amp-op de malha aberta geralmente excede 10.000.
### Malha fechada: uma configuração que tem um caminho de realimentação negativo do retorno de saída do amp-op à sua entrada.
### 4)
### 5)a) Tem como o sinal de saída o reflexo do sinal de entrada. Sua função é basicamente refletir a tensão e isolar os estágios do circuito.
![](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Atividade%202/buffer.PNG)
### b)No inversor, o sinal de entrada é refletido no eixo horizontal e amplificado, gerando assim o sinal de saída. A entrada do sinal deverá ser aplicada no terminal negativo do amplificador.
![](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Atividade%202/inversor.PNG)
### c) No amplificador não-inversor, o sinal de saída terá apenas um ganho proporcional ao sinal de entrada deste circuito.O sinal de entrada é posicionado no terminal positivo do amplificador, enquanto os resistores são colocados entre a referência e o terminal negativo do amplificador.
![](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Atividade%202/nao-inversor.PNG)
### d) Esta configuração possui uma característica diferente dos anteriores, que é a realimentação dada pelo resistor RF.
![](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Atividade%202/somador%20inversor.PNG)
### e) Neste amplificador operacional, a tensão de saída não sofre inversão.
![](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Atividade%202/somador%20nao%20inversor.PNG)
### f) Sua aplicação é inversa ao somador, tendo sua montagem base semelhante a figura abaixo.
![](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Atividade%202/subtrator.PNG)
### g) Um circuito que fornece uma saída baseado na diferença entre duas entradas. Um potenciômetro é utilizado para ajustar o fator de escala do circuito.
![](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Atividade%202/Amplificador%20para%20instrumenta%C3%A7%C3%A3o.PNG)
### 6)
### 7) Tensão de modo comum de entrada (Vcm) é a média das tensões das entradas do ampop. Na prática, a tensão de saída de um amplificador operacional depende do nível médio, ou de modo comum, do sinal aplicado nas entradas. Esta dependência, designada Ganho de Modo Comum, indica basicamente que a tensão na saída é uma função não apenas da diferença de potencial entre os terminais positivo e negativo da entrada, mas também do nível médio comum a ambos.
### 8) Trata-se de uma característica dos amplificadores operacionais. Quando dois sinais da mesma amplitude, frequência e fase são aplicados às entradas (inversora e não inversora) de um operacional eles devem se cancelar e nenhuma saída deve ocorrer.
### 9) 
### 10) a) As limitações das tensões de entrada e saída são dadas pela tensão de alimentação do amp op que está sendo aplicado no sistema. Quando atinge o valor da tensão de alimentação, ocorre o efeito de saturação, ou seja, a tensão de saída fica limitada ao valor da tensão de alimentação do componente. O AmpOp Rail-to-rail opera assim, tendo o minímo possível de perda no valor de alimentação.
### 11) Tensão de "offset" - A saída de um amplificador operacional ideal é nula quando suas entradas estão em curto circuito. Nos amplificadores reais, devido principalmente a um casamento imperfeito dos dispositivos de entrada, normalmente diferencial, a saída do amplificador operacional pode ser diferente de zero quando ambas entradas estão no potencial zero. Significa dizer que há uma tensão C.C. equivalente, na entrada, chamada de tensão de "offset". O valor da tensão de "offset" nos amplificadores comerciais estão situado na faixa de 1 a 100 mV. Os componentes comerciais são normalmente dotados de entradas para ajuste da tensão de "offset".
### 12) Pelo fato de os ampops serem dispositivos diretamente acoplados com alto ganho cc, eles estão propensos a problemas em cc. O primeiro desses problemas é a tensão de offset (desequilíbrio) cc. Considere o seguinte experimento teórico: se os dois terminais do ampop forem ligados juntos e conectados ao terra, será observada uma tensão cc finita na saída. Na realidade, se o ampop tem alto ganho cc, a saída poderá estar em um de dois níveis possíveis de saturação, positivo ou negativo. A saída do ampop pode retomar ao seu valor ideal de 0V conectado-se uma fonte cc de polaridade e valor apropriados entre seus dois terminais de entrada. Essa fonte externa compensa a tensão de entrada de offset do ampop. Portanto, a tensão de offset de entrada Vos deve ser de valor igual, mas de polaridade oposta à tensão aplicada externamente. A tensão de offset resulta de um inevitável desequilíbrio presente no estágio diferencial da entrada (interno ao ampop). A preocupação é o efeito de Vos sobre a operação em malha fechada dos circuitos com ampop. Observamos que os ampops de uso geral exibem Vos na faixa de 1 a 5mV . 
### 13) Também, o valor de Vos depende da temperatura. Os catálogos de ampop especificam geralmente valores típicos e máximos de Vos para a temperatura ambiente, assim como o coeficiente de temperatura de Vos(em geral, em µV /◦C). Eles, contudo, não especificam a polaridade de Vos porque os descasamentos entre componentes que fazem surgir Vos não são conhecidos a priori; diferentes amostras de ampops do mesmo tipo podem exibir polaridades positivas ou negativas de Vos.
### 14) Independentemente do fato de que os amplificadores operacionais apresentarem uma resistência de entrada não infinita, característica que se associa apenas aos sinais dinâmicos aplicados, a natureza própria dos transístores obriga à existência de correntes não nulas através dos terminais de entrada, IBias+ e IBias-, designadas correntes de polarização, também, distintas entre si (estas correntes associam-se à corrente na base dos transístores bipolares, e às correstes de fuga ou de saturação inversa nos transístores de efeito de campo).
### a) Na prática, a existência das correntes de polarização obriga à utilização de componentes externos adicionais, tipicamente resistências, como forma de compensar os erros de tensão induzidos na saída.




