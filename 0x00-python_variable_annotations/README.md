# :book: 0x00. Python - Variable Annotations
## :page_with_curl: Topics Covered
1. Python Type Annotation.

# :computer: Tasks.
## [0. Basic annotations - add](0-main.py)
### :page_with_curl: Task requirements.
Write a type-annotated function add that takes a float a and a float b as arguments and returns their sum as a float.
```
bob@dylan:~$ cat 0-main.py
#!/usr/bin/env python3
add = __import__('0-add').add

print(add(1.11, 2.22) == 1.11 + 2.22)
print(add.__annotations__)

bob@dylan:~$ ./0-main.py
True
{'a':  <class 'float'>, 'b': <class 'float'>, 'return': <class 'float'>}
```

### :wrench: Task setup.
```bash
# Create task files and set execute permission.
touch 0-add.py
chmod +x 0-add.py
./0-add.py

# Lint checks
pycodestyle 0-add.py
mypy 0-add.py

# Tests
touch 0-main.py
chmod +x 0-main.py
./0-main.py
```

### :heavy_check_mark: Solution
> [:point_right: 0-main.py](0-main.py)


## [1. Basic annotations - concat](1-concat.py)
### :page_with_curl: Task requirements.
Write a type-annotated function add that takes a float a and a float b as arguments and returns their sum as a float.
```
bob@dylan:~$ cat 1-concat.py
#!/usr/bin/env python3
add = __import__('0-add').add

print(add(1.11, 2.22) == 1.11 + 2.22)
print(add.__annotations__)

bob@dylan:~$ ./1-concat.py
True
{'a':  <class 'float'>, 'b': <class 'float'>, 'return': <class 'float'>}
```

### :wrench: Task setup.
```bash
# Create task files and set execute permission.
touch 1-concat.py
chmod +x 1-concat.py
./1-concat.py

pycodestyle 1-concat.py
mypy 1-concat.py

# Tests
touch 1-main.py
chmod +x 1-main.py
./1-main.py
```

### :heavy_check_mark: Solution
> [:point_right: 1-concat.py](1-concat.py)


## [2. Basic annotations - floor](2-main.py)
### :page_with_curl: Task requirements.
Write a type-annotated function floor which takes a float n as argument and returns the floor of the float.
```
bob@dylan:~$ cat 2-main.py
#!/usr/bin/env python3

import math

floor = __import__('2-floor').floor

ans = floor(3.14)

print(ans == math.floor(3.14))
print(floor.__annotations__)
print("floor(3.14) returns {}, which is a {}".format(ans, type(ans)))

bob@dylan:~$ ./2-main.py
True
{'n': <class 'float'>, 'return': <class 'int'>}
floor(3.14) returns 3, which is a <class 'int'>
```

### :wrench: Task setup.
```bash
# Create task files and set execute permission.
touch 2-floor.py
chmod +x 2-floor.py
./2-floor.py

pycodestyle 2-floor.py
mypy 2-floor.py

# Tests
touch 2-main.py
chmod +x 2-main.py
./2-main.py
```

### :heavy_check_mark: Solution
> [:point_right: 2-main.py](2-main.py)


## [3. Basic annotations - to string](3-main.py)
### :page_with_curl: Task requirements.
Write a type-annotated function to_str that takes a float n as argument and returns the string representation of the float.
```
bob@dylan:~$ cat 3-main.py
#!/usr/bin/env python3
to_str = __import__('3-to_str').to_str

pi_str = to_str(3.14)
print(pi_str == str(3.14))
print(to_str.__annotations__)
print("to_str(3.14) returns {} which is a {}".format(pi_str, type(pi_str)))

bob@dylan:~$ ./3-main.py
True
{'n': <class 'float'>, 'return': <class 'str'>}
to_str(3.14) returns 3.14, which is a <class 'str'>
```

### :wrench: Task setup.
```bash
# Create task files and set execute permission.
touch 3-to_str.py
chmod +x 3-to_str.py
./3-to_str.py

pycodestyle 3-to_str.py
mypy 3-to_str.py

# Tests
touch 3-main.py
chmod +x 3-main.py
./3-main.py
```

### :heavy_check_mark: Solution
> [:point_right: 3-main.py](3-main.py)


## [4. Define variables](4-main.py)
### :page_with_curl: Task requirements.
Define and annotate the following variables with the specified values:

  * a, an integer with a value of 1
  * pi, a float with a value of 3.14
  * i_understand_annotations, a boolean with a value of True
  * school, a string with a value of “Holberton”
```
bob@dylan:~$ cat 4-main.py
#!/usr/bin/env python3

a = __import__('4-define_variables').a
pi = __import__('4-define_variables').pi
i_understand_annotations = __import__('4-define_variables').i_understand_annotations
school = __import__('4-define_variables').school

print("a is a {} with a value of {}".format(type(a), a))
print("pi is a {} with a value of {}".format(type(pi), pi))
print("i_understand_annotations is a {} with a value of {}".format(type(i_understand_annotations), i_understand_annotations))
print("school is a {} with a value of {}".format(type(school), school))

bob@dylan:~$ ./4-main.py
a is a <class 'int'> with a value of 1
pi is a <class 'float'> with a value of 3.14
i_understand_annotations is a <class 'bool'> with a value of True
school is a <class 'str'> with a value of Holberton
```

### :wrench: Task setup.
```bash
# Create task files and set execute permission.
touch 4-define_variables.py
chmod +x 4-define_variables.py
./4-define_variables.py

pycodestyle 4-define_variables.py
mypy 4-define_variables.py

# Tests
touch 4-main.py
chmod +x 4-main.py
./4-main.py
```

### :heavy_check_mark: Solution
> [:point_right: 4-main.py](4-main.py)

