# :book: 0x00. 0x01. Python - Async
## :page_with_curl: Topics Covered
1. Python Async.

# :computer: Tasks.
## [0. The basics of async](0-basic_async_syntax.py)
### :page_with_curl: Task requirements.
Write an asynchronous coroutine that takes in an integer argument (max_delay, with a default value of 10) named wait_random that waits for a random delay between 0 and max_delay (included and float value) seconds and eventually returns it.

Use the random module.
```
bob@dylan:~$ cat 0-main.py
#!/usr/bin/env python3

import asyncio

wait_random = __import__('0-basic_async_syntax').wait_random

print(asyncio.run(wait_random()))
print(asyncio.run(wait_random(5)))
print(asyncio.run(wait_random(15)))

bob@dylan:~$ ./0-main.py
9.034261504534394
1.6216525464615306
10.634589756751769
```

### :wrench: Task setup.
```bash
# Create task files and set execute permission.
touch 0-basic_async_syntax.py
chmod +x 0-basic_async_syntax.py
./0-basic_async_syntax.py

# Lint checks
pycodestyle 0-basic_async_syntax.py
mypy 0-basic_async_syntax.py

# Tests
touch 0-main.py
chmod +x 0-main.py
./0-main.py
```

### :heavy_check_mark: Solution
> [:point_right: 0-basic_async_syntax.py](0-basic_async_syntax.py)


## [1. Let's execute multiple coroutines at the same time with async](1-concurrent_coroutines.py)
### :page_with_curl: Task requirements.
Import wait_random from the previous python file that you’ve written and write an async routine called wait_n that takes in 2 int arguments (in this order): n and max_delay. You will spawn wait_random n times with the specified max_delay.

wait_n should return the list of all the delays (float values). The list of the delays should be in ascending order without using sort() because of concurrency.
```
bob@dylan:~$ cat 1-main.py
#!/usr/bin/env python3
'''
Test file for printing the correct output of the wait_n coroutine
'''
import asyncio

wait_n = __import__('1-concurrent_coroutines').wait_n

print(asyncio.run(wait_n(5, 5)))
print(asyncio.run(wait_n(10, 7)))
print(asyncio.run(wait_n(10, 0)))

bob@dylan:~$ ./1-main.py
[0.9693881173832269, 1.0264573845731002, 1.7992690129519855, 3.641373003434587, 4.500011569340617]
[0.07256214141415429, 1.518551245602588, 3.355762808432721, 3.7032593997182923, 3.7796178143655546, 4.744537840582318, 5.50781365463315, 5.758942587637626, 6.109707751654879, 6.831351588271327]
[0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0]

The output for your answers might look a little different and that’s okay.
```

### :wrench: Task setup.
```bash
# Create task files and set execute permission.
touch 1-concurrent_coroutines.py
chmod +x 1-concurrent_coroutines.py
./1-concurrent_coroutines.py

pycodestyle 1-concurrent_coroutines.py
mypy 1-concurrent_coroutines.py

# Tests
touch 1-main.py
chmod +x 1-main.py
./1-main.py
```

### :heavy_check_mark: Solution
> [:point_right: 1-concurrent_coroutines.py](1-concurrent_coroutines.py)


## [2. Measure the runtime](2-measure_runtime.py)
### :page_with_curl: Task requirements.
From the previous file, import wait_n into 2-measure_runtime.py.

Create a measure_time function with integers n and max_delay as arguments that measures the total execution time for wait_n(n, max_delay), and returns total_time / n. Your function should return a float.

Use the time module to measure an approximate elapsed time.
```
bob@dylan:~$ cat 2-main.py
#!/usr/bin/env python3

measure_time = __import__('2-measure_runtime').measure_time

n = 5
max_delay = 9

print(measure_time(n, max_delay))

bob@dylan:~$ ./2-main.py
1.759705400466919
```

### :wrench: Task setup.
```bash
# Create task files and set execute permission.
touch 2-measure_runtime.py
chmod +x 2-measure_runtime.py
./2-measure_runtime.py

pycodestyle 2-measure_runtime.py
mypy 2-measure_runtime.py

# Tests
touch 2-main.py
chmod +x 2-main.py
./2-main.py
```

### :heavy_check_mark: Solution
> [:point_right: 2-measure_runtime.py](2-measure_runtime.py)


