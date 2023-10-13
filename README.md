# emilyytrann.github.io

# Python Notes

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
# “\033[m”
```python
print("You have a", "\033[31m" + "warning" + "\033[0m", "code.")
### You have a warning code. with warming red
print("You have a", "\033[31m", "warning", "\033[0m", "code.")
### You have a  warning  code. with a warning red but with extra spaces
```
![alt text](https://1drv.ms/i/s!AgMN1JRhFVxWkGegMNJ5rlpDO3yU?e=nmxHdT "Codes to Print in Color")
