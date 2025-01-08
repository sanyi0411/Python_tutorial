Which one is true?

```
All dictionary comprehension can be written with a for loop

All for loop can be written with a dictionary comprehension
```

<details>
<summary>Solution</summary>

```
All dictionary comprehension can be written with a for loop
```

</details>
<br/>

Given the following dictionary, double the values.

```python
mydict = {'a': 1, 'b': 2, 'c': 3, 'd': 4, 'e': 5}
```

<details>
<summary>Solution</summary>

```python
doubled = {key:value*2 for (key,value) in mydict.items()}
print(doubled)
```
```
{'a': 2, 'b': 4, 'c': 6, 'd': 8, 'e': 10}
```
Note that the order of the key-values pairs is not guaranteed

</details>
<br/>

Create a dictionary where the keys are integers 0-5 and the values are the keys squared.

```
{0: 0, 1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
```

<details>
<summary>Solution</summary>

```python
squared = { n:n**2 for n in range(5) }
```

</details>
<br/>

Create a dictionary where the keys are 2, 4, 6, 8 and the values are the keys squared.

```
{ 2: 4, 4: 16, 6: 36, 8: 64 }
```

<details>
<summary>Solution</summary>

```python
squared1 = { n:n**2 for n in range(2, 9) if n%2 == 0 }
squared2 = { n:n**2 for n in range(2, 9, 2) }
```

</details>
<br/>

Given the following dictionary, create a new dictionary with items where the value is greater than 2.

```
mydict = { 'a': 1, 'b': 2, 'c': 3, 'd': 4, 'e': 5 }
```

<details>
<summary>Solution</summary>

```python
new_dict = { key:value for (key,value) in mydict.items() if value > 2 }
print(new_dict)
```
```
{ 'c': 3, 'd': 4, 'e': 5 }
```

</details>
<br/>