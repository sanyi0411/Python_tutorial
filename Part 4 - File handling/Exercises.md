What are the different ways to open a file?

<details>
<summary>Solution</summary>

```python
# open(<file name or location>, <mode>)
open('test.txt', 'r')
```

```python
# the 'with' statement works with the open() function
# the 'with' statement will automatically close the file for you
with open('test.txt', 'r') as file
```

</details>
<br/>

What are the different modes in the ```open()``` function?

<details>
<summary>Solution</summary>

```
 - 'r' - open and read in text format
 - 'rb' - open and read in binary format
 - 'r+' - open for reading and writing
 - 'rb+' - open for reading and writing in binary format
 - 'w' - open for writing, overwrites existing file
 - 'wb' - open for writing in binary format, overwrites existing file
 - 'a' - append data
 - 'ab' - append data in binary format
```

</details>
<br/>

How do you close a file?

<details>
<summary>Solution</summary>

```python
file.close() # Note that it does not take any arguments
```

</details>
<br/>

How can you automatically close the file without explicitly telling it to?

<details>
<summary>Solution</summary>

The ```with``` statement closes the file for you without you telling it to.

```python
with open('test.txt', 'r') as file:
    data = file.readline()
    print(data)
```

</details>
<br/>

What does the ```read()``` function return?

<details>
<summary>Solution</summary>

The ```read()``` method returns the entire contents of the file as a string that will contain all the characters. You can also pass in an integer ```size``` to return only the specified number of bytes in the file. The default is ```size = -1``` which means the whole file.

```python
# Read the whole content of the file
file = open('text.txt', 'r')
data = file.read()
file.close()
```

```python
# Read the first 20 bytes/characters of the file
file = open('text.txt', 'r')
data = file.read(20)
file.close()
```

</details>
<br/>

How can you read a single line from a file?

<details>
<summary>Solution</summary>

Using the ```readline()``` function
```python
file = open('text.txt', 'r')
data = file.readline()
print(data)
file.close()
```

</details>
<br/>

How can you read a specified number of characters from a single line from a file?

<details>
<summary>Solution</summary>

Using the ```readline()``` function, where you can pass in an integer to return only the specified number of bytes from the line.
```python
# Get the first 10 characters from the first line in the file
file = open('text.txt', 'r')
data = file.readline(10)
print(data)
file.close()
```

</details>
<br/>

How can you read multiple lines from a file?

<details>
<summary>Solution</summary>

Using the ```readlines()``` function
```python
file = open('text.txt', 'r')
data = file.readlines()
print(data)
file.close()
```

</details>
<br/>

What does the ```readlines()``` method return?

<details>
<summary>Solution</summary>

It returns the contents (lines) of the file in an ordered list


</details>
<br/>

Create a new file, write your name in the file and then close the file.

<details>
<summary>Solution</summary>

```python
with open('newfile.txt', 'w') as file:
    file.write("John Doe")
```

</details>
<br/>

Create a new file, write multiple lines in it and then close the file.

<details>
<summary>Solution</summary>

```python
with open('newfile.txt', 'w') as file:
    file.writelines(["This is the first line", "\nThis is the second line", "\nThis is the third line"])
```

</details>
<br/>

Open an existing file and append a few lines in it.

<details>
<summary>Solution</summary>

```python
with open('existingfile.txt', 'a') as file:
    file.writelines(["\nFirst appended line", "\nSecond appended line"])
```

</details>
<br/>

What happens if you try to open a file that does not exist? How can you prepare for this?

<details>
<summary>Solution</summary>

It throws a ```FileNotFoundError``` error.
Wrap the ```open()``` in a ```try``` statement.
```python
try:
    with open('samplefile.txt', 'a') as file:
        file.writelines(["\nFirst appended line", "\nSecond appended line"])
except FileNotFoundError as error:
    print("ERROR", error)
```

</details>
<br/>