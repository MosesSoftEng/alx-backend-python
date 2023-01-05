# :book: 0x00. Python - Variable Annotations
## :page_with_curl: Topics Covered
1. Python Type Annotation.

# :computer: Tasks.
## [0. Basic annotations - add](task_1)
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

pycodestyle 0-add.py
mypy 0-add.py

# Tests
touch 0-main.py
chmod +x 0-main.py
./0-main.py
```

### :heavy_check_mark: Solution
> [:point_right: task_1](task_1)
