# operations

inv()------->inverse  

.*------->To perform element-wise multiplication rather than matrix multiplication

a' -------> 转置

## concatenaion

Concatenation is the process of joining arrays to make larger ones. In fact, you made your first array by concatenating its individual elements.

A = [a,a]  ------->  horizontal concatenation

A = [a;a]  ------->  vertically concatenation

## Complex Numbers

Complex numbers have both real and imaginary parts, where the imaginary unit is the square root of -1.

sqrt(-1)

## array indexing

Every variable in MATLAB® is an array that can hold many numbers. When you want to access selected elements of an array, use indexing.

For example, consider the 4-by-4 matrix A:

A = [1 2 3 4; 5 6 7 8; 9 10 11 12; 13 14 15 16]

two ways to refer to an element:

A(4,2) -------> ans = 14

A(8) -------> ans = 14

ALERT!: If you try to refer to elements outside an array on the right side of an assignment statement, MATLAB throws an error.

a way to refer to some elements:

A(1:3,4) or A(1,:)

The colon operator allows you to create an equally spaced vector of values using the more general **_form start:step:end_**.

B = 0:10:100

## Workspace Variables

whos -------> You can view the contents of the workspace, you can also add any variables behind 'whos' to figure out the variable.

save myfile.mat -------> Workspace variables do not persist after you exit MATLAB. Save your data for later use with the save command

load myfile.mat -------> Restore data from a MAT-file into the workspace using load.

## Text and Characters

### Text in String Arrays

t = "Hello, world"; ------> When you are working with text, enclose sequences of characters in double quotes. You can assign text to a variable.

q = "Something ""quoted"" and something else." -------> If the text includes double quotes, use two double quotes within the definition.

P.S: t and q are arrays, like all MATLAB® variables. Their class or data type is string.

f = 71;  
c = (f-32)/1.8;  
tempText = "Temperature is " + c + "C"  
------->tempText = "Temperature is 21.6667C" -------> To add text to the end of a string, use the plus operator, +.

strlength() ------->  Using the strlength function can find the length of each string within an array(space will occupy a length)

# Data in Character Arrays

Sometimes characters represent data that does not correspond to text, such as a DNA sequence. You can store this type of data in a character array, which has data type char. Character arrays use single quotes.

Each element of the array contains a single character.((seq = 'GCTAGAATCC'; -------> seq(4) -------> ans = 'A')

seq2 = [seq 'ATTAGAAACC'] -------> Concatenate character arrays with square brackets, just as you concatenate numeric arrays.  

P.S.:Character arrays are common in programs that were written before the introduction of double quotes for string creation in R2017a. All MATLAB functions that accept string data also accept char data, and vice versa.

## Calling Functions

max() ------>  enclose its input arguments in parentheses

union(A,B) ------> If there are multiple input arguments, separate them with commas

maxA = max(A) -------> Return output from a function by assigning it to a variable

[minA,maxA] = bounds(A) -------> When there are multiple output arguments, enclose them in square brackets

## 2-D and 3-D Plots

# line plots

To create two-dimensional line plots, use the plot function. For example, plot the sine function over a linearly spaced vector of values from 0 to 2π:  
x = linspace(0,2*pi);  
y = sin(x);  
plot(x,y)  

You can label the axes and add a title.  
xlabel("x")  
ylabel("sin(x)")  
title("Plot of the Sine Function")  

plot(x,y,"r--") -------> By adding a third input argument to the plot function, you can plot the same variables using a red dashed line. -------> "r--" is a line specification. Each specification can include characters for the line color, style, and marker. A marker is a symbol that appears at each plotted data point, such as a +, o, or *. For example, "g:*" requests a dotted green line with * markers.

Notice that the titles and labels that you defined for the first plot are no longer in the current figure window. By default, MATLAB® clears the figure each time you call a plotting function, resetting the axes and other elements to prepare the new plot.

To add plots to an existing figure, use **hold on**. Until you use **hold off** or close the window, all plots appear in the current figure window.

legend("sin","cos") ------->  the **legend** shows the different lines in a chart 

# 3-D Plots

Three-dimensional plots typically display a surface defined by a function in two variables, z=f(x,y).

Both the surf function and its companion mesh display surfaces in three dimensions. surf displays both the connecting lines and the faces of the surface in color. mesh produces wireframe surfaces that color only the connecting lines.

# Multiple Plots  
You can display multiple plots in different parts of the same window using either tiledlayout or subplot.

The tiledlayout function was introduced in R2019b and provides more control over labels and spacing than subplot. For example:  

t = tiledlayout(2,2);  
title(t,"Trigonometric Functions")  
x = linspace(0,30);  

nexttile  
plot(x,sin(x))  
title("Sine")  

nexttile  
plot(x,cos(x))  
title("Cosine")  

nexttile  
plot(x,tan(x))  
title("Tangent")  

nexttile  
plot(x,sec(x))  
title("Secant")  

## Programming and Scripts  
The simplest type of MATLAB® program is called a script. A script is a file that contains multiple sequential lines of MATLAB commands and function calls. You can run a script by typing its name at the command line.

# scripts  
edit mysphere ------->  using the edit command to create a script


