# Python Summary
## 1. Setup


### 1.1. Download
Run `python3` to check if it's already on your machine

- **Mac**: Run this in terminal: `brew install python`.
- **Windows**: Download the installer from [python.org](https://www.python.org/downloads/windows/).
- **Linux**: Run this in terminal `sudo apt-get install python3`.


### 1.2. Run First Program
Create a file `hello.py` with the following content:
```python
print("Hello, World!")
```
Run it using the command: `python3 hello.py`.

## 2. Main Functionality

### 2.1. Variable Types & Initialization
You don't need to set data type for Python variables explicitly, you just set a value to it. 

```python
str_var = "Hello"           # String
int_var = 42                 # Integer
float_var = 2.3             # Float
bool_var = True             # Boolean

list_var = [1, 2, 3]                                            # List(similar to arrays)
tuple_var = ("Hello", 42, True, 5.9, 66)              #Tuples (unchangable list)
set_var = {"Cairo", "London", "Paris"}                  # Set (unique values)
dict_var = {"key1": "value2", "key2": "value2"}         # Dictionary

null_var = None	    # Null value
```

Casting variables
```python
int_var = int(2.8)      # 2
float_var = float("3.9")     #  3.9
```

### 2.2. Operators
- Arithmetic `x = 5 * 2 - ( 3 + 1 )  `
- Assignment `x += 1`
- Logical ` x = not(True and (False or True)) `
- Comparison `x >= 10`
### 2.3. Function Definition
```python
def greet(name):
    return "Hello, " + name
```

### 2.4. If & Conditions
```python
if x > 10:
    print("x is greater than 10")
elif x == 10:
    print("x is 10")
else:
    print("x is less than 10")
```
// TODO add more conditions match case so an inline conditions

### 2.5. Loops
```python
for i in range(5):  # For loop prints 0 to 4
    print(i)
```

// todo  add itrable example dict/array
// todo pass/continue
// todo catch exception

## 3. Architecture
### 3.1. Importing Packages
//todo datetime example
```python
import math
print(math.sqrt(16))  # 4.0
```

### 3.2. Classes & Dependencies
// to do add attributes and example how it's used in main


### 3.3. Re-using Functions
```python
from my_module import my_function
```
// todo add full code for this example like both classes
//todo system input & file input
## 4. Unit Tests 


// todo add unit test example 


