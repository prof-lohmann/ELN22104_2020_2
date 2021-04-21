# Parte 01: Entendendo um regulador linear

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



## Projeto do circuito de alimentação do ampop:

Ampop utilizado: LM324

Datasheet utilizado: https://www.ti.com/lit/ds/symlink/lm324.pdf?ts=1618824027289&ref_url=https%253A%252F%252Fwww.ti.com%252Fproduct%252FLM324

- Qual a Tensão VGS? Descreva como obter o valor.

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/Fonte_Linear/imagens/vgs_idreno.png)

Conforme o datasheet a tensão Vgs para uma corrente de 1A é de 4V.


- Qual a corrente de alimentação do AmpOp?

Como especificado no datasheet:

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/Fonte_Linear/imagens/icc_.png)

Corrente de alimentação(Icc)= de 1mA até 3mA

- Qual a tensão de alimentação do AmpOP?


![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/Fonte_Linear/imagens/supplyvoltage.png)

Supply voltage(Vcc) = 32 V (máx)

Vee= 0V (gnd) no projeto


- Qual fator devo considerar para escolher o transistor Q1?

O beta precisa ser bastante elevado.
```
Beta= Ic/Ib
Beta^^^
Ic= Ie
```

- Qual valor da tensão do diodo zener D6?
  
  Considerando que a tensão de saída do ampop deve ser de 21V. Pois Vgs=4V
  
  Logo 15+4= 19V
  A tensão do diodo zener deve ser maior que 19V.
  
  Ainda deve se observar que no datasheet a tensão Vcm= Vcc-2
  
  ![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/Fonte_Linear/imagens/vcm.png)
  
  
- Como escolher o diodo zener D6, maximizando a eficiência energética e
minimizando os ruídos no circuito?

Escolhendo um diodo zener que passe a menor corrente possível. Para isso precisa ser um zener com um resistor de zener pequeno

**Projeto no ltspice:**

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/Fonte_Linear/imagens/alimenta%C3%A7ao%20opamp.png)



