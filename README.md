theme: Midnight

# emilyytrann.github.io

# Coding Made Easy: Python
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Made with Github")

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

### If-Else Statements
```python
myName = input("What's your name?: ")
if myName == "David":
  print("Hello David!")
  print("You're the baldest person ever.")  
elif myName == "Emily":
  print("Hi Emily!")
else:
  print("You're not David?!")
### will print something for David, something for Emily, and something for everything else
```
| == | =! | <= | >= | <> |
|----|----|----|----|----|
| equal to | not equal to | less than or equal | greather than or equal | less than / greater than |
