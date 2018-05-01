---
title: "MatLab_Guide"
date: 2018-04-19T10:43:25-05:00
draft: true
---
The following lines of code are general purpose commands:

```
>>clc         Clear Command Window
>>clear       Remove items from the workspace
>>clear all   Basically same as clear
>>close       Closes current figure window
>>close(H)    Closes figure with handle H
>>delete      Delete files or graphics objects
>>exit        Terminate MATLAB
>>quit        Terminate MATLAB
>>startup     MATLAB startup M-file
```
The following lines of code are used to creating vector and matrix :
```
>> x = [1,2,3]   To enter vectors use square brackets
>> x = [1 2 3]   To create a row vector separate elements with commas or spaces
>> y = [4;5;6]   To create a column vector separate elements with semicolons
>> x = x'        The transpose of a vector (or matrix) i
>> w = 1:0.5:5   To create a row vector by indicating a starting value,an increment, and an ending value, all separated by a colon
>>rand(12,4)     A12*4 matrix with uniform random numbers in [0,1]
>>zeros(12,4)    A12*4 matrix of zeros
>>ones(12,4)     A12*4 matrix of ones
```
The following lines of code are used to extracting different elements of a matrix
```
>> A(1,1)   Extracts the element in the (1,1) position
>> A(2,:)   Extracts the second row of the matrix
>> A(:,2)   Extracts the second column of the matrix
```
The following lines of code are Matrix operations
```
>>x.*y    Element by element multiplication
>>x./y    Element by element division
>>x+y     Element by element addition
>>x-y     Element by element subtraction
>>A^n     Normal/Matrix power of A
>>A.^n    Elementwise power of A
```
The following lines of code are plotting commands
```
>>fig1 = plot(x,y)                      2d line plot, handle set to fig1
>>set(fig1, ’LineWidth’, 2)             change line width
>>set(fig1, ’LineStyle’, ’-’)           dot markers (see *)
>>set(fig1, ’Marker’, ’.’)              marker type (see *)
>>set(fig1, ’color’, ’red’)             line color (see *)
>> plot(x,y1,’--’,x,y2,’-’,x,y3,’:’)    Used for multiple figures in single plot
>>xlabel (’\mu line’,’FontSize’,14)     names x/y/z axis
>>title(’name’,’fontsize’,22)           names plot
>>legend(’x’,’y’,’Namex’,’Namey’)       adds legends
>>hold on                               retains current figure when adding new stuff
>>hold off                              restores to default (no hold on)
```

[See more information here](https://www.mathworks.com/help/matlab/)
