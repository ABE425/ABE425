---
title: "ICE 8"
date: 2018-04-17T13:05:12-05:00
draft: true
---

Released:2018-04-05

Due:In class

Description:
This is In-Class Exercise 8. Read the instruction and answer the questions below.This assignment is to be submitted it in class.

Link: [ICE 8](https://github.com/ABE425/data/blob/lia/ICE/ICE_CircuitAnalysis.pdf)

Submission: [Submission link](?)

## In-Class Exercise: Schmitt-Trigger.

STUDENT NAME:

DATE: February 23, 2018

Figure 1 shows the schematic of the Schmitt-Trigger circuit. It is essentially an OpAmp used as a
comparator (hence the output can only be plus or minus Vsat), but the output is fed back to the non-inverting input terminal.
To analyze how the circuit works, first we need the general OpAmp equation which reads:

VO = AOL(V+ − V−)                                            (1)
Where AOL is the open loop amplification factor of the OpAmp which is about 106. We also need to assign values to the saturation voltage. Let’s assume that the Vcc = ±12V and therefore Vsat = ±10V.

Fill in the table below.

1. Calculate V+(k) from VO(k) using the voltage divider rule.
2. Calculate VO(k + 1) using the OpAmp equation.
3. Calculate V+(k + 1) from VO(k + 1) using the voltage divider rule.
4. Copy the (k+1) values into the (k) values of the next row, and repeat steps
2-4.


|    | V-(k)  | V+(k) | Vo(k) | Vo(k+1) |
|----|--------|-------|-------|---------|
|a| 0 | | | +10 | |
|b|+6| | | | |
|c|+6| | | | |
|d|-6| | | | |
|e|-6| | | | |


Draw the input signal V−(k) in Figure 2. Then draw the response (output signal VO)) in the figure as well. Cross-hatch the dead band in the figure.
