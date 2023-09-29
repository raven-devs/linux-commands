# Ccalculator

Basic calculator.

```bash
# basic arithmetic operations like addition, subtraction, multiplication, and division
bc
10 + 5
> 15

# assign values to variables and use them in calculations
x = 10
y = 5
x + y
> 15

# various mathematical functions, such as square root, sine, cosine, exponentiation, and more
sqrt(16)
> 4

# specify the number of decimal places to display in the result using the "scale" command, by default, it uses a scale of 0
scale = 2
1 / 3
> .33

# use "bc" within scripts to perform calculations and store the results in variables or files
# pass mathematical expressions directly as command-line arguments to "bc" without entering the interactive mode
$ echo "3 * 4" | bc
> 12

# quit
quit
```
