# Algorithms

**1. Search an array for a specific item**

- range returns a sequence of numbers starting from 0
- len returns the number of items in an object
```
def findWaldo(names):
  for i in range(len(names)):
    if names[i] == "Waldo":
      return i
  return -1
  

array = ["Frank", "Sally", "Waldo"]
print(findWaldo(array))
```

**2. Only numbers or letters**
- isalpha detects the presence of letters.
- isdigit detects the presence of numbers

```
def numsOrLetters(input_str):
    if input_str.isdigit():
        return True
    if input_str.isalpha():
        return True
    else:
        return False
    
print(numsOrLetters("asdff"))
print(numsOrLetters("fasdf"))
print(numsOrLetters("12fsd"))
```

**2. Reverse and change case**
- [::-1] will reverse a string
- swapcase will change all of the existing letter cases to their opposits

```
def changeAndReverse(txt):
    test = txt.swapcase()
    return test[:: -1]
  
print(changeAndReverse("fuNNyStuFF")
```




