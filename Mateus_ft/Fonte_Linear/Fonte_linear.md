**Parte 01: Entendendo um regulador linear**

- Qual relação entre a tensão de alimentação do ampop e a tensão de saída?

Existe uma diferença de tensão entre a tensão de saída e a tensão de alimentação que deve ser respeitada, pois o ampop satura quando a tensão de saída se aproxima da tensão de alimentação. Dessa forma é importante consultar o datasheet para consultar tais informações.


- O que devemos considerar para esse circuito operar como um LDO?

Uma baixa queda de tensão no mosfet. Tendo em vista que a potência dissipada no mosfet é diretamente proporcional a corrente que por ele passa e pela diferença de potencial. 

P=V*I


- Como obter as tensões de alimentação para o AmpOp (VCC e VEE)?


Com um dobrador de tensão. Pois a tensão de alimentação do ampop precisa ser maior do que a tensão que o circuito original fornece.


- Utilizando o circuito dobrador de tensão, qual valor de VCC você obtêm para um sinal Vin+ de 12Vrms?

Vp= 12*(2/sqrt(2))
Vp= 16,97 V

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/Fonte_Linear/imagens/dobrador%20de%20tensao.png)

Vcc= 2*Vp - 2Vd

Vcc= 2*16,97 - 2*0,7

Vcc= 32,54 V

-  Quais problemas apresentam esse circuito?

Tensão de ripple na realimentação do ampop. O que ocasiona ruído na saída

- Podemos melhorar?

Sim. Adicionar um regulador linear. Assim eliminando os ruídos.


