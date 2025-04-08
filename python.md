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
- If else
```python
if x > 10:
    print("x is greater than 10")
elif x == 10:
    print("x is 10")
else:
    print("x is less than 10")


# Short hand if
print("x is 10") if x == 10 else print("x is not 10")

```
- match case
```python
char = 'e'
match char:
  case 'a':
    print("This character is a")
  case 'b':
    print("This character is b")
  case 'c' | 'd':
  	print("This character is c or d")
  case _:
    print("This character is not a , b , c nor d")
```
### 2.5. Loops
- loop on range
```python
for i in range(5):  # For loop prints 0 to 4
    print(i)
```

- loop on array
```python
cities = ["Cairo", "London", "Paris"]
for x in cities:
  print(x)
```

- loop on dictionary
```python
dict =	{
  "key1": "value1",
  "key2": "value2"
}

for k, v in dict.items():
  print(k, "is", v)

```
- using continue

```python
for x in range(0, 6):
  if x == 2:
    continue
  print(x) 
# prints 0 1 3 4 5
```


### Catch Exception

```python
try:
  doSomething()
except:
  print("Error occurred")
finally:
  print("Done")
```

## 3. Architecture
### 3.1. Importing Packages
```python
from datetime import datetime, timedelta

current_datetime = datetime.now()

date_str = "2025-02-23 16:30:00"
parsed_datetime = datetime.strptime(date_str, "%Y-%m-%d %H:%M:%S")

old_date = parsed_datetime - timedelta(days=7)  
```

### 3.2. Classes & Dependencies

```python
# file course.py
class Course:
    def __init__(self, name):
        self.name = name

    def __str__(self):
        return self.name
```

```python
# file student.py
from course import Course  

class Student:
    def __init__(self, name):
        self.name = name
        self.courses = [] 

    def enroll(self, course):
        self.courses.append(course)
        print("Student:",  self.name, "enrolled in:", course)

    def list_courses(self):
            print("Student",  self.name,  "courses:", ' - '.join(course.name for course in self.courses))

# Example usage
if __name__ == "__main__":
    math = Course("Math")
    physics = Course("Physics")

    adam = Student("Adam")
    adam.enroll(math)      # Student: Adam enrolled in: Math
    adam.enroll(physics)   # Student: Adam enrolled in: Physics
    adam.list_courses()    # Student Adam courses: Math - Physics
```

## 4. Input & output
### 4.1. System Input

```python
input_val = input("Choose number between 1 and 20:")
```
### 4.2. File Input
sample.txt
```
This is just
To test 
How read file in python works
```

```python
my_file = open("sample.txt")
print("just 4 characters =>", my_file.read(4))
print("just one line => ", my_file.readline())
print("the whole file => ", my_file.read())
my_file.close()
```

Output
```
just 4 characters => This
just one line =>   is just

the whole file =>  To test 
How read file in python works
```

### 4.3. System output

```python
print("Hello")              # Hello
print("Hello", "world") # Hello world
```

### 4.4. File output
```python
my_file = open("sample.txt", "a")
my_file.write("This text will be added to the end of the file")
my_file.close()
```

```python
my_file = open("sample.txt", "w")
my_file.write("This text will overwrite the contents of the file")
my_file.close()
```
## 5. Unit Tests 


// todo add unit test example 


