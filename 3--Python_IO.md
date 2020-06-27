# Input/Output with Python

In this file, **three methods** will be introduced for input with python
  ## 1. **argparse**

The following program shows an easy example of input to numbers and output their sum.
```python
################## Programming body ###################################
import argparse   # First thing to do is to import the package

parser = argparse.ArgumentParser(description='Do Math')
parser.add_argument('-n1', '--num1', type=float,  default=2, metavar='', help='input the first number')
parser.add_argument('-n2', '--num2', type=float,  default=3, metavar='', help='input the second number')
args = parser.parse_args()

def add(a, b):
    return a+b

if __name__ == '__main__':
    print(add(args.num1, args.num2))   # Must be num1 and num2 instead of n1 and n2
```
```python
################### Run in python terminal ############################
# I'll take windows as an example
>conda activate python3.7
# ----------- Run help ---------------------
>python D:\WORK\test.py -h
  usage: test.py [-h] [-num1] [-num2]

  Do Math

  optional arguments:
  -h, --help       show this help message and exit
  -num1 , --num1   input the first number
  -num2 , --num2   input the second number
# ----------- Run default -------------------
>python D:\WORK\test.py
  5
# ----------- Run user input ----------------
>python D:\WORK\test.py -n1 5 -n2 7
  12
```
  - `parser = argparse.ArgumentParser(description='Do Math')`
    - **parser** is a container to hold arguments
    - For description, it's a descriptive string to state the functionality of script.
  - `parser.add_argument('-n1', '--num1', type=float,  default=2, metavar='', help='input the first number')`

    - `-n1`, `-n2`: short names of variables
    - `-num1`, `-num2`: long names of variables. They are the real **attributes** instead of the short names
    - `type=float`: Data type can be: float, int, str and so on...
    - `default=2`: Set the default number
    - `metavar=``: Make the help file neat
    - `'help='input the first number'`: help string
