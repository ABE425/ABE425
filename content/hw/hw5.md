---
title: "HW5"
date: 2018-04-17T13:04:56-05:00
draft: true
---

Released: 2019-02-21

Due: 2019-02-28

**NAME:**  
**HW: Fourier series of a triangular signal**

**Description**

If a signal is given on an interval ```[0, 2pi]```, the Fourier series can be written as:

![figure1](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/HW_other/Fourier1.png)

with coefficients:

![figure2-4](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/HW_other/Fourier2-4.png)

**Worked example 1**

![fig:1](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/hw_fourierseries/HW_FourierSeries1.png)  
The figure shows a square wave given on the interval ```[0, 2 pi]```. To calculate the Fourier coefficients, we need to evaluate the integrals above, but you need to be smart about it. Firstly, the coefficient ```c_0``` represents the mean of the signal, and just by looking at the signal you can tell ```c_0``` will be zero. Secondly, as you know, if a signal is even, then only coefficients of cosine will have a value, because the cosine itself is an even function. Vice versa for an odd function where only the sine coefficients will have a value. By the way, some signals are both odd and even, then both sine and cosine coefficients will have a value. Since our function is obviously odd (it is symmetric in the origin) only the sine coefficients will have a value therefore ```a_n = 0```. The values of the sine coefficients can be calculated by evaluating the integral:

For the part of the signal that runs from 0 to pi we get:

![figure5](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/HW_other/fourier5.png)

The values of the ```b_n``` coefficients for the interval ```0```, pi are now 0 for n = even, and 2/n*pi for n = odd.

For the part of the signal that runs from pi to 2*pi we get:

![figure6](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/HW_other/fourier6.png)

The values of the ```b_n``` coefficients for the interval pi, 2*pi are now 0 for n = even, and 2/n*pi for n = odd.

The sum of ```b_n``` coefficients for the interval 0, 2*pi are now 0 for n = even and 4/pi for n = odd. The spectrum where the coefficient values are plotted against the frequency (coefficient number n) is shown in Figure

![fig:HW_FourierSeries2](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/hw_fourierseries/HW_FourierSeries2.png).

The first two coefficients are 4/pi = 1.2732 (n=1), 4/3*pi = 0.4244 n=3, verify this in Figure above.

![fig:HW_FourierSeries3](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/hw_fourierseries/HW_FourierSeries3.png).

The Fourier series approximation of the square wave function using 50 sine coefficients is shown in Figure above. As the approximation of the Fourier series to the square wave becomes better, the peaks at the 'shoulders' will become more and more pronounced. This effect is called the Gibbs phenomenon, and in image processing we call this effect "ringing".

**Worked example 2**

![fig:HW_FourierSeries4](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/hw_fourierseries/HW_FourierSeries4.png).
shows a saw tooth signal on the interval [0, 2 pi].

![figure7](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/HW_other/fourier7.png).

It is clear from the signal that the mean value is zero, therefore ```c_0``` is zero. This signal is obviously odd since $f(-t) = -f(t)$, therefore all ```a_n``` are zero. Now we need to calculate the $b_n$ coefficients.

![figure8](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/HW_other/fourier8.png).

which can be written as (watch the limits change):

![figure9](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/HW_other/fourier9.png).

Let's do the first term first:

![figure10-13](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/HW_other/fourier10-13.png).

Substitution gives:

![figure14](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/HW_other/fourier14.png).

Inserting the limits gives:

![figure15](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/HW_other/fourier15.png).

We still have the second term as follows:

![figure16-17](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/HW_other/fourier16-17.png).

The first four coefficients are 2 (n=1), -1 (n=2), 2/3 (n=3), - 1/2 (n=4), verify this in

![fig:HW_FourierSeries5](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/hw_fourierseries/HW_FourierSeries5.png)

The Fourier series approximation of the sawtooth function using 50 basis functions is shown in Figure below.

![fig:HW_FourierSeries6](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/hw_fourierseries/HW_FourierSeries6.png)

**Your homework starts here:**

![fig:HW_FourierSeries7](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/hw_fourierseries/HW_FourierSeries7.png)

A triangular input signal as shown in Figure is given on the interval [0, 2 pi]. The functional form of this shape is:

![figure16-17](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/HW_other/fourier16-17.png).

Calculate the Fourier coefficients of this function.
**Use LaTex functionality, so just continue this document, and extend it to include your answer. Submit the pdf file of this document and don't forget to put your name at the top.** You do **NOT** need to show the Fourier coefficients in a graph, we'll do that in the lab.

**Link**: [Visit the HM5](https://github.com/ABE425/ABE425/tree/master/data/hw/HW_TheveninEquivalents )

**Submission**:[SUBMIT YOUR HOMEWORK HERE]()

**Link to resource**: [LaTex_Guide](../../resources/LaTex_Guide.md)
