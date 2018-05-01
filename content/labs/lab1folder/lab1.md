---
title: "Lab 1"
date: 2018-04-17T13:05:05-05:00
draft: false
---

## Circuit Analysis

Lab date: 01/19/2018

Due date: 01/26/2018


#### Lab Objectives:  
1. To understand how to read resistor values using the color coding system
2. To measure the true value of resistors using a handheld Digital Multimeter (DMM)
3. To build a simple resistor circuit using a standard breadboard
4. To measure voltage drops across resistors using the DMM
5. To measure current ﬂowing in a branch
6. To understand why measuring voltages is safe, since the internal resistance of the meter in that setting is near inﬁnite (at least 107Ω or 10 MegaOhm )
7. To understand why measuring current can be dangerous, since the internal resistance of the meter in that setting is zero, and shortcuts can be easily made.
8. To understand and verify the three basic circuit laws being i) Ohm’s Law, ii) Kirchoﬀ’s Voltage Law (KVL) and iii) Kirchoﬀ’s Current Law (KCL)

#### Equipment:  
1. Power supply
2. Bread board
3. Resistors, 1k, 2.7k, 4.7k, 10k
4. Handheld Digital Multimeter (DMM)

#### Procedures:  
Measure the exact values of the resistors using the handheld DMM, and determine the color coding of the resistors using Figure 2 and Figure 3. To determine the value of a resistor use the following equation: R = ab∗10c ±d%. Example: If a resistor has the color coding Yellow-Violet-Red-Gold, then a = 4, b = 7, c = 2 and d = 5 %. The value of the resistor is now 47∗102 = 4.7k±5%. Fill out the following table:

![Table 1: To be filled with resistor color coding values.](http://localhost:1313/labs/lab1folder/Lab1_Table1.PNG)

The breadboard is organized as shown in Figure 1: There are three binding posts, on which we will connect the 10 V DC power supply (positive is red, ground is black).

![Figure 1: Typical bread board for experimental circuit construction.](http://localhost:1313/labs/lab1folder/Lab1_BreadBoard.png)
**Figure 1**: Typical bread board for experimental circuit construction.

![Figure 2: Resistor Color Coding Chart.](http://localhost:1313/labs/lab1folder/Lab1_ResistorColorCoding.png)
**Figure 2**: Resistor Color Coding Chart.

![Figure 3: Resistor Color Coding Table.](http://localhost:1313/labs/lab1folder/Lab1_ResistorColorCodingTable.png)
**Figure 3**: Resistor Color Coding Table.

#### Circuit Measurements:  
1) Hook up the circuit as shown below on the breadboard. When you are done, let the TA or instructor check your work.
2) Turn on the power supply with the input dials all the way down (CCW) and slowly adjust the power supply to 10V.
3) Measure the voltages across all resistors as shown in Figure 4; keep the red DMM wire on top. Fill out the table:

![Table 2: To be filled with measured voltages](http://localhost:1313/labs/lab1folder/Lab1_Table2.PNG)
VOLTAGE MEASUREMENTS ARE SAFE, SINCE IN THIS MODE THE INTERNAL RESISTANCE OF THE METER IS NEAR INFINITE.

![Figure 4: Circuit1. Ask yourself how much current is ﬂowing in the 10k branch.](http://localhost:1313/labs/lab1folder/Lab1_Circuit1.png)
**Figure 4**: Circuit1. Ask yourself how much current is ﬂowing in the 10k branch.

4) Measure the current ﬂowing into the 2.7k resistor as shown in Figure 5. CURRENT MEASUREMENTS ARE POTENTIALLY DANGEROUS BECAUSE IN THIS MODE THE INTERNAL RESISTANCE OF THE METER IS ZERO, SO PAY CLOSE ATTENTION.
* Remove the top wire of the 2.7k resistor
* Turn your DMM to Current measurement and move the red wire to Current Measurement
* Connect your meter between the positive binding post and the loose end of the resistor
* Measure the current and ﬁll out the table:

![Table 3: To be filled with the measured current](http://localhost:1313/labs/lab1folder/Lab1_Table3.PNG)

* **Immediately move the red wire of the DMM back to Voltage measurement and turn the dial to DC Voltage measurement.** Measure the voltage drops across the following resistors and ﬁll out the table:

![Table 4: To be filled with the measured voltage drops over the given resistors](http://localhost:1313/labs/lab1folder/Lab1_Table2.PNG)

![Figure 5: Circuit2. Measure the current into the 2.7k resistor, after the measurement set your DVM back to Voltage measurement.](http://localhost:1313/labs/lab1folder/Lab1_Circuit2.png)
**Figure 5**: Circuit2. Measure the current into the 2.7k resistor, after the measurement set your DVM back to Voltage measurement.

5) Repeat the voltage measurements with the 1k resistor placed in series with the 10k resistor as shown in Figure 6. Fill out the table:

![Table 5: To be filled with the measured voltage drops over the given resistors](http://localhost:1313/labs/lab1folder/Lab1_Table4.PNG)

![Figure 6: Circuit3. Connect a 1k resistor in series with the 10k resistor. Measure the voltages across all resistors](http://localhost:1313/labs/lab1folder/Lab1_Circuit3.png)
**Figure 6**: Circuit3. Connect a 1k resistor in series with the 10k resistor. Measure the voltages across all resistors.

6) Measure the current ﬂowing into the 1k resistor, the 4.7k resistor and into the 10k+1k branch as shown in Figure 7. Fill out the table:

![Table 6: To be filled with the measured voltage drops over the given resistors](http://localhost:1313/labs/lab1folder/Lab1_Table5.PNG)

![Figure 7: Circuit4. Measure the current into the 2.7k resistor, the 4.7k resistor and the branch containing the 10k and 1k resistor. After the measurement set your DVM back to Voltage measurement.](http://localhost:1313/labs/lab1folder/Lab1_Circuit4.png)
**Figure 7**: Circuit4. Measure the current into the 2.7k resistor, the 4.7k resistor and the branch containing the 10k and 1k resistor. After the measurement set your DVM back to Voltage measurement.

#### Questions:  
Q1: Using Ohm’s law ∆U = iR verify the measured values of the voltages across all resistors

![Equation 1](http://localhost:1313/labs/lab1folder/Equation1.PNG)

A1:    

Q2: Show the validity of Kirchhoﬀ’s voltage law which reads: In a closed loop, the algebraic sum of the voltages must be zero. To do this, in the closed loop 4.7k – 10k – 1k measure all voltages keeping the order of polarity the same (always measure high-low or red wire/black wire) and add them up.

A2:    

Q3: Show the validity of Kirchoﬀ’s current law which reads: In a node, the algebraic sum of the currents must be zero. Verify this using the current measurements from section 6).

A3:    

#### Links:  

[Ohm's Law](https://en.wikipedia.org/wiki/Ohm%27s_law)  
[Kirchoff's Laws](https://en.wikipedia.org/wiki/Kirchhoff%27s_circuit_laws)


Lab File:

Submission: [Submission link](https://compass2g.illinois.edu/webapps/login/)

**Link to resource**:  
[MATLAB Tutorial](http://localhost:1313/resources/matlab_guide/)  
[LaTex_Guide](http://localhost:1313/resources/latex_guide/)
