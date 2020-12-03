# algorithms
algorithms

1. Search an array for a specific item

```
def findWaldo(names):
  for i in range(len(names)):
    if names[i] == "Waldo":
      return i
  return -1
  

array = ["Frank", "Sally", "Waldo"]
print(findWaldo(array))
```
