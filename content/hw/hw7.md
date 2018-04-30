---
title: "HW7"
date: 2018-04-17T13:04:56-05:00
draft: true
---

Released: 2019-03-05

Due: 2019-03-12

**NAME:**
**HW: Mandelbrot Fractal Programming in MatLab**

#Description

The purpose of this homework is to give the student a thorough exercise in MatLab programming, and en passe appreciate the concept of mathematical complexity.

#Introduction
Before fractal geometry was discovered by[Benoit Mandelbrot][https://en.wikipedia.org/wiki/Benoit_Mandelbrot], we only had Euclidian geometry which cannot describe "natural" objects such as mountains, clouds, trees, plants, lungs, artery systems etc. Since agricultural engineering is about connecting living objects to technology, it is only natural (pun intended) to discuss fractals.

[Benoit Mandelbrot][https://en.wikipedia.org/wiki/Benoit_Mandelbrot] is credited with being the first person to visualize mathematical complexity in a spectacular way. The idea is to take a non-linear equation, and iterate it, meaning that you give it a starting value and then calculate a new value by entering this starting value into the equation. Then you take the result of the equation, put it back in and calculate a new value. You keep doing this and check if the value eventually goes to infinity (or out of a preset bound) or if it stays within the bound. You also keep track of how many iterations it took for the value to go out of the bound, you use that to assign a color.

To calculate the Mandelbrot fractal, we need to use the complex plane that runs from ```[-2.5, 1.5]``` on the real axis and ```[-1.5,1.5]``` in the imaginary axis.

![HW_MandelbrotFractalCoordinates](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/hw_fractal/HW_MandelbrotFractalCoordinates.PNG)

The equation we are going to use is a logistics equation:
```
z(n+1) = z(n)^2 + c
```
where z and c are complex numbers, and n indicates the iteration (look at ```z(n)``` as the previous value of ```z(n+1)```). For the programming it is easiest to split our complex number into a real and imaginary part (although you don't have to, MatLab can deal with complex numbers quite well). However, we would have to use "r" for real and "j" for imaginary, in our case it is much easier to look at the x-axis as the real axis and the y-axis as the imaginary axis. This makes the notation much more in line with a program that would use an x and y axis. Therefore we'll define ```z_r = z_x``` and ```z_j = z_y```. Our complex number z now becomes:

![figute2](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/HW_other/Fractal2.png)

If we substitute this form into the logistics equation we get:

![figute3](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/HW_other/Fractal3.png)

Evaluating the square gives:

![figute4](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/HW_other/fractal4.png)

Splitting the real and imaginary parts gives:

![figute5](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/HW_other/fractal5.png)

and:

![figute6](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/HW_other/fractal6.png)

The constant ```c``` is quite important. If you set this factor to a constant number in the range as shown in Figure, then you get what is known as a Julia Fractal. However, if you set the constant ```c``` equal to the coordinate of the pixel under calculation, then you get the Mandelbrot fractal, which is our aim here.

#Program structure
The variables as shown in Equations(5)and (6) look good in a report, but MatLab cannot read them as such (for instance MatLab does not regard z_n+1 a variable). Therefore we need some representatives. Let's assign _z_x_new_ to ```z_x(n+1)``` and _z_x_old_ to ```z_x(n)``` and _z_y_new_ to ```z_y(n+1)``` and _z_y_old_ to z_y(n). We will write _x_coor_ for c_x and _y_coor_ for ```c_y```.

The program has three major sections that are executed in sequence being 1) Initialization, 2) Calculation and 3) Output (a graph). In the intialization section, you set constants and give them logical names.
Give a value to MaxIterations to say 100. This variable sets a limit to the maximum number of iterations that we will do before we quit. The boundaries of our fractal are _x_min_ = -2.5 and _x_max_ = 1.5, _y_min_ = -1.5, _y_max_ = 1.5. The program needs to begin by entering the boundary coordinates and a step size to calculate the coordinates of our pixels. If we want a 400 * 300 image, then we the x-stepsize would be 4/400 = 0.01 and the y-stepsize would be 3/300 = 0.01.

Now we need to create an "empty" image that we can use to write values to (you'll see later what values). The easiest trick is to fill that "empty" image with MaxIterations, it just looks good.

Now we have to run through all rows, and all columns to address each pixel. We start with the coordinate of the pixel and then iterate the real and imaginary parts of the pixel using  Equations(5)and (6). You iterate these calculations, until the absolute value ```A = |z(n+1)| = sqrt(z_r(n+1)^2 + z_j(n+1)^2)```  becomes larger than 2 **OR** we exceed a preset number of iterations. If the absolute value of the trajectory goes out of the bound (2) then we write the number of iterations as the pixel value in our current coordinate. This method shows the "depth" of the Mandelbrot fractal structure. We also need to set a limit to the number of iterations to avoid getting into an infinite loop. If a trajectory has not gone out of the bound (2) within say 100 iterations, we conclude that it is bounded and do nothing, at that point the pixel keeps the value it was assigned before the calculations.

Now we need to go through the whole image starting at the bottom left (_x_min_, _y_min_) and work our way through every pixel row by row. For this we need two nested loops.

Inside the hot loop, we need to calculate the absolute value ```|z(n+1)|``` and keep track of for how many iterations it stays withing the limit of 2. Some pixels will stay bounded forever so we need to set a limit to the maximum number of iterations to prevent getting stuck in an infinite loop. Finally we plot the Fractal image using imagesc (which scales it properly).

The complete process is shown in a Nassi-Shneiderman diagram in Figure below

![fig:MandelbrotNSDiagram](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/hw_fractal/MandelbrotNSDiagram.png).  
[MandelbrotNSDiagram][https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/hw_fractal/MandelbrotNSDiagram.png]

shows the Mandelbrot fractal.

The first thing that should strike you (I hope) is that there is an overwhelming amount of detail, self-similarity and unique areas in the Mandelbrot fractal. The most baffling thing is that all this emerges from iterating a very simple equation! The intuitive idea that a complex object needs a complex underlying mechanism is obviously false! For instance when you see the pattern of the coat of a cat

![fig:MaineCoon_SolidBlackCat](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/hw_fractal/MaineCoon_SolidBlackCat.PNG)

Compare a Maine Coon cat (left) with elaborate striping to a solid black cat. One would expect that the striping of the Maine Coon (notice the M on this cat's forehead) would require a large number of genes. That is not the case, even a small number of genes can give rise to enormous differences in phenotype. Complexity can arise from very simple rules.

you would imagine that many genes may be involved to produce this kind of complexity. It turns out that is not the case, only a handful of genes make up the difference between a solid colored cat and a Maine coon (note the M on this cat's forehead).

Q1: Give the name of the fractal shown in Figure below
![fig:HW_Q1Fractal](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/hw_fractal/HW_Q1Fractal.png)

_(The answer can be found in the Nova documentary "Hunting the hidden dimension")._

**Link**: [Visit the HM7](https://github.com/ABE425/ABE425/tree/master/data/hw/HW_TheveninEquivalents )

Submission:[SUBMIT YOUR HOMEWORK HERE]()

Link to resource: [LaTex_Guide](../../resources/LaTex_Guide.md)
