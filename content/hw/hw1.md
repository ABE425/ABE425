---
title: "HW1"
date: 2018-04-17T13:04:56-05:00
draft: true
---

Released: 2018-01-23

Due: 2018-01-30

**NAME:**  
**HW:Thevenin Equivalents.**

**Description**

This homework contains three worked examples of increasing complexity, and three examples that you need to do. Although the examples all have numbers, you need to submit equations. Many students do not like homeworks without numbers, but the reality is that you need to have equations before you can plug in numbers anyway, so asking for numbers is only more work. In fact, the best way to solve these kinds of problems is to first write out the equations and then write a simple MatLab script to do the calculations!

**Procedure**

The procedure of the Thevenin Equivalent method is as follows:

1. Determine the Open Voltage across a,b (note ground symbol)  
2. With all sources replaced by their internal resistance, calculate the circuit's Equivalent Resistance that a ohm meter would "see" at a,b.  
3. Determine the circuit's short current through a-b by drawing in a direct connection between a,b.  
4. Verify your answer using Ohm's Law: U_open = R_eq * i_short  

As you will see in the three worked examples, you need to determine the equations for the Open Voltage, Equivalent Resistance and the Short Current. To get numerical values, we need to write a simple MatLab program. This is much faster than doing it on paper, and the computer does not make any mistakes. First we need a function called 'parallel' so we can calculate the equivalent value of two resistors in parallel: Copy these two lines in MatLab's editor and save as 'parallel.m'. As you can see it simply takes two resistors and applies the 'product over sum' rule. Now you can use this function in your homework.

```
function Rout = parallel(R1, R2)  
Rout = R1*R2/(R1 + R2);
```

![Figure1](https://github.com/ABE425/ABE425/blob/master/data/hw/HW_TheveninEquivalents/HW_Thevenin1.PNG)

**Worked example 1**

figure1 shows the circuit. It is easy to see that the two resistors make up a voltage divider. Since the Open Voltage is the voltage across resistor R_2, it is now the resistor itself, divided by the sum of the two resistors, and multiplied by the voltage drop across both of them (note that the voltage on the bottom end is zero (ground symbol) but this is not always the case!)

To determine the equivalent resistance, you replace the voltage source by its internal resistance (which is zero). Now it is easy to recognize that the equivalent resistance is the parallel circuit made up by the two resistors.

To calculate ```i_short``` you imagine point a,b being connected and the current flowing from a to b is the ```i_short```). If you connect a wire in parallel with ```R_2```, ```R_2``` no longer plays a role (the resistance of any resistor in parallel with a zero resistance is that zero resistance.) Now the short current ```i_short``` is the voltage drop across ```R_1``` divided by ```R_1``` itself:

```
U_open= R_2\(R_2+R_1)U
R_eq  = (R_2 R_1)\(R_2 + R_1)
i_short= U\R_1
```

Check:

```
U_open = R_eq * i_short = (R_2 R_1)\(R_2 + R_1) * U\R_1 = R_2\(R_2+R_1)*U
```

Now you write a program (which calls the 'parallel' function) as follows: Remember that every time you want to put two resistors R_1, R_2 in parallel simply call 'parallel(R1,R2)'.

The listing of the program for worked example 1 is given here:

```
clear all
close all
clc

U              = 12;
R1             = 10;
R2             = 20;

Uopen          = U*R2/(R1+R2)
Req            = parallel(R1, R2)
i_short        = U/R1

i_short_check  = Uopen / Req
```

The output of this program is:

```
Uopen 			    =    8
Req 			      =    6.6667
i_short 		    =    1.2000

i_short_check 	=    1.2000
```


**Worked example2**

![Figure2](https://github.com/ABE425/ABE425/blob/master/data/hw/HW_TheveninEquivalents/HW_Thevenin2.PNG)  
Figure2 shows a circuit that contains a single current source. To calculate the Open Voltage, you have to recognize that there is no current flowing through resistor ```R_2``` and therefore there is no voltage **DROP** across ```R_2```, in other words, the voltage left and right of the resistor are the same. The voltage drop across ```R_1``` is according to Ohm's law equal to ```i*R_1```, which is then also the voltage at point a.

The equivalent resistance ```R_eq``` is easy to see, since you need to replace the current source with its internal resistance (which is infinite), therefore the ```R_eq``` is the sum of the two resistors (since they are in series.)

To calculate ```i_short``` you need to recognize that this becomes a current divider (imagine point a,b connected and the current flowing from a to b is the ```i_short```). So the current through the ```R_2``` branch is now the opposite resistor divided by the sum of the resistors, multiplied by the current entering them:


```
U_open  = i R_1  
R_eq    = R_1 + R_2  
i_short = R_1\(R_1+R_2)*i  
```

Check:

```
U_open = R_eq * i_short = (R_1 + R_2)*R_1\(R_1+R_2*i = i*R_1
```

The listing of the program for worked example 2 is given here:

```
clear all
close all
clc

i              = 1.5;

R1             = 10;
R2             = 20;

Uopen          = i*R1
Req            = R1+ R2
i_short        = i*R1/(R1+R2)

i_short_check  = Uopen / Req
```

The output of this program is:

```
Uopen          = 15
Req            = 30
i_short        = 0.5000
i_short_check  = 0.5000
```


**Worked example 3**

![Figure3](https://github.com/ABE425/ABE425/blob/master/data/hw/HW_TheveninEquivalents/HW_Thevenin3.PNG)  
Figure3 shows the circuit. Here is where things get a litte more difficult, since we now have two sources, a voltage source and a current source. The trick is to use the super position principle to determine the Thevenin equivalent. What this boils down to is that during the calculation of U_open, you calculate the influence of the voltage source (while temporarily replacing the current source by its internal resistance, which is infinite) and then you do the opposite, you calculate the influence of the current source (while temporarily replacing the voltage source by its internal resistance, which is zero). Then you simply add the two influences. You do the exact same thing for the short current i_short. However you do not need to do this for the equivalent resistance, since it is not a source; You calculate the equivalent resistance by replacing both sources by their internal resistance.

For circuits like these, it is best to split it into two parts, 1) where you only have a voltage source and 2) where you only have a current source (see Figures4 and 5). Once you get good at this, you think you can see it in your head, but people are limited in the number of variables they can oversee at once. It is much better to be systematic than to rely on intuition!

![Figure4](https://github.com/ABE425/ABE425/blob/master/data/hw/HW_TheveninEquivalents/HW_Thevenin3_VoltageSource.PNG)

Figure4 shows the circuit where the current source is replaced by its internal resistance, which is infinite, therefore the whole source simply disappears.

By now you should be able to determine the ```U_open```, ```R_eq```, and ```i_short``` of the circuit. Since there is no current flowing in the entire circuit, it is clear that the voltage at point a, is equal to the voltage above the voltage source which is U.

The equivalent resistance is also simple, because any meter hooked up to point a,b will see two resistors in series (```R_1``` plays no role since there is no current running through it).

The short current is now the current flow through ```R_2``` and ```R_3``` which is equal to the voltage source divided by the sum of resistors  ```R_2``` and ```R_3```:

```
U_open   = U
R_eq     = R_2 + R_3  
i_short  = U\(R_2+R_3)  
```

Check:

```
U_{open} = R_{eq} * i_{short} = (R_2 + R_3)*U\(R_2+R_3)= U
```

![Figure5](https://github.com/ABE425/ABE425/blob/master/data/hw/HW_TheveninEquivalents/HW_Thevenin3_CurrentSource.PNG)
Figure5 shows the circuit where the voltage source is replaced by its internal resistance, which is zero, therefore the source is replaced by a wire.

Now we are going to determine the ```U_open```, ```R_eq```, and ```i_short``` of this circuit. Since there is no current flowing through ```R_3```, there is no voltage drop across it, and the voltage at point a is equal to the voltage to the left of resistor ```R_3```. Since all current flows through ```R_2```, the voltage above ```R_2``` is equal to ```i*R_2```.

The equivalent resistance is equal to the one we found before, it is not a function of the sources therefore it is equal to the sum of resistors ```R_2```, ```R_3```.

The short current can be calculated by recognizing the current divider, and therefore the current flowing through resistor ```R_3``` (which is ```i_short```) is now equal to the opposite resistor ```R_2``` divided by the sum of the resistors that make up the current divider ```R_2 + R_3```  times the current running into them which is ```i```.

```
U_open   = i R_2  
R_eq     = R_2 + R_3
i_short  = R_2\(R_2+R_3)*i
```

Check:

```
U_open = R_eq * i_short =(R_2 + R_3)*R_2\(R_2+R_3)*i = i*R_2
```

Since we have split the original circuit into two parts, we need to add the influences of the voltage and current source separately as follows (note that the equivalent resistance ```R_eq``` remains unaffected):

```
U_open  = U + i*R_2  
R_eq    = R_2 + R_3  
i_short = U*R_2+R_3 +R_2\(R_2+R_3)*i  
```

Check:

```
U_open = R_eq * i_short = (R_2 + R_3)*U\(R_2+R_3) + R_2\(R_2+R_3)*i= U + i*R_2
```

The listing of the program for worked example 3 is given here:

```
clear all
close all
clc

U              = 12;
i              = 1.5;

R1             = 10;
R2             = 20;
R3             = 30;

Uopen          = U + i*R2
Req            = R2 + R3

i_short        = U/(R2+R3) + i*R2/(R2+R3)

i_short_check  = Uopen / Req
```

The output of this program is:

```
Uopen 		  	 =42
Req 			     =50
i_short 		   =0.8400
i_short_check  =0.8400
```

**Your homework starts here.**

Figures6,7,8 show three circuits, all of them having dual sources. Use the superposition principle to calculate the Thevenin equivalents. You do not have to insert the split circuits, but you are urged to do this on a piece of paper, and don't forget to add the influence of the separate sources at the end.

_To submit this homework, you need to continue this document, and solve the problems 4,5,6 in exactly the same way as was done in the worked examples. Include the equations, as well as the MatLab code._

_**Circuit 4**_

![Figure6](https://github.com/ABE425/ABE425/blob/master/data/hw/HW_TheveninEquivalents/HW_Thevenin4.PNG)

This circuit has two sources, U_1 and U_2. If you do not like the positive sign of source U_2 at the bottom, simply put it at the top, and write yourself a note that its value is U_2' = -U_2.

```
U_open  =  
R_eq    =  
i_short =  

```
Check:

```
U_open = R_eq * i_short =  
```

The listing of the program for circuit 4 is given here:




The output of this program is:



_**Circuit 5**_

![Figure7](https://github.com/ABE425/ABE425/blob/master/data/hw/HW_TheveninEquivalents/HW_Thevenin5.PNG)

This circuit has a voltage and a current source, so you need to evaluate the influence of the two sources separately. Also, if you do not like the current flowing downward, simply reverse its direction and write yourself a note that says i' = -i.

```
U_open  =  
R_eq    =  
i_short =  

```
Check:

```
U_open = R_eq * i_short =  
```

The listing of the program for circuit 5 is given here:

The output of this program is:

_**Circuit 6**_

![Figure8](https://github.com/ABE425/ABE425/blob/master/data/hw/HW_TheveninEquivalents/HW_Thevenin6.PNG)

This circuit has two sources, use the superposition principle.

```
U_open  =  
R_eq    =  
i_short =  
```

Check:

```
U_open = R_eq * i_short =  
```

**Link**: [VISIT THE HM1](https://github.com/ABE425/ABE425/tree/master/data/hw/HW_TheveninEquivalents )

**Submission**:[SUBMIT YOUR HOMEWORK HERE]()

**Link to resource**:

[MATLAB Tutorial](../../resources/MATLAB_Guide.md)  
[LaTex_Guide](../../resources/LaTex_Guide.md)
