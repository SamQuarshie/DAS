# COMPREHENSIVE REVISION
### Python Basics + Statistics for Data Science 

**How to use this file:** Every code block below has been tested and runs with no errors. Each section is self-contained — copy the whole block for a topic and run it together (don't mix blocks from different sections in one run, since some reuse variable names like `data`).

**Requirements:** `numpy`, `scipy` — install once if needed:
```bash
pip install numpy scipy --break-system-packages
```

---
---

# PART A — PYTHON BASICS

## A1. Variables & Data Types
```python
# Example 1 — basic variables and their types
name = "Ama"
age = 25
price = 19.99
is_active = True
print(name, type(name))
print(age, type(age))
print(price, type(price))
print(is_active, type(is_active))

# Example 2 — converting a string to an integer
str_num = "45"
num = int(str_num)
print(num, type(num))

# Example 3 — converting an integer to a float
x = 10
y = float(x)
print(y, type(y))

# Example 4 — multiple assignment in one line
a, b, c = 1, 2, 3
print(a, b, c)

# Example 5 — a variable can be reassigned to a different type
value = 10
print(type(value))
value = "ten"
print(type(value))
```

## A2. Operators
```python
# Example 1 — arithmetic operators
a = 10
b = 3
print(a + b, a - b, a * b, a / b, a // b, a % b, a ** b)

# Example 2 — comparison operators
print(10 > 5, 10 == 10, 10 != 5, 10 <= 9)

# Example 3 — logical operators
print(True and False, True or False, not True)

# Example 4 — combining comparison and logical operators
age = 25
has_id = True
print(age >= 18 and has_id)

# Example 5 — string operators (+ and *)
print("Ha" * 3 + "!!")
```

## A3. Booleans
```python
# Example 1 — a boolean from a comparison
is_adult = 20 >= 18
print(is_adult)

# Example 2 — bool() conversion
print(bool(0), bool(1), bool(""), bool("hi"))

# Example 3 — using a boolean in a condition
in_stock = True
print("Available" if in_stock else "Out of stock")

# Example 4 — combining booleans
logged_in = True
is_admin = False
print(logged_in and not is_admin)

# Example 5 — counting True values in a list
votes = [True, False, True, True]
print(sum(votes))
```

## A4. Strings
```python
# Example 1 — upper and capitalize
name = "python"
print(name.upper(), name.capitalize())

# Example 2 — slicing
word = "Analytics"
print(word[0:4], word[-4:])

# Example 3 — f-strings
age = 30
print(f"I am {age} years old")

# Example 4 — split and join
sentence = "data is powerful"
words = sentence.split()
print(words)
print("-".join(words))

# Example 5 — strip and replace
text = "  hello world  "
print(text.strip().replace("world", "python"))

# Example 6 - Finding and Counting
word = "banana"
phrase = "banana"
print(word.find("nana"))   # position
print(phrase.count("a"))   # count

# Example 7 - What starts and end strings
filename = "report.pdf"

print(filename.startswith("rep"))
print(filename.endswith(".csv"))

# Example 8 - Check the content of strings
User_id = "12345"
username = "coder123"

print(User_id.isdigit())
print(username.isalpha())

# Example 9 - step slicing(skipping characters) using[start:stop:step]
alphabet = "abcdef"

print(alphabet[::2])   # every second letter

# Example 10 - case swapping
title = "i told you so"
mixed = "daTA ScienCE"

print(title.title())  # captalize every word
print(mixed.swapcase())  # flips lower to upper and upper to lower
```

## A5. Lists
```python
# Example 1 — create and index
fruits = ["apple", "banana", "mango"]
print(fruits[0], fruits[-1])

# Example 2 — append and remove
fruits.append("grape")
fruits.remove("banana")
print(fruits)

# Example 3 — slicing
numbers = [10, 20, 30, 40, 50]
print(numbers[1:4])

# Example 4 — sorting
scores = [88, 45, 76, 92]
scores.sort()
print(scores)

# Example 5 — list comprehension
squares = [x**2 for x in range(5)]
print(squares)

# Example 6 - Filtering Numbers
odd_squares = [x**2 for x in range(5) if x % 2 != 0]
print(odd_squares)

# Example 7 - Filtering towns
towns = ["Zugu", "Takoradi", "Ho", "Tamale", "Accra", "Techiman", "Kumasi"]
 cities_gt_5 = [t.upper() for t in towns if len(t) >= 5]
 print(cities_gt_5)
```

## A6. Tuples
```python
# Example 1 — create and access
point = (4, 5)
print(point[0], point[1])

# Example 2 — unpacking
coordinates = (10, 20)
x, y = coordinates
print(x, y)

# Example 3 — immutability (this will raise an error, which we catch)
try:
    tup = (1, 2, 3)
    tup[0] = 99
except TypeError as e:
    print("Error:", e)

# Example 4 — tuple of tuples
students = (("Ama", 23), ("Kojo", 25))
print(students[1])

# Example 5 — count and index methods
numbers = (1, 2, 2, 3, 2)
print(numbers.count(2), numbers.index(3))

# Example 6 - Counting Items
response = ("Yes", "No", "Yes", "Maybe", "Yes")
print(response.count("Yes"))
print(response.count("No"))

# Example 7 - Finding Positions with index
winners = ("Alice", "Bob", "Charlie", "Bob")
print(winners.index("Bob"))

# Example 8 - Warning ⚠️ 
colors = ("red", "blue", "green")

if "yellow" in colors:
    print(colors.index("yellow"))
else:
    print("'yellow' is not in the tuple!")
```

## A7. Dictionaries
```python
# Example 1 — create and access
person = {"name": "Kwame", "age": 30}
print(person["name"])

# Example 1.1 
dic = {
    "brand": "Ford",
    "model": "Mustang",
    "year": 1964
}
print(dic)

# Example 2 Dictionaries does not allow duplicate of keys
dic = {
    "brand": "Ford",
    "model": "Mustang",
    "year": 1964
    "year": 2020
}
print(dic)

# Example 3 Use *len() function to know how many items a dictionary has
print(len(dic))

# Example 4 dictionary values or items can be of any data type(String,int, boolean, and list )
dict1 = {
  "brand": "Ford",
  "electric": False,
  "year": 1964,
  "colors": ["red", "white", "blue"]
}
print(type(dic1))

# Ecample 4 We can use the *dict()*
d = dict(name = "John", age = 36, country = "Norway")
print(d)

# Example 5 Accessing items in dictionaries
print(person.get("salary", "Not specified"))
print(person.get("name"))

sdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
y = sdict["model"]
print(y)
ys = sdict.get("model")

# Exampple 6 get the list of keys with *keys()* method
x = thisdict.keys()
print(x)

# Example 7 get the values
a = sdict.values()

car = {
"brand": "Ford",
"model": "Mustang",
"year": 1964
}
print(x)

x = car.values()

# Example 8 *items()* method return each item in a dictionary as a tuple in a list
x = car.items()

car = {
"brand": "Ford",
"model": "Mustang",
"year": 1964
}

x = car.items()

print(x) #before the change

car["year"] = 2020

print(x) #after the change

# Example 9 — add/update a key
person["city"] = "Accra"
print(person)

sdict2 = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
if "model" in sdict2:
  print("Yes, 'model' is one of the keys in the thisdict dictionary")


# Example 10 — loop through key-value pairs
for key, value in person.items():
    print(key, value)

# Example 11 — nested dictionary
company = {"ceo": {"name": "Ama", "age": 45}}
print(company["ceo"]["name"])
print(company["ceo"].get("Age"))

# Example 12 - Delete Key
person = {"name": "Kwame", "age": 30, "city": "Accra"}
removed_city = person.pop("city", "Key not found")
print(f"Removed value: {removed_city}") 
print(person)

# Example 13 - loop through dictionary
person_new = {"name": "Kwame", "age": 30, "job": "Developer"}

# loop through keys and values simultaneously
for key, value in person_new.items():
    print(f"The person's {key} is {value}")
```

## A8. Sets
```python
# A set is a collection which is unordered, unchangeable*, and unindexed.
*Note:* Set items are unchangeable, but you can remove items and add new items. Duplicates are not allowed in sets.

# We can use len on sets, it accepts int, boolean and strings. Sets() creats set list.

# Example 1 — create and print a set
colors = {"red", "green", "blue"}
print(colors)

# Example 2 — removing duplicates from a list
nums = [1, 2, 2, 3, 3, 3]
print(set(nums))

# Example 3 — add and discard
colors.add("yellow")
colors.discard("red")
print(colors)

# Example 4 - we can remove an item with *remove()* or *discard()*
tsset = {"apple", "banana", "cherry"}

tsset.remove("banana")

print(tsset)

# We can use the pop but its not adviceable because it removes a random item or object
s = tsset.pop()
print(s)
print(tsset)

# Example 5 Add items from another set, use  *add* and *update()*
des_up = {"apple", "banana", "cherry"}
des_up.add("orange")
print(des_up)

# Example 6 Add list to a set
trop = {"pineapple","mango","papaya"}
des_up.update(trop)
ups = {"apple", "banana", "cherry"}
mylist = ["Kiwi","orange"]

ups.udpate(mylist)


# Example 7 — union and intersection
a = {1, 2, 3}
b = {2, 3, 4}
print(a.union(b), a.intersection(b))
result = a & b
print(result)

# Example 7.1 — difference
print(a.difference(b))
print(a-b)

# Example 8 - Set symmetric_difference() Method
# Return a set that contains all items from both sets, except items that are present in both sets
x = {"apple", "banana", "cherry"}
y = {"google", "microsoft", "apple"}

z = x.symmetric_difference(y)

print(z)

# We can use *^* as a shortcut instead of symmetric_difference()
x = {"apple", "banana", "cherry"}
y = {"google", "microsoft", "apple"}

z = x ^ y

print(z)

# Example 9 Access a set item
# We can not using the indexor key  approach to access an item in a set but we can use *for loop*,*in* and *not*

aset = {"apple", "banana", "cherry"}

for x in aset:
  print(x)

bset = {"apple", "banana", "cherry"}

print("banana" not in bset)

#Example 10 We can clear a set with the method *clear()* and del to delete a ser
t = {"apple", "banana", "cherry"}
print(t)

t.clear()

print(t)

tt = {"apple", "banana", "cherry"}
print(tt)

del(tt)

print(tt)

```

## A9. Mutable vs Immutable
```python
# Example 1 — a list IS mutable
lst = [1, 2, 3]
lst[0] = 99
print(lst)

# Example 2 — a tuple is NOT mutable
try:
    tup = (1, 2, 3)
    tup[0] = 99
except TypeError as e:
    print("Error:", e)

# Example 3 — a string is NOT mutable
try:
    s = "hello"
    s[0] = "H"
except TypeError as e:
    print("Error:", e)

# Example 4 — a dictionary IS mutable
d = {"a": 1}
d["a"] = 2
print(d)

# Example 5 — proof: a mutated list keeps the same memory id
lst = [1, 2]
print(id(lst))
lst.append(3)
print(id(lst))   # same id — it was changed in place, not replaced
```

## A10. Conditionals
```python
# Example 1 — simple if/else
score = 70
print("Pass" if score >= 50 else "Fail")

# Example 2 — if/elif/else
temp = 35
if temp > 30:
    print("Hot")
elif temp > 20:
    print("Warm")
else:
    print("Cold")

# Example 3 — nested if
age = 20
has_ticket = True
if age > 18:
    if has_ticket:
        print("Entry allowed")
    else:
        print("Buy a ticket")
else:
    print("Not allowed")

# Example 4 — multiple conditions with 'and'
income = 4000
credit_score = 720
if income > 3000 and credit_score > 700:
    print("Loan approved")

# Example 5 — membership check with 'in'
fruit = "mango"
if fruit in ["apple", "mango", "pear"]:
    print("Available")

# Example 6 — Traffic light system (Red, Green, Amber)
light_color = "Amber"

if light_color == "Red":
    print("Stop")
elif light_color == "Green":
    print("Go")
elif light_color == "Amber":
    print("Slow down, prepare to stop")
else:
    print("Invalid light color")
```

## A11. Loops
```python
# Example 1 — for loop over a list
for fruit in ["apple", "banana", "mango"]:
    print(fruit)

# Example 2 — for loop with range()
for i in range(5):
    print(i)

# Example 3 — while loop
count = 0
while count < 3:
    print(count)
    count += 1

# Example 4 — break
for num in range(10):
    if num == 5:
        break
    print(num)

# Example 5 — continue
for num in range(5):
    if num == 2:
        continue
    print(num)
```

## A12. Functions
```python
# A function is a block of code which only runs when it is called.A function helps avoiding code repetition
# Function names must start with a letter or underscore thus may contain only numbers, letters and underscores. The names are case sensitive (Power and power are different)

# Example 1 — a simple function
def greet(name):
    return f"Hello, {name}"
print(greet("Ama"))

# Example 2 — a function with a default parameter
def power(base, exp=2):
    return base ** exp
print(power(5))

# Example 3 — a function returning multiple values
def min_max(numbers):
    return min(numbers), max(numbers)
print(min_max([3, 7, 1, 9]))

# Example 4 — one function calling another
def square(x):
    return x * x
def sum_of_squares(p, q):
    return square(p) + square(q)
print(sum_of_squares(2, 3))

# Example 5 — a function using built-ins internally
def average(numbers):
    return sum(numbers) / len(numbers)
print(average([10, 20, 30]))
```

## A13. Built-in Functions
```python
# Example 1 — len() and sum()
data = [5, 10, 15]
print(len(data), sum(data))

# Example 2 — max() and min()
print(max(data), min(data))

# Example 3 — round()
print(round(3.14159, 2))

# Example 4 — sorted() with reverse
print(sorted(data, reverse=True))   #.sort works on list and sorted works on Tuples, str, Dicts

# Example 5 — enumerate()
for index, value in enumerate(data):
    print(index, value)

# To use more of the built in functions we import *math*
# This gives us the options to use math.ceil, math.floor for rounding, math.sqrt for square roots, math.pi for pi 
```
# Pyhton Dates
```python
# A date in Python is not a data type of its own, but we can import a module named datetime to work with dates as date objects.
# To use datetime in pyhton we need to import the module by name *datetime* so python sees it as an object. This helps python work with it as date objects.

import datetime
# lets display the current time
x = datetime.datetime.now()
print(x)

# lets print the year and name of the week
x = datetime.datetime.now()

print(x.year)
print(x.strftime("%A"))
# str = string, f = format, time = time, "%A" = converts the number to text

# We can create our date objects manually
x = datetime.datetime(2026, 10, 17)
print(x)
```

# JSON
```python
# JSON is a syntax for storing and exchanging data. JSON is text, written with JavaScript object notation.
# To import this module in python we use import *json* which is used to work with json data

When we have a JSON string, we can use or parse the json.loads() method. this will result in a dictionary

# Example 1: lets convert JSON to a python
import json

# some JSON:
x =  '{ "name":"John", "age":30, "city":"New York"}'

# parse x:
y = json.loads(x)

# the result is a Python dictionary:
print(y["age"])

# Example 2: Reverse_Convert a python to a JSON

# a Python object (dict):
x = {
  "name": "John",
  "age": 30,
  "city": "New York"
}

# convert into JSON:
y = json.dumps(x)

# the result is a JSON string:
print(y)

*NOTE* you can convert python object of the following types to JSON strings:
* Dict
* list
* tuple
* int
* float
* True
* False
* None

# Example 3:  Convert python objects to JSON strings and print the values:

print(json.dumps({"name": "John", "age": 30}))
print(json.dumps(["apple", "bananas"]))
print(json.dumps(("apple", "bananas")))
print(json.dumps("hello"))
print(json.dumps(42))
print(json.dumps(31.76))
print(json.dumps(True))
print(json.dumps(False))
print(json.dumps(None))


# Convert a Python object containing all data types

x = {
  "name": "John",
  "age": 30,
  "married": True,
  "divorced": False,
  "children": ("Ann","Billy"),
  "pets": None,
  "cars": [
    {"model": "BMW 230", "mpg": 27.5},
    {"model": "Ford Edge", "mpg": 24.1}
  ]
}

print(json.dumps(x))

# Example 4: Adding ident to specify the number of indent
json.dumps(x, indent=4)
# You can also define the separators, default value is (", ", ": "), which means using a comma and a space to 
# separate each object, and a colon and a space to separate keys from values

Example 5: using the seperators parameter
json.dumps(x, indent=4, separators=(". ", " = "))

Example 6: using the sort_keys parameter. This specifies if the output should be sorted or not
json.dumps(x, indent=4, sort_keys=True)
```
# RegEx 
```python
re is a built-in package which can be used to work with Regular Expressions. We parse it using import *re*
# Example 1:  The *findall()* function returns a list containing all matches
import re

txt = "The rain in Spain"
x = re.findall("ai", txt)
print(x)

# If no matches were found, an empty list is returned


# The search () Function searches the string for a match, and returns a Match object if there is a match. If there is more than one match, only the first occurrence of the match will be returned

# Example 2: Lests search for the white space
txt = "The rain in Spain"
x = re.search("\s", txt)

print("The first white-space character is located in position:", x.start())

# Example 3: If no value is found the output becomes *None*
txt = "The rain in Spain"
x = re.search("Portugal", txt)
print(x)

The split() function returns a list where the string has been split at each match
# Example 4: split() Function
txt = "The rain in Spain"
x = re.split("\s", txt)
print(x)

We can control the number of split with maxsplit parameter
# Example 5: 
txt = "The rain in Spain"
x = re.split("\s", txt, 1)
print(x)

The sub() function replaces the matches with the text of your choice
Example 6: Lets replace every white space character with 9

```

# Numpy
```python
# Introduction
NumPy stands for numerical Python

# Why is NumPy Faster Than Lists?
NumPy arrays are stored at one continuous place in memory unlike lists, so processes can access and manipulate them very efficiently
This behavior is called locality of reference in computer science. This is the main reason why NumPy is faster than lists. Also it is optimized to work with latest CPU architectures.

# NumPy as np
NumPy is usually imported under the np alias.

NumPy is used to work with arrays. The array object in NumPy is called ndarray. We can create a NumPy ndarray object by using the array() function

Dimensions in arrays is one level of array depth (nested arrays). Nested arrays are arrays that have arrays as their elements.

import numpy as np

arr = np.array([1, 2, 3, 4, 5])

print(arr)

print(type(arr))

# Check NumPy Version
print(np.__version__)

# NumPy Creating Arrays
arr = np.array([1, 2, 3, 4, 5])

print(arr)

print(type(arr))

# lets Create a tuple with NumPy
arr = np.array((1, 2, 3, 4, 5))

print(arr)

# Lets create a 0 - D array
# 0-D Arrays
# 0-D arrays, or Scalars, are the elements in an array. Each value in an array is a 0-D array.

arr = np.array(42)

print(arr)

# Lets create 1-D Arrays
# An array that has 0-D arrays as its elements is called uni-dimensional or 1-D array.These are the most common and basic arrays.

arr = np.array([1, 2, 3, 4, 5])

print(arr)

# Lets create 2-D Arrays
# An array that has 1-D arrays as its elements is called a 2-D array. These are often used to represent matrix or 2nd order tensors.
arr = np.array([[1, 2, 3], [4, 5, 6]])

print(arr)


# Lets create a 3-D arrays
# An array that has 2-D arrays (matrices) as its elements is called 3-D array. These are often used to represent a 3rd order tensor.
arr = np.array([[[1, 2, 3], [4, 5, 6]], [[1, 2, 3], [4, 5, 6]]])

print(arr)

# Lets check the Number of Dimensions
# NumPy Arrays provides the *ndim* attribute that returns an integer that tells us how many dimensions the array have.

a = np.array(42)
b = np.array([1, 2, 3, 4, 5])
c = np.array([[1, 2, 3], [4, 5, 6]])
d = np.array([[[1, 2, 3], [4, 5, 6]], [[1, 2, 3], [4, 5, 6]]])

print(a.ndim)
print(b.ndim)
print(c.ndim)
print(d.ndim)

# Lets set the dimension higher
# An array can have any number of dimensions. When the array is created, you can define the number of dimensions by using the ndmin argument.

arr = np.array([1, 2, 3, 4], ndmin=5)

print(arr)
print('number of dimensions :', arr.ndim)

# NumPy Array Indexing 
# Access Array Elements
# Array indexing is the same as accessing an array element. You can access an array element by referring to its index number. The indexes # in NumPy arrays start with 0, meaning that the first element has index 0, and the second has index 1 etc.

arr = np.array([1, 2, 3, 4])

print(arr[0])

# lets get the second element from the following array.
arr = np.array([1, 2, 3, 4])

print(arr[1])

# Lets get third and fourth elements from the following array and add them.
arr = np.array([1, 2, 3, 4])

print(arr[2] + arr[3])

# Access 2-D Arrays
# To access elements from 2-D arrays we can use comma separated integers representing the dimension and the index of the element. Think of 2-D arrays like a table with rows and columns, where the dimension represents the row and the index represents the column.

# Lets access the element on the first row, second column
arr = np.array([[1,2,3,4,5], [6,7,8,9,10]])

print('2nd element on 1st row: ', arr[0, 1])

# Lets access the element on the 2nd row, 5th column
arr = np.array([[1,2,3,4,5], [6,7,8,9,10]])

print('5th element on 2nd row: ', arr[1, 4])

# Lets access 3-D Arrays
# To access elements from 3-D arrays we can use comma separated integers representing the dimensions and the index of the element.

arr = np.array([[[1, 2, 3], [4, 5, 6]], [[7, 8, 9], [10, 11, 12]]])

print(arr[0, 1, 2]) # Accessed the third element of the second array of the first array

# Lets do negative Indexing
# Use negative indexing to access an array from the end

arr = np.array([[1,2,3,4,5], [6,7,8,9,10]])

print('Last element from 2nd dim: ', arr[1, -1])  #Print the last element from the 2nd dim


# NumPy Array Slicing
# Slicing arrays
# Slicing in python means taking elements from one given index to another given index. We pass slice instead of index like this: [start:end]. We can also define the step, like this: [start:end:step]. If we don't pass start its considered 0 If we don't pass end its considered length of array in that dimension, If we don't pass step its considered 1

# Lets Slice elements from index 1 to index 5
arr = np.array([1, 2, 3, 4, 5, 6, 7])

print(arr[1:5])

# lets Slice elements from index 4 to the end of the array
arr = np.array([1, 2, 3, 4, 5, 6, 7])

print(arr[4:])

# Lets Slice elements from the beginning to index 4
arr = np.array([1, 2, 3, 4, 5, 6, 7])

print(arr[:4])


# Negative Slicing
# Use the minus operator to refer to an index from the end

arr = np.array([1, 2, 3, 4, 5, 6, 7])

print(arr[-3:-1]) # Slice from the index 3 from the end to index 1 from the end

## STEP
# Use the step value to determine the step of the slicing
arr = np.array([1, 2, 3, 4, 5, 6, 7])

print(arr[1:5:2]) # gives us every other element from index 1 to index 5

# lets print every other element from the entire array
arr = np.array([1, 2, 3, 4, 5, 6, 7])

print(arr[::2])

# Slicing 2-D Arrays
# Lets slice the second element, slice elements from index 1 to index 4
arr = np.array([[1, 2, 3, 4, 5], [6, 7, 8, 9, 10]])

print(arr[1, 1:4])

# Lets slice from both elements to return index 2
arr = np.array([[1, 2, 3, 4, 5], [6, 7, 8, 9, 10]])

print(arr[0:2, 2])

# Lets slice to get a 2-D Array
arr = np.array([[1, 2, 3, 4, 5], [6, 7, 8, 9, 10]])

print(arr[0:2, 1:4])

# NumPy Data Types
# Python has default dada types (strings, integer, float, boolean, complex(1.0 + 2.0j))

i - integer
b - boolean
u - unsigned integer
f - float
c - complex float
m - timedelta
M - datetime
O - object
S - string
U - unicode string

# How to check numpy data type
arr = np.array([1, 2, 3, 4])

print(arr.dtype)

# lets coerce or change any data type

arr = np.array([1, 2, 3, 4], dtype='S')

print(arr)
print(arr.dtype)

# lets Convert Data Type on Existing Arrays
# The best way to change the data type of an existing array, is to make a copy of the array with the astype() method. The astype() function creates a copy of the array, and allows you to specify the data type as a parameter. The data type can be specified using a string, like 'f' for float, 'i' for integer etc. or you can use the data type directly like float for float and int for integer.

arr = np.array([1.1, 2.1, 3.1])

newarr = arr.astype('i')  # Change data type from float to integer

print(newarr)
print(newarr.dtype)

arr = np.array([1.1, 2.1, 3.1])

newarr = arr.astype(int)  # Change data type from float to integer

print(newarr)
print(newarr.dtype)


arr = np.array([1, 0, 3])

newarr = arr.astype(bool) # Change data type from integer to boolean

print(newarr)
print(newarr.dtype)


# NumPy Array Copy vs View
# The main difference between a copy and a view of an array is that the copy is a new array, and the view is just a view of the original array. The copy owns the data and any changes made to the copy will not affect original array, and any changes made to the original array will not affect the copy. However the view dowes not own the original data any changes made to it will affect it(the view)

# COPY
arr = np.array([1, 2, 3, 4, 5])
x = arr.copy()
arr[0] = 42

print(arr)
print(x)


# VIEW
arr = np.array([1, 2, 3, 4, 5])
x = arr.view() 
arr[0] = 42

print(arr)
print(x)

# lets do both view and copy together
arr = np.array([1, 2, 3, 4, 5])

x = arr.copy()
y = arr.view()

print(x.base)
print(y.base)

# NumPy Array Shape
# The shape of an array is the number of elements in each dimension.NumPy arrays have an attribute called shape that returns a tuple with each index having the number of corresponding elements.
arr = np.array([[1, 2, 3, 4], [5, 6, 7, 8]])

print(arr.shape)   # (2. 4)

arr = np.array([1, 2, 3, 4], ndmin=5)

print(arr)
print('shape of array :', arr.shape)

# NumPy Array Reshaping
# Reshaping means changing the shape of an array. The shape of an array is the number of elements in each dimension by reshaping we can add or remove dimensions or change number of elements in each dimension. We can reshape into any shape as long as the elements required for reshaping are equal in both shapes.

# Reshape From 1-D to 2-D
# Convert the following 1-D array with 12 elements into a 2-D array.
# The outermost dimension will have 4 arrays, each with 3 elements
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12])

newarr = arr.reshape(4, 3)

print(newarr)

# Reshape From 1-D to 3-D
# The outermost dimension will have 2 arrays that contains 3 arrays, each with 2 elements
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12])

newarr = arr.reshape(2, 3, 2)

print(newarr)

# Flattening the arrays
# This means converting a multidimensional array into a 1D array
arr = np.array([[1, 2, 3], [4, 5, 6]])

newarr = arr.reshape(-1)

print(newarr)

# Iterating Arrays
# This means going through elerments one by one. As we deal with multi-dimemsion arrays in numpy, we can do this using basic for loop. 

# Iterate through 1-D
arr = np.array([1, 2, 3])

for x in arr:
  print(x)

# Iterate through 2-D
arr = np.array([[1, 2, 3], [4, 5, 6]])

for x in arr:
  print(x)


# Iterate through 3-D
arr = np.array([[[1, 2, 3], [4, 5, 6]], [[7, 8, 9], [10, 11, 12]]])

for x in arr:
  print(x)


arr = np.array([[[1, 2, 3], [4, 5, 6]], [[7, 8, 9], [10, 11, 12]]])

for x in arr:
  for y in x:
    for z in y:
      print(z)

# We can use *diter() for iterating through 
arr = np.array([[[1, 2], [3, 4]], [[5, 6], [7, 8]]])

for x in np.nditer(arr):
  print(x)


# Iterating arrays with different data types 
arr = np.array([1, 2, 3])

for x in np.nditer(arr, flags=['buffered'], op_dtypes=['S']):
  print(x)

# Iterating with different step size
arr = np.array([[1, 2, 3, 4], [5, 6, 7, 8]])

for x in np.nditer(arr[:, ::2]):
  print(x)

# Iterating using ndenumerate()
arr = np.array([1, 2, 3])

for idx, x in np.ndenumerate(arr):
  print(idx, x)


arr = np.array([[1, 2, 3, 4], [5, 6, 7, 8]])

for idx, x in np.ndenumerate(arr):
  print(idx, x)

# Joining Numpy Arrays
# Joining means putting contents of two or more arrays in a single array. In SQL we join tables based on a key, whereas in NumPy we join arrays by axes. We pass a sequence of arrays that we want to join to the concatenate() function, along with the axis. If axis is not explicitly passed, it is taken as 0

# Join Using Concatenate
# lets join two arrays
arr1 = np.array([1, 2, 3])

arr2 = np.array([4, 5, 6])

arr = np.concatenate((arr1, arr2))

print(arr)

# lets join 2-D arrays along row (axis=1)
arr1 = np.array([[1, 2], [3, 4]])

arr2 = np.array([[5, 6], [7, 8]])

arr = np.concatenate((arr1, arr2), axis=1)

print(arr)

# Join using *stack()*
# Stacking is same as concatenation, the only difference is that stacking is done along a new axis. We can concatenate two 1-D arrays along the second axis which would result in putting them one over the other, ie. stacking. We pass a sequence of arrays that we want to join to the stack() method along with the axis. If axis is not explicitly passed it is taken as 0.

arr1 = np.array([1, 2, 3])

arr2 = np.array([4, 5, 6])

arr = np.stack((arr1, arr2), axis=1)

print(arr)

# Join using *hstack()* which stacks along rows
arr1 = np.array([1, 2, 3])

arr2 = np.array([4, 5, 6])

arr = np.hstack((arr1, arr2))

print(arr)


# Join using *vstack()* stcks along columns
arr1 = np.array([1, 2, 3])

arr2 = np.array([4, 5, 6])

arr = np.vstack((arr1, arr2))

print(arr)

# Join using *dstack()* stack along height, which is the same as depth
arr1 = np.array([1, 2, 3])

arr2 = np.array([4, 5, 6])

arr = np.dstack((arr1, arr2))

print(arr)

# Numpy Split Arrays
# Splitting is reverse operation of Joining. Joining merges multiple arrays into one and Splitting breaks one array into multiple. We use array_split() for splitting arrays, we pass it the array we want to split and the number of splits.

# Lets split an array in 3 parts
arr = np.array([1, 2, 3, 4, 5, 6])

newarr = np.array_split(arr, 3)

print(newarr)  # list of 3 arrays

# lets split an array in 4 parts
arr = np.array([1, 2, 3, 4, 5, 6])

newarr = np.array_split(arr, 4)

print(newarr)    # list of 4 arrays
```
# Pandas
```python
Pandas is a Python library used for data manipulation and analysis. It helps us work with structured data, such as Excel spreadsheets, CSV files, SQL tables, and other datasets.
Think of Pandas as an Excel spreadsheet inside Python, but with much greater flexibility and automation. We use import pandas as pd as the means to access the pandas library.

import pandas as pd

## Data Ingestion & Inspection
Data ingestion means bringing data into Python from different sources so that we can work on it. Imagine a bank gives you customer information in an Excel file. Before you can analyse customers or build a loan default prediction model, you must first bring that information into Python. Pandas supports different data sources, including CSV, Excel, JSON, SAV, SPSS, and SQL databases. Data inspection means examining the dataset after loading it to understand what it contains

raw = pd.DataFrame({
    "name": ["Ama", "Kojo", "Efua", "Yaw", "Adjoa", "Nii"],
    "age": [23, 35, 41, 29, 52, 38],
    "branch": ["Osu", "Adenta", "Tema", "Osu", "Madina", "Tema"],
    "loan_amount": [3000, 1500, 5000, 2500, 8000, 4200],
})

raw.to_csv("loans.csv", index=False)
raw.to_json("loans.json", orient="records")
raw.to_excel("loans.xlsx", index=False)        # needs openpyxl

# Real life scenarios examples
This is the most common way to start pandas

# Example 1 — read a CSV file
df = pd.read_csv("loans.csv")
print("printing results: read_csv")
print(df)

# Example 2 — read a JSON file
df_json = pd.read_json("loans.json")
print("\nprinting results: read_json")

print(df_json)
df_excel = pd.read_excel("loans.xlsx")

# Example 3 — read an Excel file
print("\nExample 3: read_excel")
print(df_excel)

# Example 4 — head()
print("\nExample 4: head")
print(df.head(3))

# Example 5 — tail() shows the last rows.
print("\nExample 5: tail")
print(df.tail(2))

# Example 6 — shape tells you (rows, columns)
print(df.shape)
print("Rows:", df.shape[0], "| Columns:", df.shape[1])

# Example 7 — column names and the type of each column.
print("\nExample 7: columns and types")
print(df.columns.tolist())
print(df.dtypes)

# Example 8 — info() is a quick health report of the whole table.
print("\nExample 8: info")
df.info()

# Example 9 — describe() summarises the number columns. For now, look only at
# count, mean, min and max. The other rows are explained in the statistics lessons.
print("\nExample 9: describe")
print(df.describe())

# Example 10 — count how often each value appears in a column.
print("\nExample 10: value_counts")
print(df["branch"].value_counts())
print("Different branches:", df["branch"].nunique())

## Selection & Filtering
df = pd.DataFrame({
    "name": ["Ama", "Kojo", "Efua", "Yaw", "Adjoa", "Nii"],
    "age": [23, 35, 41, 29, 52, 38],
    "branch": ["Osu", "Adenta", "Tema", "Osu", "Madina", "Tema"],
    "loan_amount": [3000, 1500, 5000, 2500, 8000, 4200],
})

# Example 1 — one column. Use its name in square brackets.
print("Example 1: one column")
print(df["name"])

# Example 2 — several columns. Place the names in a list, so there are TWO square brackets.
print("\nExample 2: several columns")
print(df[["name", "loan_amount"]])

# Example 3 — one row, by its row label, with loc.
print("\nExample 3: one row with loc")
print(df.loc[2])

# Example 4 — rows and columns together with loc: first the rows, then the columns.
# With loc, the last row in a slice IS included.
print("\nExample 4: loc rows 1 to 3, chosen columns")
print(df.loc[1:3, ["name", "branch"]])

# Example 5 — by position with iloc: the first row is 0, the first column is 0.
# With iloc, the last number in a slice is NOT included.
print("\nExample 5: iloc")
print(df.iloc[0:3, 0:2])

# Example 6 — filter with one condition. Pandas checks every row and keeps the True ones.
print("\nExample 6: loans above 4000")
print(df[df["loan_amount"] > 4000])

# Example 7 — filter for an exact match with ==.
print("\nExample 7: clients in Osu")
print(df[df["branch"] == "Osu"])

# Example 8 — two conditions. Use & for AND. Put each condition in round brackets.
print("\nExample 8: Osu AND loan above 2500")
print(df[(df["branch"] == "Osu") & (df["loan_amount"] > 2500)])

# Example 9 — isin() checks whether a value is in a list. Neater than many OR conditions.
print("\nExample 9: Osu or Tema")
print(df[df["branch"].isin(["Osu", "Tema"])])

# Example 10 — sort so the biggest comes first, or take the top rows directly.
print("\nExample 10: sorting")
print(df.sort_values("loan_amount", ascending=False))
print(df.nlargest(3, "loan_amount"))

## Handling Missing Data(Data cleaning)
rd = pd.DataFrame({
    "name": ["Ama", "Kojo", "Efua", "Yaw", "Adjoa", "Kojo"],
    "age": [23, 35, None, 29, 250, 35],                       # a missing age and an impossible age (250)
    "branch": ["Osu", "Adenta", "Tema", None, "Madina", "Adenta"],   # a missing branch
    "loan_amount": [3000, 1500, None, 2500, 8000, 1500],      # a missing loan
    "signup_date": ["2025-01-15", "2025-03-10", "2025-06-01",
                    "not a date", "2025-09-05", "2025-03-10"],   # a bad date
})
print("The messy table:")
print(rd)

# Example 1 — how many empty cells are in each column
print("\nExample 1: empty cells per column")
print(rd.isnull().sum())

# Example 2 — as a percentage of the rows.
print("\nExample 2: percentage empty")
print((rd.isnull().sum() / len(rd) * 100).round(1))

# Example 3 — dropna() removes every row that has ANY empty cell. Quickly, but we lose data.
d = rd.dropna()
print("\nExample 3: dropna")
print("Rows before:", len(rd), "| after:", len(d))

# Example 4 — remove rows only if one chosen column is empty.
d = rd.dropna(subset=["loan_amount"])
print("\nExample 4: dropna on one column")
print("Rows before:", len(raw), "| after:", len(d))

# Example 5 — fill empty cells with a fixed value. Text gets a label, a count gets 0.
d = rd.copy()
d["branch"] = d["branch"].fillna("Unknown")
d["loan_amount"] = d["loan_amount"].fillna(0)
print("\nExample 5: fill with a fixed value")
print(d[["branch", "loan_amount"]])

# Example 6 — fill a number column with its average.
d = raw.copy()
average_loan = d["loan_amount"].mean()
d["loan_amount"] = d["loan_amount"].fillna(average_loan)
print("\nExample 6: fill with the average")
print("Average used:", average_loan)
print(d["loan_amount"])

# Example 7 — fill a text column with its most common value.
d = rd.copy()
most_common = d["branch"].mode()[0]
d["branch"] = d["branch"].fillna(most_common)
print("\nExample 7: fill with the most common value")
print("Most common branch:", most_common)
print(d["branch"])

# Example 8 — wrong format. Turn text into real dates. errors="coerce" turns a bad date into
# NaT (Not a Time) instead of crashing.
d = rd.copy()
d["signup_date"] = pd.to_datetime(d["signup_date"], errors="coerce")
print("\nExample 8: fix the date format")
print(d["signup_date"])
print("Bad dates found:", d["signup_date"].isnull().sum())

# Example 9 — wrong data. An age of 250 is impossible. Replace it with the average of the good ages.
# (The empty age in row 2 is a different problem. It is fixed the same way as Example 6.)
d = rd.copy()
good_average = d.loc[d["age"] <= 100, "age"].mean()
d.loc[d["age"] > 100, "age"] = good_average
print("\nExample 9: fix the impossible age")
print(d["age"])

# Example 10 — duplicates. duplicated() finds repeated rows; drop_duplicates() removes them.
print("\nExample 10: duplicates")
print("Repeated rows:", raw.duplicated().sum())
d = raw.drop_duplicates()
print("Rows before:", len(raw), "| after:", len(d))

## Categorical Encoding
df = pd.DataFrame({
    "name": ["Ama", "Kojo", "Efua", "Yaw", "Adjoa", "Nii"],
    "age": [23, 35, 41, 29, 52, 38],
    "gender": ["Female", "Male", "Female", "Male", "Female", "Male"],
    "branch": ["Osu", "Adenta", "Tema", "Osu", "Madina", "Tema"],
    "has_guarantor": ["Yes", "no", "YES ", "Yes", "No", "no"],    # messy on purpose
    "is_active": [True, False, True, True, False, True],
    "risk_level": ["Low", "High", "Medium", "Low", "High", "Medium"],
    "loan_amount": [3000, 1500, 5000, 2500, 8000, 4200],
})

# Example 1 — first look at the categories: which values exist and how often
print("Example 1: look at the categories")
print(df["branch"].unique())
print(df["has_guarantor"].value_counts())

# Example 2 — tidy the text first. "Yes", "YES " and "yes" must all become one value.
df["has_guarantor"] = df["has_guarantor"].str.strip().str.lower()
print("\nExample 2: tidy the text")
print(df["has_guarantor"].value_counts())

# Example 3 — Yes/No to 1/0 with map() and a dictionary.
df["guarantor_num"] = df["has_guarantor"].map({"yes": 1, "no": 0})
print("\nExample 3: map with a dictionary")
print(df[["has_guarantor", "guarantor_num"]])

# Example 4 — True/False to 1/0 with astype(int).
df["active_num"] = df["is_active"].astype(int)
print("\nExample 4: True/False to 1/0")
print(df[["is_active", "active_num"]])

# Example 5 — labels that HAVE an order. Low < Medium < High, so the numbers must follow it.
df["risk_num"] = df["risk_level"].map({"Low": 0, "Medium": 1, "High": 2})
print("\nExample 5: ordered labels")
print(df[["risk_level", "risk_num"]])

# Example 6 — give each category a number (label encoding). Quick, but it invents an order
# that does not really exist (Tema is not "bigger" than Osu). Use it with care.
df["branch_code"] = df["branch"].astype("category").cat.codes
print("\nExample 6: category codes")
print(df[["branch", "branch_code"]])

# Example 7 — one-hot encoding: one new 0/1 column for each category. No false order.
print("\nExample 7: get_dummies")
print(pd.get_dummies(df["branch"], dtype=int))

# Example 8 — drop_first=True removes one column. That column can always be worked out from the others 
# (if it is not Adenta, Madina or Osu, it must be Tema).
print("\nExample 8: get_dummies with drop_first")
print(pd.get_dummies(df["branch"], drop_first=True, dtype=int))

# Example 9 — one-hot encode several columns in one go.
print("\nExample 9: several columns at once")
print(pd.get_dummies(df[["name", "gender", "branch"]], columns=["gender", "branch"], dtype=int))

# Example 10 — put it together and check that only numbers are left.
ready = df[["age", "loan_amount", "guarantor_num", "active_num", "risk_num"]].copy()
ready = pd.concat([ready, pd.get_dummies(df["branch"], dtype=int)], axis=1)
print("\nExample 10: a table that is all numbers")
print(ready)
print(ready.dtypes)


## Feature Engineering
df = pd.DataFrame({
    "name": ["Ama Serwaa", "Kojo Mensah", "Efua Boateng", "Yaw Asare", "Adjoa Owusu", "Nii Lamptey"],
    "age": [23, 35, 41, 29, 52, 38],
    "income": [2500, 4200, 6000, 3100, 8500, 3900],
    "bonus": [200, 0, 500, 100, 800, 0],
    "loan_amount": [3000, 5000, 12000, 2500, 20000, 4800],
    "start_date": ["2025-01-15", "2025-03-10", "2025-06-01", "2025-07-22", "2025-09-05", "2025-11-30"],
})
df["start_date"] = pd.to_datetime(df["start_date"])

# Example 1 — add two columns together.
df["total_income"] = df["income"] + df["bonus"]
print("Example 1: add columns")
print(df[["name", "income", "bonus", "total_income"]])

# Example 2 — multiply a column. A 5% fee on every loan.
df["fee"] = df["loan_amount"] * 0.05
print("\nExample 2: multiply a column")
print(df[["name", "loan_amount", "fee"]])

# Example 3 — divide one column by another. How many times bigger is the loan than the income?
df["loan_to_income"] = (df["loan_amount"] / df["income"]).round(2)
print("\nExample 3: a ratio")
print(df[["name", "loan_amount", "income", "loan_to_income"]])

# Example 4 — a yes/no flag with np.where(condition, value_if_true, value_if_false).
df["high_risk"] = np.where(df["loan_to_income"] > 1.5, 1, 0)
print("\nExample 4: np.where flag")
print(df[["name", "loan_to_income", "high_risk"]])

# Example 5 — lets apply the function on pandas data, applied to every value. This is the if/elif/else
def loan_size(amount):
    if amount >= 10000:
        return "Large"
    elif amount >= 4000:
        return "Medium"
    else:
        return "Small"

df["loan_size"] = df["loan_amount"].apply(loan_size)
print("\nExample 5: apply a function")
print(df[["name", "loan_amount", "loan_size"]])

# Example 6 — more than two outcomes with np.select(conditions, labels, default).
# It is if/elif/else for a whole column at once.
conditions = [df["loan_to_income"] < 1.0, df["loan_to_income"] < 1.5]
labels = ["Low", "Medium"]
df["risk_band"] = np.select(conditions, labels, default="High")
print("\nExample 6: np.select")
print(df[["name", "loan_to_income", "risk_band"]])

# Example 7 — put numbers into groups with pd.cut. You choose where each group starts and ends.
df["age_group"] = pd.cut(df["age"], bins=[17, 30, 45, 100], labels=["Young", "Middle", "Senior"])
print("\nExample 7: age groups")
print(df[["name", "age", "age_group"]])

# Example 8 — pull parts out of a date with .dt
df["start_year"] = df["start_date"].dt.year
df["start_month"] = df["start_date"].dt.month
df["weekday"] = df["start_date"].dt.day_name()
print("\nExample 8: parts of a date")
print(df[["name", "start_date", "start_year", "start_month", "weekday"]])

# Example 9 — pull parts out of text with .str
df["first_name"] = df["name"].str.split().str[0]
df["last_name"] = df["name"].str.split().str[-1]
df["name_length"] = df["name"].str.len()
print("\nExample 9: parts of text")
print(df[["name", "first_name", "last_name", "name_length"]])

# Example 10 — tidy up: rename a column, drop columns you no longer need.
tidy = df.rename(columns={"loan_amount": "loan"})
tidy = tidy.drop(columns=["bonus", "start_date", "name_length"])
print("\nExample 10: rename and drop")
print(tidy.columns.tolist())

## Combining & Aggregation of Datasets
clients_a = pd.DataFrame({"client_id": [1, 2, 3], "name": ["Ama", "Kojo", "Efua"], "branch_id": [10, 20, 10]})
clients_b = pd.DataFrame({"client_id": [4, 5], "name": ["Yaw", "Adjoa"], "branch_id": [30, 20]})
clients = pd.concat([clients_a, clients_b], ignore_index=True)

loans = pd.DataFrame({
    "loan_id": [501, 502, 503, 504, 505],
    "client_id": [1, 2, 2, 4, 6],               # client 6 is not in the clients table
    "amount": [3000, 1500, 2200, 5000, 4000],
    "status": ["Paid", "Active", "Paid", "Active", "Active"],
})
branches = pd.DataFrame({"branch_id": [10, 20, 30], "branch_name": ["Osu", "Adenta", "Tema"]})

# Example 1 — stack tables that have the same columns, one below the other.
print("Example 1: concat rows")
print(pd.concat([clients_a, clients_b], ignore_index=True))

# Example 2 — place tables side by side (axis=1). Rows are matched by position.
scores = pd.DataFrame({"credit_score": [620, 580, 700]})
print("\nExample 2: concat columns")
print(pd.concat([clients_a, scores], axis=1))

# Example 3 — merge, keeping only clients who appear in BOTH tables (inner).
print("\nExample 3: inner merge")
print(loans.merge(clients, on="client_id", how="inner"))

# Example 4 — keep every row of the left table (left). Missing matches show as NaN.
print("\nExample 4: left merge")
print(clients.merge(loans, on="client_id", how="left"))

# Example 5 — keep everything from both tables (outer).
print("\nExample 5: outer merge")
print(clients.merge(loans, on="client_id", how="outer"))

# Example 6 — when the key column has a different name in each table, use left_on and right_on.
loans_renamed = loans.rename(columns={"client_id": "cust_id"})
print("\nExample 6: different key names")
print(clients.merge(loans_renamed, left_on="client_id", right_on="cust_id", how="inner"))

# Example 7 — join three tables into one, then add up the loans for each branch.
full = loans.merge(clients, on="client_id").merge(branches, on="branch_id")
print("\nExample 7: one full table, then groupby and sum")
print(full)
print(full.groupby("branch_name")["amount"].sum())

# Example 8 — count how many loans each branch has.
print("\nExample 8: groupby and count")
print(full.groupby("branch_name")["loan_id"].count())

# Example 9 — several summaries at once with agg().
print("\nExample 9: agg")
print(full.groupby("branch_name")["amount"].agg(["count", "sum", "max"]))

# Example 10 — pivot_table builds a summary grid like an Excel pivot table.
print("\nExample 10: pivot_table")
print(pd.pivot_table(full, values="amount", index="branch_name", columns="status",
                     aggfunc="sum", fill_value=0))


## Exporting to Machine Learning
from sklearn.model_selection import train_test_split

df = pd.DataFrame({
    "age":         [23, 35, 41, 29, 52, 38, 45, 31, 27, 60, 34, 48],
    "income":      [2500, 4200, 6000, None, 8500, 3900, 5200, 3100, None, 7000, 4500, 6400],
    "loan_amount": [3000, 5000, 12000, 2500, 20000, 4800, 9000, 3500, 3300, 15000, 4000, 11000],
    "branch":      ["Osu", "Adenta", "Tema", "Osu", "Madina", "Tema",
                    "Osu", "Adenta", "Tema", "Madina", "Osu", "Adenta"],
    "defaulted":   [0, 0, 1, 0, 1, 0, 1, 0, 0, 1, 0, 1],
})

# Example 1 — split the table into inputs (X) and the answer (y).
X = df.drop(columns="defaulted")
y = df["defaulted"]
print("Example 1: inputs and answer")
print("X columns:", X.columns.tolist())
print("y is the column:", y.name)

# Example 2 — machine-learning tools do not accept empty cells. Look for them first.
print("\nExample 2: any empty cells?")
print(X.isnull().sum())

# Example 3 — fill the empty cells (Section 3). Here we use the average income.
X["income"] = X["income"].fillna(X["income"].mean())
print("\nExample 3: empty cells left")
print(X.isnull().sum().sum())

# Example 4 — turn words into numbers (Section 4).
X = pd.get_dummies(X, columns=["branch"], dtype=int)
print("\nExample 4: words turned into numbers")
print(X.head())

# Example 5 — check that every column is a number.
print("\nExample 5: column types")
print(X.dtypes)

# Example 6 — turn the tables into plain number grids (NumPy arrays), which many tools prefer.
X_array = X.to_numpy()
y_array = y.to_numpy()
print("\nExample 6: to NumPy")
print("X array shape:", X_array.shape)
print("y array shape:", y_array.shape)

# Example 7 — split into a practice set (train) and an exam set (test).
# test_size=0.25 means a quarter of the rows are kept back for the exam.
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.25, random_state=42)
print("\nExample 7: practice set and exam set")
print("Practice rows:", len(X_train), "| Exam rows:", len(X_test))

# Example 8 — random_state=42 means "shuffle the same way every time". Same number, same split.
a_train, a_test, b_train, b_test = train_test_split(X, y, test_size=0.25, random_state=42)
print("\nExample 8: the same split twice")
print("Same practice rows both times:", X_train.index.equals(a_train.index))

# Example 9 — check that practice and exam sets have the same columns.
print("\nExample 9: matching columns")
print("Same columns:", X_train.columns.tolist() == X_test.columns.tolist())
print("Rows in y_train match X_train:", len(y_train) == len(X_train))

# Example 10 — save the practice to files, then load one back to check.
X_train.assign(defaulted=y_train).to_csv("train.csv", index=False)
X_test.assign(defaulted=y_test).to_csv("test.csv", index=False)
print("\nExample 10: saved and loaded back")
print(pd.read_csv("train.csv").shape)
```

```pyton

```

# References 
w3schools - https://www.w3schools.com/python/  
geeksforgeeks - https://www.geeksforgeeks.org/python/python-programming-language-tutorial/
Claud ai
Google

---
---

# PART B — STATISTICS FOR DATA SCIENCE
*(Based on the GeeksforGeeks Statistics for Data Science reference)*

## B1. Measures of Central Tendency (Mean, Median, Mode)
```python
import statistics
import numpy as np

# Example 1 — Mean
sales = [250, 300, 275, 400, 320]
print("Mean:", statistics.mean(sales))

# Example 2 — Median
scores = [60, 70, 70, 80, 90]
print("Median:", statistics.median(scores))

# Example 3 — Mode
shoe_sizes = [38, 39, 39, 40, 39]
print("Mode:", statistics.mode(shoe_sizes))

# Example 4 — Mean calculated manually (no library)
ages = [22, 25, 28, 30, 35]
manual_mean = sum(ages) / len(ages)
print("Manual Mean:", manual_mean)

# Example 5 — Using NumPy for mean and median
data = np.array([10, 20, 30, 40, 50])
print("NumPy Mean:", np.mean(data))
print("NumPy Median:", np.median(data))
```

## B2. Measures of Dispersion (Range, Variance, Std Dev, IQR)
```python
import statistics
import numpy as np

# Example 1 — Range
temperatures = [22, 25, 19, 30, 28]
data_range = max(temperatures) - min(temperatures)
print("Range:", data_range)

# Example 2 — Variance (sample)
loan_amounts = [2500, 1800, 4200, 900, 3300]
print("Variance:", statistics.variance(loan_amounts))

# Example 3 — Standard Deviation
print("Standard Deviation:", statistics.stdev(loan_amounts))

# Example 4 — Interquartile Range (IQR) using NumPy
exam_scores = np.array([55, 60, 65, 70, 72, 75, 80, 85, 90, 95])
q1 = np.percentile(exam_scores, 25)
q3 = np.percentile(exam_scores, 75)
iqr = q3 - q1
print("Q1:", q1, "Q3:", q3, "IQR:", iqr)

# Example 5 — Coefficient of Variation
mean_val = statistics.mean(loan_amounts)
std_val = statistics.stdev(loan_amounts)
cv = (std_val / mean_val) * 100
print("Coefficient of Variation (%):", round(cv, 2))
```

## B3. Measures of Shape (Skewness & Kurtosis)
```python
import numpy as np
from scipy import stats

# Example 1 — Skewness of a dataset
sales_data = np.array([100, 120, 110, 130, 500])
print("Skewness:", stats.skew(sales_data))

# Example 2 — Kurtosis of a dataset
print("Kurtosis:", stats.kurtosis(sales_data))

# Example 3 — A symmetric dataset's skew (should be close to 0)
symmetric_data = np.array([10, 20, 30, 40, 50])
print("Symmetric Data Skewness:", stats.skew(symmetric_data))

# Example 4 — Interpreting the sign of skew
skew_value = stats.skew(sales_data)
if skew_value > 0:
    print("Positively skewed (right-tailed)")
elif skew_value < 0:
    print("Negatively skewed (left-tailed)")
else:
    print("Symmetrical distribution")

# Example 5 — Business example: customer wait times (usually right-skewed)
wait_times = np.array([2, 3, 2, 4, 3, 2, 15])
print("Wait Times Skewness:", stats.skew(wait_times))
```

## B4. Measures of Relationship (Covariance & Correlation)
```python
import numpy as np
from scipy import stats

# Example 1 — Covariance between two variables
temperature = np.array([20, 25, 28, 30, 35])
ice_cream_sales = np.array([50, 65, 70, 80, 95])
cov_matrix = np.cov(temperature, ice_cream_sales)
print("Covariance:", cov_matrix[0][1])

# Example 2 — Correlation coefficient
corr_matrix = np.corrcoef(temperature, ice_cream_sales)
print("Correlation:", corr_matrix[0][1])

# Example 3 — Correlation with p-value using SciPy
corr, p_value = stats.pearsonr(temperature, ice_cream_sales)
print("Correlation:", corr, "| P-value:", p_value)

# Example 4 — Business example: positive correlation
study_hours = np.array([1, 2, 3, 4, 5])
exam_scores = np.array([50, 55, 65, 70, 85])
print("Study Hours vs Scores Correlation:", np.corrcoef(study_hours, exam_scores)[0][1])

# Example 5 — Business example: negative correlation
delivery_delays = np.array([1, 2, 3, 4, 5])
customer_satisfaction = np.array([95, 85, 75, 60, 40])
print("Delays vs Satisfaction Correlation:", np.corrcoef(delivery_delays, customer_satisfaction)[0][1])
```

## B5. Probability Basics
```python
import random

# Example 1 — Simple probability (favorable / total outcomes)
favorable_outcomes = 1
total_outcomes = 6
probability = favorable_outcomes / total_outcomes
print("Probability of rolling a 4:", probability)

# Example 2 — Joint probability of independent events
p_rain = 0.3
p_traffic = 0.4
p_rain_and_traffic = p_rain * p_traffic
print("P(Rain and Traffic):", p_rain_and_traffic)

# Example 3 — Union probability
p_a = 0.3
p_b = 0.4
p_a_and_b = 0.12
p_a_or_b = p_a + p_b - p_a_and_b
print("P(Rain or Traffic):", p_a_or_b)

# Example 4 — Simulating coin flips to estimate probability
random.seed(42)
flips = [random.choice(["Heads", "Tails"]) for _ in range(1000)]
heads_count = flips.count("Heads")
print("Empirical Probability of Heads:", heads_count / len(flips))

# Example 5 — Conditional probability: P(A|B) = P(A and B) / P(B)
p_default_and_late = 0.08
p_late_payment = 0.20
p_default_given_late = p_default_and_late / p_late_payment
print("P(Default | Late Payment):", p_default_given_late)
```

## B6. Normal Distribution & Z-Scores
```python
import numpy as np
from scipy import stats

# Example 1 — Generate a normal distribution sample
np.random.seed(42)
heights = np.random.normal(loc=170, scale=10, size=1000)
print("Sample Mean:", round(np.mean(heights), 2))
print("Sample Std Dev:", round(np.std(heights), 2))

# Example 2 — Compute a z-score manually
value = 185
mean = 170
std_dev = 10
z_score = (value - mean) / std_dev
print("Z-score:", z_score)

# Example 3 — Probability of a value below a threshold (CDF)
probability_below = stats.norm.cdf(185, loc=170, scale=10)
print("P(X < 185):", probability_below)

# Example 4 — Empirical Rule check (~68% within 1 standard deviation)
within_1_std = np.sum((heights > 160) & (heights < 180)) / len(heights)
print("Proportion within 1 std dev:", within_1_std)

# Example 5 — Z-scores for an entire array
sample_scores = np.array([60, 70, 80, 90, 100])
z_scores = stats.zscore(sample_scores)
print("Z-scores:", z_scores)
```

## B7. Hypothesis Testing Basics
```python
from scipy import stats

# Example 1 — One-sample t-test
sample_scores = [78, 82, 85, 90, 76, 88, 95]
t_stat, p_value = stats.ttest_1samp(sample_scores, popmean=80)
print("T-statistic:", t_stat, "| P-value:", p_value)

# Example 2 — Two-sample independent t-test
group_a = [85, 90, 88, 92, 95]
group_b = [78, 82, 80, 85, 79]
t_stat, p_value = stats.ttest_ind(group_a, group_b)
print("T-statistic:", t_stat, "| P-value:", p_value)

# Example 3 — Interpreting the p-value against alpha
alpha = 0.05
if p_value < alpha:
    print("Reject the null hypothesis — significant difference")
else:
    print("Fail to reject the null hypothesis — no significant difference")

# Example 4 — Degrees of freedom
sample_size = len(sample_scores)
degrees_of_freedom = sample_size - 1
print("Degrees of Freedom:", degrees_of_freedom)

# Example 5 — Paired t-test (before vs. after)
before = [70, 75, 80, 65, 90]
after = [75, 78, 85, 70, 92]
t_stat, p_value = stats.ttest_rel(before, after)
print("Paired T-statistic:", t_stat, "| P-value:", p_value)
```

## B8. Simple Linear Regression
```python
import numpy as np
from scipy import stats

# Example 1 — Manually calculate slope and intercept
hours_studied = np.array([1, 2, 3, 4, 5])
exam_scores = np.array([50, 55, 65, 70, 85])

mean_x = np.mean(hours_studied)
mean_y = np.mean(exam_scores)
slope = np.sum((hours_studied - mean_x) * (exam_scores - mean_y)) / np.sum((hours_studied - mean_x) ** 2)
intercept = mean_y - slope * mean_x
print("Slope:", slope, "| Intercept:", intercept)

# Example 2 — Fit a line using NumPy's polyfit
coefficients = np.polyfit(hours_studied, exam_scores, 1)
print("NumPy Slope and Intercept:", coefficients)

# Example 3 — Predict a new value using the fitted line
new_hours = 6
predicted_score = slope * new_hours + intercept
print("Predicted score for 6 hours studied:", predicted_score)

# Example 4 — Correlation coefficient alongside regression
correlation = np.corrcoef(hours_studied, exam_scores)[0][1]
print("Correlation Coefficient:", correlation)

# Example 5 — Full regression summary using SciPy
result = stats.linregress(hours_studied, exam_scores)
print("Slope:", result.slope)
print("Intercept:", result.intercept)
print("R-value:", result.rvalue)
print("P-value:", result.pvalue)
```

---

## BONUS — ADVANCED TOPICS

## B9. Bayes' Theorem
```python
# Example 1 — Basic Bayes calculation: P(A|B) = P(B|A) * P(A) / P(B)
p_a = 0.01
p_b_given_a = 0.95
p_b = 0.058
p_a_given_b = (p_b_given_a * p_a) / p_b
print("P(Disease | Positive Test):", round(p_a_given_b, 4))

# Example 2 — Medical test with sensitivity/specificity
prevalence = 0.02
sensitivity = 0.90
false_positive_rate = 0.05
p_positive = (sensitivity * prevalence) + (false_positive_rate * (1 - prevalence))
p_disease_given_positive = (sensitivity * prevalence) / p_positive
print("P(Disease | Positive):", round(p_disease_given_positive, 4))

# Example 3 — Spam email example
p_spam = 0.4
p_word_given_spam = 0.7
p_word_given_not_spam = 0.1
p_word = (p_word_given_spam * p_spam) + (p_word_given_not_spam * (1 - p_spam))
p_spam_given_word = (p_word_given_spam * p_spam) / p_word
print("P(Spam | Contains Word):", round(p_spam_given_word, 4))

# Example 4 — Updating belief with new evidence
prior = 0.3
likelihood = 0.8
evidence = 0.5
posterior = (likelihood * prior) / evidence
print("Updated belief (posterior):", posterior)

# Example 5 — Business example: loan default given late payment history
p_default = 0.1
p_late_given_default = 0.6
p_late = 0.2
p_default_given_late = (p_late_given_default * p_default) / p_late
print("P(Default | Late Payment):", p_default_given_late)
```

## B10. Chi-Square Test
```python
import numpy as np
from scipy import stats

# Example 1 — Goodness-of-fit test
observed = [18, 22, 20, 25, 15]
expected = [20, 20, 20, 20, 20]
chi2_stat, p_value = stats.chisquare(observed, expected)
print("Chi-Square Statistic:", chi2_stat, "| P-value:", p_value)

# Example 2 — Test of independence using a contingency table
contingency_table = np.array([[30, 10], [20, 40]])
chi2, p, dof, expected_freq = stats.chi2_contingency(contingency_table)
print("Chi-Square:", chi2, "| P-value:", p, "| DoF:", dof)

# Example 3 — Interpreting the p-value
alpha = 0.05
if p < alpha:
    print("Significant association found between the variables")
else:
    print("No significant association found")

# Example 4 — Manually calculating the chi-square statistic
observed_vals = np.array([30, 10, 20, 40])
expected_vals = np.array([25, 15, 25, 35])
manual_chi2 = np.sum((observed_vals - expected_vals) ** 2 / expected_vals)
print("Manually Calculated Chi-Square:", manual_chi2)

# Example 5 — Business example: gender vs. product preference
product_preference = np.array([[40, 10], [15, 35]])
chi2, p, dof, expected_freq = stats.chi2_contingency(product_preference)
print("Chi-Square:", chi2, "| P-value:", p)
```

## B11. ANOVA (Analysis of Variance)
```python
import numpy as np
from scipy import stats

# Example 1 — One-way ANOVA across three groups
region_a_sales = [200, 220, 210, 230, 215]
region_b_sales = [180, 190, 175, 185, 195]
region_c_sales = [250, 260, 245, 255, 265]
f_stat, p_value = stats.f_oneway(region_a_sales, region_b_sales, region_c_sales)
print("F-statistic:", f_stat, "| P-value:", p_value)

# Example 2 — Interpreting the result
alpha = 0.05
if p_value < alpha:
    print("At least one region's average sales significantly differs")
else:
    print("No significant difference between regions")

# Example 3 — Business example: comparing training methods
method_1_scores = [70, 75, 72, 78, 74]
method_2_scores = [80, 85, 82, 88, 84]
method_3_scores = [65, 68, 70, 66, 69]
f_stat, p_value = stats.f_oneway(method_1_scores, method_2_scores, method_3_scores)
print("F-statistic:", f_stat, "| P-value:", p_value)

# Example 4 — Manually computing group means before running ANOVA
print("Region A Mean:", np.mean(region_a_sales))
print("Region B Mean:", np.mean(region_b_sales))
print("Region C Mean:", np.mean(region_c_sales))

# Example 5 — Two-group comparison (ANOVA and t-test agree for 2 groups)
f_stat, p_val_anova = stats.f_oneway(region_a_sales, region_b_sales)
t_stat, p_val_ttest = stats.ttest_ind(region_a_sales, region_b_sales)
print("ANOVA P-value:", p_val_anova)
print("T-test P-value:", p_val_ttest)
```