# Input/Output with Python

In this file, **three methods** will be introduced for input with python
  - **argparse**
  - **sys.argv**
  - **yaml File**

  ## 1. **argparse**

The following program shows an easy example of input to numbers and output their sum. __The code hase bo be executed in terminal__
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

### Example:
```python
import argparse

def main(data):
    print(vars(data))
    print(vars(data)['t1'])
    for i, j in vars(data).items():
        print(i, j)

if __name__ == '__main__':
    parser = argparse.ArgumentParser()
    parser.add_argument('-num_band', type=int, default=5, metavar='', help='Total number of bands to calculate')
    sufficient; More accurate IFC plot depends on total number of N_kx, N_ky')
    parser.add_argument('-n', type=float, default=1.525, metavar='', help='Refractive index')
    #  Unit cell dimension
    parser.add_argument('-beta', type=float, default=2.3, metavar='', help='The ratio of b/a')
    parser.add_argument('-t1', type=float, default=0.27, metavar='', help='t1/a ; t1 = 0.2a')
    parser.add_argument('-t2', type=float, default=0.6, metavar='', help='t2/b ; t2 = 0.6b')
    args = parser.parse_args()

    main(args)
```
```python
# -------------- Run in Linux terminal -------------------

# ---- Run help ----
$ python 1.2.0--Band_Data_Calculation.py -h

    usage: 1.2.0--Band_Data_Calculation.py [-h] [-num_band] [-n] [-beta] [-t1]
                                           [-t2]

    optional arguments:
      -h, --help  show this help message and exit
      -num_band   Total number of bands to calculate
      -n          Refractive index
      -beta       The ratio of b/a
      -t1         t1/a ; t1 = 0.2a
      -t2         t2/b ; t2 = 0.6b
```
It outputs **usages** with all the **optional arguments**, and gets them listed out with the help texts.
```python
# ---- Run the file itself ----
$ python 1.2.0--Band_Data_Calculation.py

  {'num_band': 5, 'n': 1.525, 'beta': 2.3, 't1': 0.27, 't2': 0.6}
  0.27
  num_band 5
  n 1.525
  beta 2.3
  t1 0.27
  t2 0.6

```
   - `args` is **class** data type with many attributes
   - `vars(args)` converts it to **dictionary** data type
   - The code below prints out all the components
   ```python
   for i, j in vars(data).items():
       print(i, j)
# --- output ---
       num_band 5
       n 1.525
       beta 2.3
       t1 0.27
       t2 0.6
  ```

## 2. **sys.argv**

It simply takes whatever is in the input, here is how it works
 - Only show all the inputs

 ```python
 #------------ Program body -------------
 import sys
 print(sys.argv)
 ```
 ```python
 #------------ Run in windows terminal -------------
 >D:/WORK/test.py 1 2 3 4 5
    ['D:/WORK/test.py', '1', '2', '3', '4', '5']
 ```

 - Only take the **input numbers**, convert to **float** type, and put them in a **list**
 ```python
 #------------ Program body -------------
 import sys
 input = map(float,sys.argv[1:])
 print(list(input))
 ```
 ```python
 #------------ Run in windows terminal -------------
 >D:/WORK/test.py 1 2 3 4 5
    [1.0, 2.0, 3.0, 4.0, 5.0]
 ```
