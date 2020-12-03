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
