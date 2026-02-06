# Lambda functions in Python

## Videos
https://www.youtube.com/watch?v=j6FCewxjrBM

## Articles
https://www.geeksforgeeks.org/python/python-lambda-anonymous-functions-filter-map-reduce/

## Summary

- Lambda functions are anonymous functions
- They are short lived: creaed and used immediately
- In Python they are created using the `lambda` keyword
- In Python a lambda function must be written on a single line
- In Python they use implicit return (no return statement)
```python
lambda parameter: expression
lambda param_1, param_2: expression
```
- You can assign a lambda function to a variable:
```python
square = lambda num: num * num
```
- A lambda function is usually passed as an argument to another function
- A function that takes another function as an argument is called a `Higher-order function`
- Using a lambda function as argument makes it clear that the lambda function's operation is only needed inside the higher-order function
- Python has several built-in higher-order functions
```python
nums = [1, 2, 3, 4]

map(lambda num: num ** 3, nums)
# map() returns a map object
# use list() to turn the map object into a list
cubed = list(map(lambda num: num ** 3, nums))
```