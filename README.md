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

**3. Reverse and change case**
- [::-1] will reverse a string
- swapcase will change all of the existing letter cases to their opposits

```
def changeAndReverse(txt):
    test = txt.swapcase()
    return test[:: -1]
  
print(changeAndReverse("fuNNyStuFF")
```

**4. Square the numbers**
-  (**) to square numbers    
Something to keep in mind.  These numbers are being passed as an int.  They are not iterable.    
For this reason we change them to a string in the for loop. Working from the inside out,    
we assign test to an int, square the numbers, the revert back to a string so we can    
attacth them to the result.  In the return, we send them back as ints.  The same way they were    
originally sent.

```
def nums(n):
    result = ""
    for test in str(n):
        result += str(int(test) ** 2)
    return int(result)

print(nums(1234))
```

**5. Check if it ends with...**
- .endswith() will check to see if a string ends with a specified element (e.g., string or number)   
Something to keep in mind. In general case append will add one item to the list, while += will copy    
all elements of right-hand-side list into the left-hand-side list.  This is why we use append    
in the else statement rather than ```result += ```.  Otherwise we'd get "s,a,n,d,y,x"

```
def endswith(words):
    
    result = []
    
    for word in words:
        if word.endswith("x"):
            result += [word]
        else:
            result.append(word + "x")
            
    return result


print(endswith(["coolx", "sandy", "funx", "balloon"]))

```

**6. Replace with...**
- .replace().  This takes two parameters (what you're looking for, what you want to replace it with).    
In this case, .replace(letters, something).  So the obvious quesiton might be, "why did you create a copy    
of the string?"  It's because strings are immutable.  If I were to go ```for i in the_str.lower()``` it wouldn't    
work because I would be mutating the string.

```
def replaceMe(the_str):
    
    letters = ("e", "c", "o")
    
    myStr = the_str.lower()
    
    for i in myStr:
        if i in letters:
            myStr = myStr.replace(i,"-")
    return myStr
    

print(replaceMe("get the Cats out"))
```

**7. The shortest word..using len, min, and list comprehension**
- min returns the minimum element 
- len gets the length of elements
- list comprehensions are an abbreviated way to write solutions
- .split() will split each word into a list item

In this case, we'll use the list comprehension syntax, but apply it to a string.  Let's break this apart.    
```for word in input_str.split()``` is splitting the string into individual list items.    
```len(word)``` is then getting the length of those words    
```min()``` is then getting the min or smallest word from the list    

```
def minWord(input_str):
    
    test = min(len(word) for word in input_str.split())
    return test
    
print(minWord("the fish is a swimmer"))

```


