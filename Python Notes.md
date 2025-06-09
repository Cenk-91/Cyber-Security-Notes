
1. It was initially designed by Guido van Rossum in 1991 and developed by Python Software Foundation.

2. It is written in the **C** programming language.

3. The name was inspired by the British comedy group Monty Python.

4. **`#`** This is a comment. It will not be executed.

5. It runs commands line by line. Each line contains a single instruction.

6. The **`print()`** function is used to display text or values on the screen.
```python
print("Hello, World!")
print(123)
```

7. A **string** is text in Python. It must be inside quotes: "hello" or 'hello'.

8. The **`type()`** function returns the data type (class) of the given value.
```python
print(type("cenk"))      # <class 'str'>
print(type(42))          # <class 'int'>
```

9. An **int (integer)** represents whole numbers (positive, negative, or zero) in Python.

10. A **float** represents decimal (floating point) numbers in Python.
```python
boy = 1.75
print(type(boy))  # <class 'float'>
```

11. A **bool** represents logical values: **True** or **False**. (Boolean data type)
```python
hava_gunesli = True # Capital Letter
sigara_icti_mi = False # Capital Letter
print(type(hava_gunesli))   # <class 'bool'>
```

12. A **list** is an ordered collection of items. Lists are **mutable** (you can change their content after creation).
```python
my_list = [1, 2, 3]
my_list[0] = 10
print(my_list)  # Output: [10, 2, 3]
```

13. A **tuple** is an ordered collection of items like a list, but it is **immutable** (you cannot change its content).
```python
my_tuple = (1, 2, 3)
print(my_tuple[1])  # Output: 2
```

14. **`len()`** fuction returns the number of items in a sequence or collection. It works with: strings, lists, tuples, dictionaries, etc.
```python
len("Cenk")             # 4
len([1, 2, 3])          # 3
len((True, False))      # 2
len({"a": 1, "b": 2})   # 2
```

15. **`dict`** A dictionary stores **key-value pairs**. **Keys** must be **unique**. **Values** can be **any type**.
```python
person = {
    "name": "Cenk",
    "age": 33,
    "city": "Ankara"
}
print(person["name"])      # Output: Cenk
person.keys()      # All the keys
person.values()    # All the values
person.items()     # All the keys and values
```

16. A **variable** is used to store data. Python doesn’t require you to declare the type.
- name = "Cenk" stores a string.

16. **`input("message")`** displays a prompt and waits for user input. The result is always a string. Use `int()`, `float()` etc. to convert if needed.
```python
name = input("What's your name? ")
print("Hey", name)
```

18. **`int()`** function converts a value to an integer type (whole number).
```python
num = int("42")    # string → int
print(num + 1)     # Output: 43
```

19. **`str()`** function converts a value to a string type.
```python
age = 33
message = "Age: " + str(age)
print(message)     # Output: Age: 33
```

20. Converting input to integer using **`int()`**
- Ask for two numbers from the user and add them
```python
num1 = int(input("Enter the first number: "))
num2 = int(input("Enter the second number: "))
total = num1 + num2
print("The total is:", total)
```

21. **`input()`** always returns a string, even if the user types a number.
- **You must convert it using `int()` or `float()` before doing math operations.**

21. **if** statement – basic conditional logic
- Ask the user's age and respond based on the input
```python
age = int(input("Enter your age: "))
if age >= 18:
    print("You are an adult!")
else:
    print("You are not an adult.")
```
- if is used to check a condition.
- If the condition is True, the block under if runs.
- If the condition is False, the else block runs.

23. **`None`** Represents the absence of a value. The data type is **NoneType**.
```python
x = None
print(x)            # Output: None
print(type(x))      # <class 'NoneType'>
```

24. Type casting is the process of converting one data type into another (e.g. string to int).
```python
int("123")      # string → int
float("3.14")   # string → float
str(42)         # int → string
bool(0)         # 0 → False, others → True
```

25. The **`bool()`** function converts a value to a boolean (True or False).
- Common rules: 0, 0.0, "", [], (), {}, None → False.
- Everything else → True.
```python
print(bool(0))        # Output: False
print(bool("Hi"))     # Output: True
print(bool([]))       # Output: False
print(bool([1, 2]))   # Output: True
```

26. The **pass** statement is a placeholder that does nothing.
- It's useful when a statement is syntactically required but no action is needed yet.
```python
if True:
    pass  # Do nothing for now
else:
    print("This won't run")
```

27. **`elif`** Keyword – Multiple Conditions
```python
age = int(input("Enter your age: "))
if age < 13:
    print("Child")
elif age < 20:
    print("Teenager")
else:
    print("Adult")
```
- `elif` stands for **"else if"**. It lets you check multiple conditions in sequence.

28. **`in`** Operator – Membership Test
```python
fruits = ["apple", "banana", "cherry"]
if "banana" in fruits:
	print("Yes, banana is in the list!")

```
- `in` checks if a value exists inside a list, string, or other iterable.

 29. **`+`** (Addition Operator)
- Used to add two numbers or concatenate strings.
- **Numbers**
`a = 5 + 3      # 8`
- **Strings**
`greeting = "Hello, " + "Cenk!"  # "Hello, Cenk!"`

 30. **`-`** (Subtraction Operator)
- Used to subtract one number from another.
`x = 10 - 4     # 6`
- Note: These operators work only on compatible types (e.g., you can't subtract strings).

31. **`*`** (Multiplication Operator)
- Used to multiply two numbers or repeat a string.
- **Numbers**
`area = 4 * 5      # 20`
- **Strings**
`echo = "Hi! " * 3    # "Hi! Hi! Hi! "`

32. **`/`** (Division Operator)
- Used to divide one number by another.
- Returns a **float** result even if the division is exact.
`result = 10 / 2     # 5.0`
- Note: If you want **integer division**, use `//` (floor division).


