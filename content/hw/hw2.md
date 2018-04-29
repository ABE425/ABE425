---
title: "HW2"
date: 2018-04-17T13:04:56-05:00
draft: true
---

Released: 2018-01-30

Due: 2018-02-07


**Description**  
TThis homework must be completed in LaTex, you can do the work on paper, but you have to submit it as an extension of the document you are reading now.
One of the most confusing formulas that you were ever given in college was Euler's formula, and I am willing to bet that nobody ever showed you how to derive it. The reason why it is confusing is that it equates an exponential function, to the sum of cosine and sine functions. Most people think of an exponential function as one that is unbounded, and that tends to infinity very quickly. On the other hand, one thinks of cosine and sine as bounded functions, which makes equating them counter-intuitive. Throwing in the complex operator j (since we avoid the symbol i, which we use for current) does not make it easier.

This is why you need to derive Euler's formula, afterward you may still think it is confusing, but at least you'll remember that at some point in your life you derived it yourself. The method we will use is to express all three terms of Euler's formula in a MacLaurin series, and we'll discover that the MacLaurin series of the LHS and the RHS of the formula are the same, proving its validity.

**Euler's formula is given as:**

e^(jt) = cos(t) + j sin(t)


**The Taylor series approximation is given as:**

![figure]()

**The MacLaurin series approximation is a Taylor series approximation** where
xbar = 0
![figure2]()

\( f(x) =f(0) + \dfrac{f'(0)}{1!}x + \dfrac{f''(0)}{2!}x^2 + \dfrac{f'''(0)}{3!}x^3 + h.o.t.  =\sum_{n=0}^{\infty}\dfrac{f(0)^{(n)}x^n}{n!}\)

Exercise 1: Express e^t in a MacLaurin series.

Exercise 2: Show in the MacLaurin series of $e^t$ that the derivative of  e^t =  e^t, in other words $e^t$ is its own derivative.


Exercise 3: Express e^1 in a MacLaurin series. This is the number $e$.


Exercise 4: Express e^(jt)  in a MacLaurin series.


Exercise 5: Express sin(t) in a MacLaurin series, write it out here.


Exercise 6: Express cos(t) in a MacLaurin series, write it out here.


Exercise 7: Add the approximations of cosine and sine and multiply every term in the sine approximation by $j$ to get the MacLaurin approximation of cos(t) + j sin(t). Compare this series with the MacLaurin approximation of e^(jt).




**Link**: [Visit the HM2](https://github.com/ABE425/ABE425/tree/master/data/hw/HW_TheveninEquivalents )

Submission:[SUBMIT YOUR HOMEWORK HERE]()

Link to resource:[MATLAB Tutorial](../../resources/MATLAB_Guide.md)  
                [LaTex_Guide](../../resources/LaTex_Guide.md)
