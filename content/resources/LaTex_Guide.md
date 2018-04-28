---
title: "LaTex_Guide"
date: 2018-04-19T10:43:25-05:00
draft: true
---

Always write the names of everyone in the lab group in the `\author{STUDENT NAME}` line of code located near the top of the LaTex code.  

When submitting labs on Compass2g, you must submit the (1) .tex file, (2) .pdf file, and (3) any images you added to the LaTex document. When saving an image, .png files work best.

When inserting an image into a LaTex document, you must save the image in the same, extracted folder as the rest of the lab files, to ensure a working pathway to the image. The image file name must not include any spaces (hence the underscores); if there are spaces, the LaTex file will not compile correctly.

The following lines of code are used to insert a figure/image:

```
\begin{figure} [h]
\centering
\includegraphics[width=1\linewidth]{NAME_OF_FILE}
\caption{ WRITE YOUR CAPTION HERE}
\label{fig:NAME_OF_FILE}
\end{figure}
```

The [h] is optional, and you may notice it is never present in any of the labs. It, however, forces the figure to appear where you are placing it in the LaTex document rather than the next available space. It's essentially a `here` command.

|Function | Description |
| ------- | ----------- |
| \\\\ | Acts as an `enter` button <br> ends the line/goes to a new line of text. |
|$x^2$|The dollar signs are used to convey equation formatting for the content between them when typing in general text (like within a paragraph, for example). <br> The example given here would compile as x2. You can write whole equations between the $ as well.|
|\begin{equation} <br> \end{equation}|Any line you write between these two will automatically take the format of an equation and be centered in the middle of the page. <br> Only one line of equation/math can be written here (a \\\\ won't create another line).|
|\begin{lstlisting} <br> \end{lstlisting}|Formats text into a box with numbered line in ABE 425 labs, this is how MatLab code is generally formatted into the LaTex document. <br> There's no need to use functions like \\\\ or any LaTex math functions for formatting in here. <br> It will show exactly what you type similar to how it shows up on MatLab.|
|\left[ <br> \right]|For formatting purposes, this will enlarge the parentheses of choice (in this case [ ]) to fit the equation(s) inside.|
|\dfrac{}{}|Corresponds to a fraction. Type the numerator between the first {} and the denominator in the second.|
|x^{10} <br> U_{out}|If the exponent contains more than one character, then it must be placed between {} in order for the whole thing to be read as the exponent. The same applies to subscript.|
|\pi <br> \omega <br> \tau <br> \theta <br> \omega|Common Greek letters used in mathematics are input into an equation like this. This function must be followed by a space in order to be read correctly. Note \omega is the symbol used to represent ohms.|
|\infty|The infinity symbol.|
|\sin <br> \cos <br> \tan|Use to write sin/cos/tan so that it does not appear italicized in an equation (as though each letter were an individual variable).|
|\sqrt{}|Square root symbol over whatever is placed inside the {}.|
|\dot{}|Places an overdot on whatever variable is typed between the {} which mathematically tends to indicate a derivative of that variable.|
|\bar{}|Places a pay over whatever variable is between the {}.|
|\hat{}|Places a hat over whatever variable is between the {}.|
|\int_{}^{}|This provides the integral sign with defined a lower bound (in the first {}) and a defined upper bound (in the second {}). <br> Ex: \int_{t=0}^{t=2\pi} f(x) dx|
|�]_{}*{}|After taking an integral, you may still want to write the equation before having input the upper and lower bounds into the corresponding variable. In such a case, you can indicate what they are using the _{}^{}, which is identical to how they are shown on the integral symbol (see above).|
|\sum_{}^{}|The summation symbol with lower and upper bounds.|
|\begin{pmatrix} <br> �& & \\\\ <br> �& & \\\\ <br> �& & \\\\ <br> �& & <br> \end{pmatrix}|Example matrix function. The &s separate the columns, and the \\ creates a new row. This example would be a 4 by 3 matrix (4 rows, 3 columns).|
|\begin{tabular}{\|c\|c\|c\|c\|c\|} <br> \hline & & & & \\\\ <br> \hline & & & & \\\\ <br> \hline & & & & \\\\ <br> \hline & & & & \\\\ <br> \hline & & & & \\\\ <br> \hline <br> \end{tabular} | Example of a table. The number of columns is defined in the first line by the number of �c�s, which in this example represents 5 columns. The &s separate values along a row. The \\ marks the ends a row/starts a new one. The \hline is a horizontal line, which is essentially visually separating the rows; the lone \hline on the end draws the bottom border of the table.|
