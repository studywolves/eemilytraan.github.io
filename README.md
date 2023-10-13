# emilyytrann.github.io

# Python Notes
![alt text](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.pinterest.com%2Fpin%2F518828819554429602%2F&psig=AOvVaw309zWutYAv2I378Q7rEPdu&ust=1697326065249000&source=images&cd=vfe&opi=89978449&ved=0CBAQjRxqFwoTCNCijbqW9IEDFQAAAAAdAAAAABAE "Underline")
---
***

### Printing
```python
print("Hello World")
print("""
      This will print exactly as it is written in this box.
      """)
print("")
### Will print an indention
```

### Concatentation
```python
print(food, "with", badFood, plant, "on a bed of", item)
### , will print out the users input with a space automatically in between
print(food + " with " + badFood + “ ” + plant + " on a bed of " + item)
### + you have to place in the spaces where you want them
```

### Print in Color
> # “\033[m”
```python
print("You have a", "\033[31m" + "warning" + "\033[0m", "code.")
### You have a warning code. with warming red
print("You have a", "\033[31m", "warning", "\033[0m", "code.")
### You have a  warning  code. with a warning red but with extra spaces
```
| **Color**   | **Value** |
|---------|-------|
| Default | 0     |
| Black   | 30    |
| Red     | 31    |
| Green   | 32    |
| Yellow  | 33    |
| Blue    | 34    |
| Purple  | 35    |
| Cyan    | 36    |
| White   | 37    |
