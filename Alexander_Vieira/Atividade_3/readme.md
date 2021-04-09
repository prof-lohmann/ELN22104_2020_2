# Atividade 2
Aluno: 
* Alexsander Vieira - <alexsander_vieira@hotmail.com>
 
Professor: 
* Daniel Lohmann
 
## Amplificadores Operacionais

<p align="justify">
Amplificadores operacionais, também conhecidos como ampop, consistem fundamentalmente de amplificadores de tensão, este componente utilizado em conjunto com com o feedback de componentes externos, como resistores e capacitores, permite criar circuitos como seguidores de tensão, comparadores de tensão, filtros, entre outros.
Devido ao ampops reais possuírem desempenho muito próximo dos ampops ideais, este componente é muito fácil de ser utilizado e muito versátil em suas aplicações.
</p>

### Amplificador Operacional Ideal
<p align="center">
    <img src="ampop1.PNG" width="400">
    <br><br>    
    Figura 1 - Atividade 2
</p>

Referencia: [edisciplinas.usp.br/pluginfile.php/3874541/mod_resource/content/0/AOP.pdf, Pag 4](https://edisciplinas.usp.br/pluginfile.php/3874541/mod_resource/content/0/AOP.pdf)

<p align="justify">

 * O ampop ideal amplifica a diferença dos sinais de entrada e possui ganho teórico limitado, portanto o ampop ideal nunca satura. 
 * A impedância dos terminais de entrada seria ilimitada, permitindo que o componente não consuma corrente de seus sinais de referência.
 * O ampop ideia possui impedância de saída nula, o que permitiria que toda a tensão disponível na saída seja aplicada na carga, sem perdas no ampop semelhante a um fonte de tensão ideal.
 * O ampop ideal possui ganho infinito, permitindo a ampliação de quaisquer sinas de entrada.
 * O ganho do ampop deve ser um numero real positivo e não deve interferir com a frequencia dos sinais de entrada, nem introduzir defasagens ou atrazos.
 * O ampop ideal não deve ser sensível à temperatura.

</p>

<p align="center">
    <img src="ampop2.PNG" width="500">
    <br><br>    
    Figura 2 - Atividade 2
</p>

Referencia: [wiki.sj.ifsc.edu.br/wiki/images/8/82/2_Ampop.pdf, Pag 5](https://wiki.sj.ifsc.edu.br/wiki/images/8/82/2_Ampop.pdf)

### Amplificador Operacional - Malha Aberta

<p align="justify">
Malha aberta é uma configuração de montagem do amplificador operacional onde não é utilizada a realimentação do sinal de saída para a entrada. Este montagem em geral possui ganhos muito altos.
</p>

### Amplificador Operacional - Malha Fechada

<p align="justify">
Malha fechada é uma configuração que utiliza a realimentação do sinal de saída na entrada, geralmente na entrada negativa(inversora). Nesta configuração normalmente os ganhos são bem inferiores aos obtidos em malha aberta.
</p>

### Calculando circuitos em malha fechada

Levando em consideração as características do amplificador operacional ideal:

* Inicialmente temos;

<p align="center">
    <img src="ampop4.PNG" width="150">
</p>

* Considerando V2 igual a 0;

<p align="center">
    <img src="ampop5.PNG" width="150">
</p>

* Aplicando a malha de realimentação;

<p align="center">
    <img src="ampop6.PNG" width="200">
</p>

* Considerando o ampop ideal, a corrente em R1 deve ser a mesma em R2, pois a impedância de entrada seria infinita, logo;

<p align="center">
    <img src="ampop7.PNG" width="150">+
</p>

* Aplicando “i” a equação;

<p align="center">
    <img src="ampop8.PNG" width="250">
</p>

* Isolando o termo Vout;

<p align="center">
    <img src="ampop9.PNG" width="200">
</p>

* Levando em consideração o ganho infinito de um ampop ideal, podemos chegar ao final da equação;

<p align="center">
    <img src="ampop10.PNG" width="200">
</p>

<p align="center">
    <img src="ampop3.PNG" width="500">
    <br><br>    
    Figura 3 - Atividade 2
</p>

Referencia: [wiki.sj.ifsc.edu.br/wiki/images/8/82/2_Ampop.pdf, pag 8](https://wiki.sj.ifsc.edu.br/wiki/images/8/82/2_Ampop.pdf)

### Principais topologias

#### Buffer

<p align="justify">
A topologia Buffer ou Seguidor de tensão, permite isolar um sinal da entrada de uma carga, este processo é alcançado ao criar um estágio de ganho unitário. Neste caso V0 = V1.
</p>

<p align="center">
    <img src="ampop11.PNG" width="500">
    <br><br>    
    Figura 4 - Atividade 2
</p>

Referencia: [wiki.sj.ifsc.edu.br/wiki/images/8/82/2_Ampop.pdf, pag 11](https://wiki.sj.ifsc.edu.br/wiki/images/8/82/2_Ampop.pdf)

#### Amplificador Inversor

<p align="justify">
A topologia Amplificador inversor, permite obter uma tensão com sinal oposto ao de entrada e realizar uma amplificação ou atenuação no mesmo. Neste caso V0 = -(R2/R1)*Vin.
</p>

<p align="center">
    <img src="ampop12.PNG" width="400">
    <br><br>    
    Figura 5 - Atividade 2
</p>

Referencia: [edisciplinas.usp.br/pluginfile.php/3874541/mod_resource/content/0/AOP.pdf, pag 7](https://edisciplinas.usp.br/pluginfile.php/3874541/mod_resource/content/0/AOP.pdf)

#### Amplificador não Inversor

<p align="justify">
A topologia Amplificador não inversor, permite obter uma tensão com o mesmo sinal  ao de entrada e realizar uma amplificação ou atenuação no mesmo. Neste caso V0 = -(1+(R2/R1))*Vin.
</p>

<p align="center">
    <img src="ampop12-1.PNG" width="400">
    <br><br>    
    Figura 6 - Atividade 2
</p>

Referencia: [edisciplinas.usp.br/pluginfile.php/3874541/mod_resource/content/0/AOP.pdf, pag 8](https://edisciplinas.usp.br/pluginfile.php/3874541/mod_resource/content/0/AOP.pdf)

#### Amplificador somador inversor

<p align="justify">
A topologia Amplificador somador inversor, permite obter uma soma ponderada e invertida das tensões de entrada do amplificador. Neste caso temos:
</p>

<p align="center">
    <img src="ampop14.PNG" width="400">
    <br><br>
    <img src="ampop13.PNG" width="400">
    <br><br> 
    Figura 7 - Atividade 2
</p>

Referencia: [amorim.eng.br/aulasCE2/pdf_aulas/aula_4_AmpOp1.pdf, pag 15](https://amorim.eng.br/aulasCE2/pdf_aulas/aula_4_AmpOp1.pdf)

#### Amplificador somador não inversor

<p align="justify">
A topologia Amplificador somador, permite obter uma soma ponderada não invertida das tensões de entrada do amplificador. Neste caso temos:
</p>

<p align="center">
    <img src="ampop16.PNG" width="200">
    <br><br>
    <img src="ampop15.PNG" width="400">
    <br><br> 
    Figura 8 - Atividade 2
</p>

Referencia: [amorim.eng.br/aulasCE2/pdf_aulas/aula_4_AmpOp1.pdf, pag 19](https://amorim.eng.br/aulasCE2/pdf_aulas/aula_4_AmpOp1.pdf)

#### Amplificador Subtrator

<p align="justify">
O Amplificador subtrator tem a finalidade de amplificar as diferenças de tensões entre as entradas. Neste caso temos:
</p>

<p align="center">
    <img src="ampop17.PNG" width="500">
    <br><br> 
    Figura 9 - Atividade 2
</p>

Referencia: [edisciplinas.usp.br/pluginfile.php/3874541/mod_resource/content/0/AOP.pdf, pag 10](https://edisciplinas.usp.br/pluginfile.php/3874541/mod_resource/content/0/AOP.pdf)

#### Amplificador de Instrumentação

<p align="justify">
Esta topologia visa resolver a inconveniência da necessidade de de uma resistencia de entrada dos amplificadores subtratores, isto é realizado utilizando 2 ampops não inversores e um amplificador subtrator, assim tiramos proveito da propriedade de resistência de ser praticamente infinita.
</p>

<p align="center">
    <img src="ampop19.PNG" width="200">
    <br><br>
    <img src="ampop18.PNG" width="400">
    <br><br> 
    Figura 10 - Atividade 2
</p>

Referencia: [www.ufrgs.br/eng04030/Aulas/teoria/cap_15/circampo.htm](http://www.ufrgs.br/eng04030/Aulas/teoria/cap_15/circampo.htm)

### Ganho de malha aberto Finito

<p align="justify">
O ganho em malha aberto finito pode ser demonstrado ao compararmos o ganho nominal com o ganho em malha fechada. No exemplo abaixo o ganho nominal foi variado de -1000 a -10 para um ampop inversor e de 1000 a 10 para um não inversor. Variando Av de 10000 para 100.
</p>

<p align="center">
    <table style="width:100%">
    <thead>
    <tr >
        <th colspan="4">Inversor</th> 
        <th colspan="4">Não Inversor</th>
    </tr>
    </thead>
    <tbody>
    <tr>
        <td>Av</td>
        <td>|(-R2/R1)|</td>
        <td>|G|</td>
        <td>Erro (%)</td>
        <td>Av</td>
        <td>|(-R2/R1)|</td>
        <td>|G|</td>
        <td>Erro (%)</td>
    </tr>
    <tr>
        <td>10000</td>
        <td>1000</td>
        <td>909</td>
        <td>9,1</td>
        <td>10000</td>
        <td>1000</td>
        <td>909</td>
        <td>9,1</td>
    </tr>
    <tr>
        <td>100</td>
        <td>1000</td>
        <td>90,83</td>
        <td>90,9</td>
        <td>100</td>
        <td>1000</td>
        <td>90,9</td>
        <td>90,9</td>
    </tr>
    <tr>
        <td>10000</td>
        <td>10</td>
        <td>9,83</td>
        <td>0,2</td>
        <td>10000</td>
        <td>10</td>
        <td>9,99</td>
        <td>0,1</td>
    </tr>
    <tr>
        <td>100</td>
        <td>10</td>
        <td>9,01</td>
        <td>9,9</td>
        <td>100</td>
        <td>10</td>
        <td>9,09</td>
        <td>9,1</td>
    </tr>
    </tbody>
    </table>
</p>

<p align="center">
    <img src="ampop20.PNG" width="600">
</p>

<p align="justify">
Analisando os resultados é possível perceber que conforme o valor de Av aumenta em direção ao ganho de malha aberta menor se torna o erro.
</p>

### Tensão de modo comum (Vcm)

<p align="justify">
Tensão de modo comum, ao aplicar tensões iguais (modulo e fase identicos) as entradas de um ampop (inversora e não inversora simultaneamente) surgira em Vout a tensão em modo comum, idealmente zero.
Este parâmetro pode ser calculado utilizando as expressões abaixo:
</p>

<p align="center">
    <img src="ampop21.PNG" width="600">
</p>

<p align="justify">
Onde “Ad” representa o ganho da diferença dos sinais de entradas e Acm o ganho em modo comum.
</p>

### Razão de rejeição de modo comum (CMRR)

<p align="justify">
CMRR é uma característica muito importante para um ampop, CMRR= Ad/Acm. Como ampops trabalham como aplicações de diferenças um alto valor de CMRR é muito melhor para a correta operação, sendo assim quanto maior o valor de Acm mais prejudicial para o circuito implementado isso sera.

Exemplo da influência da tolerância dos resistores para o CMRR
</p>

<p align="center">
    <img src="ampop22.PNG" width="600">
</p>

<p align="justify">
Como é possível verificar na imagem, ao variar a resistência de realimentação em 1% e 5% o circuito passa a apresentar tensão na saída, evidenciando um leve descasamento entre as entradas.
</p>

### Limitações de tensão de entrada e saída de um ampop

<p align="justify">
Diferente do componente ideal um ampop real possui limitações físicas que são inerentes de sua construção.
</p>

<p align="center">
    <img src="ampop23.PNG" width="600">
    <br><br> 
    Figura 11 - Atividade 2
</p>

Referencia: [br.mouser.com/datasheet/2/609/LT1001-1529864.pdf, datasheet LM1001](https://br.mouser.com/datasheet/2/609/LT1001-1529864.pdf)

<p align="justify">
Como é possivel verificar na imagem acima o circuito interno de um Ampop é composto por diversos componentes, desta forma se montarmos um circuito que não respeite essas limitações podemos danificar estes componentes e afetando o funcionamento utilizado. As limitações de um ampop estão descritação em seu datasheet, usaremos como exemplo as fotos do datasheet do LM1001 abaixo
</p>

<p align="center">
    <img src="ampop24.PNG" width="650">
    <img src="ampop25png.PNG" width="650">
    <br><br> 
    Figura 11-12 - Atividade 2
</p>

Referencia: [br.mouser.com/datasheet/2/609/LT1001-1529864.pdf, datasheet LM1001](https://br.mouser.com/datasheet/2/609/LT1001-1529864.pdf)

### Ampop - Rail-to-Rail

<p align="justify">
Amplificadores operacionais Rail-to-Rail são amplificadores operacionais que possuem duas entradas V+ e V-. Desse modo suas saídas podem apresentar ganhos muito maiores com um valor absoluto menor em cada uma das entradas simétricas.
</p>

### Tensão de offset

<p align="justify">
A tensão de offset é a diferença de potencial necessária entre os terminais de entrada do amplificador para se alcançar 0V na saída do mesmo. Este parâmetro é modelado de forma a compensar o descasamento dos transistores e dos demais componentes do circuito interno do amplificador. Para um amplificador inversor basta aterrar a entrada do mesmo que a tensão de offset será apresentada na saída, o valor na saída será -(V_offset)*(ganho) por se tratar de um ampop inversor.
Para minimizar o efeito da tensão de offset podemos colocar uma fonte de tensão de sinal contrário na entrada com offset.
</p>

### Variação da tensão de offset pela temperatura

<p align="justify">
Como os transistores internos do amplificador são afetados por variações de temperatura, e o descasamento entre estes componentes resulta na tensão de offset do amplificador. Variações de temperatura podem intensificar essas diferenças e alterar o valor da tensão de offset, esta variação pode ser verificada normalmente em gráficos no datasheet do amplificador. Exemplo LM1001.
</p>

<p align="center">
    <img src="ampop26.PNG" width="350">
    <br><br> 
    Figura 13 - Atividade 2
</p>

Referencia: [br.mouser.com/datasheet/2/609/LT1001-1529864.pdf, datasheet LM1001](https://br.mouser.com/datasheet/2/609/LT1001-1529864.pdf)

### Correntes de Polarização

<p align="justify">
Correntes de polarização são correntes que saem ou entram nos terminais de entrada do amplificador, estas correntes para um amplificador ideal são iguais a zero, entretanto para um amplificador real essas correntes surgem devido a polarização dos transistores internos do amplificador. A diferença entre a corrente na entrada normal e na inversora é chamada de corrente de offset. Quando esta corrente é pequena é possível cancelar este efeito meramente ajustando as impedâncias de entrada.
Outro método de mitigar este efeito consiste em medir o valor desta corrente para adicionar ao circuito de entrada uma corrente de mesma intensidade porém com sinal oposto neutralizando a corrente de offset.
</p>

<p align="center">
    <img src="ampop27.PNG" width="600">
    <br><br> 
    Figura 14 - Atividade 2
</p>

Referencia: [www.analog.com/media/en/training-seminars/tutorials/MT-038.pdf, pag 4](https://www.analog.com/media/en/training-seminars/tutorials/MT-038.pdf)

