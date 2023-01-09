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


