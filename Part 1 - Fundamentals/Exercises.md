Print out **Hello world!** to the terminal.
<details>
<summary>Solution</summary>

```python
print("Hello world!")
```

</details>
<br/>

What are the five main data types in python?
<details>
<summary>Solution</summary>

```
numeric
sequence
dictionary
boolean
set
```

</details>
<br/>

The **numeric** data type can be extended. What types does **numeric** consist of?
<details>
<summary>Solution</summary>

```
int
float
complex
```

</details>
<br/>

The **sequence** data type can be extended. What types does **sequnce** consist of?
<details>
<summary>Solution</summary>

```
string
list
tuple
```

</details>
<br/>

Create a variable of type int and name it **number**. Print its value to the terminal.
<details>
<summary>Solution</summary>

```python
number = 5
print(number)
```

</details>
<br/>

Create a variable of type float and name it **price**. Print its value to the terminal.
<details>
<summary>Solution</summary>

```python
price = 5.99
print(price)
```

</details>
<br/>

Create a variable of type string and name it **name**. Print its value to the terminal.
<details>
<summary>Solution</summary>

```python
name = "John Doe"
print(name)
```

</details>
<br/>

How do you check the type of the previous 3 variables? Print out their types to the terminal.
<details>
<summary>Solution</summary>

```python
print(type(number))
print(type(price))
print(type(name))
```

</details>
<br/>

Create a variable with any value and reassign its value
<details>
<summary>Solution</summary>

```python
my_var = "Hello"
print(my_var)
my_var = "World"
print(my_var)
my_var = 5
print(my_var)
my_var = True
print(my_var)
```

</details>
<br/>

What quotation marks can you use to declare a string in Python?
<details>
<summary>Solution</summary>

Single or double quotations. Example:
```python
string1 = "John Doe"
string2 = 'Mary Jane'
```

</details>
<br/>

How can you declare a string with quotation marks in it?
<details>
<summary>Solution</summary>

 - Use single or and double quotation marks together
```python
print('"A sentence that needs quotation marks"')
```
 - Escape the double quotes within the string
```python
print("\"A word that needs quotation marks\"")
```
 - Use triple-quoted strings
```python
print(""" "A word that needs quotation marks" """)
```

</details>
<br/>

How can you create a long string that has a declaration spread across multiple lines? How will the output look like if you print this variable?
<details>
<summary>Solution</summary>

```python
my_long_string = "Hello and welcome \
to your python tutorial \
where we learn about \
strings"
print(my_long_string)
```

</details>
<br/>

Create a comment in your python file
<details>
<summary>Solution</summary>

```python
# My first comment
```

</details>
<br/>

Create a variable with a long string in it. How do you access the 3. letter in the string? Print out the 2. and 6. letter of this string to the terminal.
<details>
<summary>Solution</summary>

```python
my_long_string = "This is a long sentence"
print("The 2nd letter of the string is ", my_long_string[1])
print("The 6th letter of the string is ", my_long_string[5])
```

</details>
<br/>

How can you get the length of a string?
<details>
<summary>Solution</summary>

```python
my_long_string = "This is a long sentence"
print(len(my_long_string))
```

</details>
<br/>

How can you concatenate two string?
<details>
<summary>Solution</summary>

```python
str1 = "Hello "
str2 = "World!"
print(str1 + str2)
```

</details>
<br/>

You are given two numbers but in the following way. How can you add them together?

```python
num1 = 5
num2 = "6"
```

<details>
<summary>Solution</summary>

```python
num1 = 5
num2 = "6"
result = num1 + int(num2)
print(result)
```

</details>
<br/>

What will be data type of the following variable?

```python
myvar = 5
```

<details>
<summary>Solution</summary>

```python
int
```

</details>
<br/>

What will be data type of the following variable?

```python
myvar = 17.987
```

<details>
<summary>Solution</summary>

```python
float
```

</details>
<br/>

What will be data type of the following variable?

```python
myvar = 'Hello'
```

<details>
<summary>Solution</summary>

```python
str
```

</details>
<br/>

What will be data type of the following variable?

```python
myvar = 1j
```

<details>
<summary>Solution</summary>

```python
complex
```

</details>
<br/>

Write a function that returns the multiple of two given numbers.

<details>
<summary>Solution</summary>

```python
def multiply(num1, num2):
    return num1 * num2
```

</details>
<br/>

What will be the output of the following code?

```python
def divide(num1, num2):
    return num1 / num2

divide(4, 5, 6)
```

<details>
<summary>Solution</summary>

```
TypeError: divide() takes 2 positional arguments but 3 were given
```

</details>
<br/>

What are the two types of conversion in Python? What are the differences?

<details>
<summary>Solution</summary>

- Implicit conversion
- Explicit conversion

</details>
<br/>

What type of conversion happens in the following code?

```python
num1 = 6
num2 = 7.54
print(num1 + num2)
```

<details>
<summary>Solution</summary>

```
Implicit conversion
num1 is implicitly converted from int to float
```

</details>
<br/>

What is the output of the following code?

```python
var1 = "8"
var2 = 7.54
print(var1 + var2)
```

<details>
<summary>Solution</summary>

```
TypeError: can only concatenate str (not "float") to str
```

</details>
<br/>

Cast the following variable to string

```python
num1 = 7.83
```

<details>
<summary>Solution</summary>

```python
num1 = 7.83
str1 = str(num1)
print(str1)
```

</details>
<br/>

What is the output of the following code?

```python
num1 = 7
float1 = float(num1)
print(float1)
```

<details>
<summary>Solution</summary>

```
7.0
```

</details>
<br/>

Ask the user for their name, save the answer in a variable and greet the user.

<details>
<summary>Solution</summary>

```python
name = input('Enter your name:')
print('Hello, ' + name)
```

</details>
<br/>

What will be the output of the following code?

```python
new_list = [1,2,3,4]
new_list[4] = 10
print(new_list)
```

<details>
<summary>Solution</summary>

```
IndexError: list assignment index out of range
```

</details>
<br/>

What will be the output of the following code?

```python
def myfunc(arg):
    print(arg[0])

myfunc({'key1':'hello', 'key2':'world'})
```

<details>
<summary>Solution</summary>

```
KeyError: 0
```

</details>
<br/>