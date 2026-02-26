# Python decorators

- A decorator is itself a function
- The purpose of the decorator is to enhance the base function
- The base function is passed to the decorator as an argument
- The decorator wraps the base function in some code
- The decorator returns an enhanced function

```
                       Decorator
                      +---------+           # Code
base_function  --->   |         |  --->   base_function
                      +---------+           # Code

```

## Simple Example
### Implementation
```python
import time

def timer_decorator(base_function):
    def enhanced_func():
        start_time = time.time()
        base_function()
        end_time = time.time()
        print(f"Function '{base_function.__name__}' took {end_time - start_time:.4f} seconds")
    return enhanced_func

def slow_function():
    time.sleep(2)   # Pretend its a long API/DB call
    print("Finished work")
```

### Usage
- Calling the original function will not time it:
```python
slow_function()
```

- This line returns a function object, the enhanced function :
```python
timer_decorator(slow_function)
```

- To call the enhanced function later, you can assign it to a variable:
```python
timed_slow_function = timer_decorator(slow_function)
timed_slow_function()
```

- You can reassign the decorated function back to the original function name
- This ensures that every call to the original function will include the decorator
    - But this hides that the base function is enhanced and it will be timed
    - Someone reading the code for the base function will not see that it is enhanced
```python
slow_function = timer_decorator(slow_function)
```

- You can use the `@` syntax
- Use `@` and the decorator name above the base function definition
    - This makes the decoration an explicit part of the definition
```python
@timer_decorator
def slow_function():
    time.sleep(2)   # Pretend its a long API/DB call
    print("Finished work")
```

## Functions with parameters

- Prerequisites: learn about `*args` and `**kwargs`

```python
import time

def timer_decorator(base_function):
    def enhanced_func(*args, **kwargs):
        start_time = time.time()
        base_function(*args, **kwargs)
        end_time = time.time()
        print(f"Function '{base_function.__name__}' took {end_time - start_time:.4f} seconds")
    return enhanced_func

@timer_decorator
def slow_function(greet, name):
    print(greet)
    time.sleep(1)   # Pretend its a long API/DB call
    print(name)
```

## Functions with return values

- Lets expande the previous example

```python
import time

def timer_decorator(base_function):
    def enhanced_func(*args, **kwargs):
        start_time = time.time()
        result = base_function(*args, **kwargs)
        end_time = time.time()
        print(f"Function '{base_function.__name__}' took {end_time - start_time:.4f} seconds")
        return result
    return enhanced_func

@timer_decorator
def slow_function(greet, name):
    print(greet)
    time.sleep(1)   # Pretend its a long API/DB call
    print(name)
```

## Why use it?
- Why use decorator? Why not just copy the decorator's code into the base function?
    - This would violate the single responsibility principle
    - The base function would do more than its name suggets
    - The enhancement part of the code is not resuable