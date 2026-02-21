## How to use this tutorial

Read through the linked tutorials, watch the videos, make notes if you want.

Then go to the **Part 3 -> Exercises** and solve all(!) the exercises. Come back
to these tutorials if needed.

You are encouraged to play around and try new things out, things that are not
in these tutorials.

## Functions

Syntax:
```python
def functioname ():
    # Code body
    # Code body, 2nd line
    return variable
# Code outside the function
```
- use the `def` keyword to define a function
- the function name should be descriptive
- inside the `()` are the function inputs (a.k.a. arguments, parameters)
- the first line of the function (the `def`, the name, the inputs, and the `:`) is also called the function header
- after the header the function lines must be indented by one tab
- within a function, a local namespace is created
    - variables created inside the function are only available inside this namespace
    - variables created inside the function are not available outside the function
- use the `return` keyword to return a value to the calling area
    - the value is returned before the local namespace is discarded
- everything after the header in the function's body
- any unindented code is not considered the part of the function

Example:
```python
# Definition of a function:
def calculate_rectangle_area (length, width):
    area = length * width
    return area

# Call of a function:
rec_area = calculate_rectangle_area(10, 14)
```

## What's next?

Now go to **Part 3 -> Exercises** and solve all(!) exercises. Come back to these
tutorials if needed.