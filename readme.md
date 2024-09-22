# SSC0108 - Prática Sistemas Digitais

[Projeto 1: Latches, Flip-flops, and Registers.](./lab3.pdf)

### ALUNOS

|        Nome                         |    NUSP   |       
|:-----------------------------------:|:---------:|  
|   Artur Domitti Camargo             |  15441661 |   
|   Lucas Mello Ciosaki       	      |  14591305 |   
|   Lucas Alves da Silva		         |  11819553  | 

### PART I

[RTL VIEWER FOR PART I](./part1.pdf)

[TECHNOLOGY MAP VIEWER FOR PART I](./part1tmv.pdf)

SIMULATION PART I
<img src="sim1.png">

VHDL CODE
LIBRARY ieee;
USE ieee.std_logic_1164.all;

ENTITY part1 IS
  PORT ( Clk, R, S : IN STD_LOGIC;
  Q : OUT STD_LOGIC);
END part1;

ARCHITECTURE Structural OF part1 IS
  SIGNAL R_g, S_g, Qa, Qb : STD_LOGIC ;
  ATTRIBUTE KEEP : BOOLEAN;
  ATTRIBUTE KEEP OF R_g, S_g, Qa, Qb : SIGNAL IS TRUE;
BEGIN
  R_g <= R AND Clk;
  S_g <= S AND Clk;
  Qa <= NOT (R_g OR Qb);
  Qb <= NOT (S_g OR Qa);
  Q <= Qa;
END Structural;

### PART II

[RTL VIEWER FOR PART II](./part2.pdf)

[TECHNOLOGY MAP VIEWER FOR PART II](./part2tmv.pdf)

SIMULATION PART II

<img src="sim2.png">

VHDL CODE 

### PART III

[RTL VIEWER FOR PART II](./part3.pdf)

[TECHNOLOGY MAP VIEWER FOR PART II](./part3tmv.pdf)

SIMULATION PART III

<img src="sim3.png">

VHDL CODE

### PART IV

[RTL VIEWER FOR PART II](./part4.pdf)

[TECHNOLOGY MAP VIEWER FOR PART II](./part4tmv.pdf)

SIMULATION PART IV

<img src="sim4.png">

