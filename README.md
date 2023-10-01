# Lecture 6 - CIST 1600
## Objectives:
Define and use:
- Lists, tuples, and dictionaries
- Basic list operators, replacing, inserting,
removing an element;
- Dictionary literals,
  - adding and removing keys
  - accessing and replacing values;
- Traversing dictionaries.

### Lists
A list is a sequence of values. In a string, the values are all characters; in a list, they can be any type. The values in a list are called elements or items.

There are several ways to create a list but the easiest is to create values, separated by a comma, inside of square braces []

```
>>> list1 = [2, 3, 5, 6]
>>> print( list1[2] )
>>> list2 = ["Alice", "Bob", "Catherine", "Doug"]
>>> print( list2[2] )
```  

Unlike other languages, the elements of a list do not need to be the same type.
```
>>> list3 = ["apple", 5, "grapes", 23.7]
>>> for element in list3:
...   print(element)
```  
Lists can also be changed, we can update the value at a position.
```
>>> print(list1)
>>> list1[2] = 17
>>> print(list1)
```
#### Traversing a List
There are multiple ways to use loops with a list. Similar to the way strings can be traversed, we will look at visiting each element in a list by its numerical position and by iterating using a for loop.
```
list1 = [3, 1, 4, 1, 5, 9, 2, 6]
position = 0
while position < len(list1):
  print(list1[position])
  position = position + 1
```
This method is the best option if you need to know where you are in a list. For example, if your goal is to remove elements, or search for the location of an item in a list.

Using a for loop, we can iterate across each element of a list. This is useful if we want to print the contents of a list, find the sum of a list, or determine if an element exists in a list (but not where).
```
for item in list1:
  print(item)
```
This allows us to easily traverse a list without ever knowing how long the list is, or keep track of our position in the list.

### List operations
There are several operations you can do to a list. The first operation is joining two lists with the + operator.
```
>>> a = [1, 2, 3]
>>> b = [7, 8, 9]
>>> c = a + b
>>> print (c)
```
In this operation, the two lists are appended to each other and the result is saved to the variable c.
The * operator repeats a list a number of times.
```
>>> [0] * 5
>>> [1, 2, 3] * 3
```

Another useful operation is to add a new element to a list. This can be done in a few ways.
#### append (element)
```
>>> t = ['a', 'b', 'c']
>>> t.append('d')
>>> print(t)
```

#### delete (position)
```
>>> t = ['a', 'b', 'c']
>>> del t[1]
>>> print(t)
```
#### delete (value)
```
>>> t = ['a', 'b', 'c']
>>> t.remove('a')
>>> print(t)
```

#### slicing[start: end]
Slicing a list is very similar to slicing a string, this is because python treats strings as a list of characters.
```
>>> t = ['a', 'b', 'c', 'd', 'e', 'f']
>>> t[1:3]
>>> t[:4]
>>> t[3:]
```
#### Strings -> Lists
While a string is a list of characters, it is possible to make a list of individual words or even a list of individual sentences.
```
>>> s = "This is a sentence."
>>> words = s.split()
>>> print(words)
```

### Dictionaries
Dictionaries are similar to lists but the index is not necessarily an integer. Dictionaries are denoted with braces { } rather than brackets [ ] like a list. The position is still in the brackets.
```
>>> colors = {'red' : 'rojo', 'green' : 'verde', 'blue' : 'azul', 'yellow': 'amarillo'}
>>> colors['blue']
>>> colors['rojo']
>>> colors[3]
```
#### Traversing Dictionaries
What do we get if we wanted to print all the elements in a dictionary?
```
>>> for c in colors:
...   print(c)
```
How could we use that to get all the elements?

### Quiz
1. How many elements are in the list quizScores?
  - quizScores.length()
  - quizScores.length
  - len(quizScores)
  - quizScores.num_elements
1. A list has the number of days in the month.
```
days = [31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31]
```
  How would I display the number of days in February?
  - days[3]
  - days[2]
  - days[1]
  - days['Feb']
1. What is a flaw with this code to remove all the "4" values from a list?
```
nums = [1, 3, 5, 4, 7, 8, 4, 4, 9, 1, 12]
nums.remove(4)
```
1. What is the flaw with this code to remove all the "4" values from a list?
```
nums = [1, 3, 5, 4, 7, 8, 4, 4, 9, 1, 12]
spot = 0
while spot < len(nums):
  if nums[spot] == 4:
    del nums[spot]

  spot = spot + 1
```  
1. A dictionary is created with the number of days in each month.
```
days = {'Jan' : 31, 'Feb' : 28, 'Mar' : 31, 'Apr' : 30, 'May' : 31, 'Jun' : 30, 'Jul' : 31, 'Aug' : 31, 'Sep' : 30, 'Oct' : 31, 'Nov' : 30, 'Dec' : 31}
```
How would in display the number of days in February?
- days[2]
- days[1]
- days['Feb']
- days[28]
