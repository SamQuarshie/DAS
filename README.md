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

```
# References 
w3schools - https://www.w3schools.com/python/  
geeksforgeeks - https://www.geeksforgeeks.org/python/python-programming-language-tutorial/


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