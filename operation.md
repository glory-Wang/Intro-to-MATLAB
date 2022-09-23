# operations

inv()------->inverse  

.*------->To perform element-wise multiplication rather than matrix multiplication

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

strlength() ------->
