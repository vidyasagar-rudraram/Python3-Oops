**Python Dictionaries** assesses understanding of the ability to define and use dictionary (mapping) types in a Python 3 program, including setting values, using default values, and iterations.

1. **Defining a Dictionary**

- A dictionary in Python is a collection of key-value pairs, where each key is unique.
- You can define a dictionary using curly braces {} and colon : to separate keys and values.

```python
# dictionary of student names and their corresponding ages
student_age = {'Alice': 20, 'Bob': 22, 'Charlie': 21}
```

2. **Setting Values in a Dictionary**

- You can set values in a dictionary using assignment syntax or the update() method.

```python
# Set value for a key using assignment syntax
student_age['David'] = 23

# Update dictionary with multiple key-value pairs using update() method
student_age.update({'Emily': 24, 'Frank': 25})
```

3. **Using Default Values**

- You can use the get() method or the defaultdict class from the collections module to handle missing keys gracefully.

```python
# Using get() method to provide a default value if key is missing
age_of_john = student_age.get('John', 'N/A')

# Using defaultdict to set a default value factory
from collections import defaultdict
student_scores = defaultdict(int)  # Default value for missing keys is 0 (int)
student_scores['Alice'] += 1
```

4. **Iterations**

- You can iterate over the keys, values, or key-value pairs of a dictionary using a loop or using dictionary methods like keys(), values(), or items().

```python
# Iterate over keys
for name in student_age:
    print(name)

# Iterate over values
for age in student_age.values():
    print(age)

# Iterate over key-value pairs
for name, age in student_age.items():
    print(f"{name} is {age} years old")
```

---

**Python File I/O** evaluates knowledge of external file interaction using Python 3, including reading, writing, opening, and closing files and sockets.

1. **Reading from a File**

- You can read from a file using the open() function in combination with the read() or readlines() method.

```python
# Open file in read mode
with open('example.txt', 'r') as file:
    # Read the entire content of the file
    content = file.read()
    print(content)

    # Alternatively, read line by line
    # for line in file:
    #     print(line)
```

2. **Writing to a File**

- You can write to a file using the open() function in combination with the write() method.

```python
# Open file in write mode
with open('example.txt', 'w') as file:
    # Write content to the file
    file.write('Hello, World!\n')
    file.write('This is a sample text.')
```

3. **Appending to a File**

- You can append to a file using the open() function in combination with the write() method in append mode.

```python
# Open file in append mode
with open('example.txt', 'a') as file:
    # Append content to the file
    file.write('\nAppending additional content.')
```

4. **Opening and Closing Files**

- You can open and close files using the open() function and the close() method, respectively. However, using a context manager (with statement) is recommended as it automatically closes the file when the block is exited.

```python
# Open file in read mode
file = open('example.txt', 'r')
# Perform file operations...
file.close()  # Close the file when done

# Alternatively, use a context manager
with open('example.txt', 'r') as file:
    # Perform file operations...
```

---

**Python Functions** tests Python 3 function definition syntax, parameter passing, and returning results. Lambda expressions are also covered.

1. **Function Definition Syntax**

- You can define a function using the def keyword followed by the function name, parameters (if any), and a colon. The function body is indented.

```python
# Function definition
def greet(name):
    print(f"Hello, {name}!")

# Function call
greet('Alice')

```

2. **Parameter Passing**

- Parameters can be passed to functions in Python by position (positional arguments) or by name (keyword arguments).

```python
# Function definition with multiple parameters
def add(a, b):
    return a + b

# Positional arguments
print(add(3, 5))  # Output: 8

# Keyword arguments
print(add(b=4, a=2))  # Output: 6
```

3. **Returning Results**

- Functions can return results using the return statement. If no return statement is specified, the function returns None by default.

```python
# Function definition with return statement
def multiply(a, b):
    return a * b

# Function call with result assignment
result = multiply(4, 6)
print(result)  # Output: 24
```

4. **Lambda Expressions**

- Lambda expressions are anonymous functions defined using the lambda keyword. They are useful for creating small, inline functions.

```python
# Lambda expression to square a number
square = lambda x: x**2
print(square(5))  # Output: 25

```

---

**Python Lists and Tuples** demonstrates knowledge of the Python 3 list and tuple sequence aggregate types, including accessing values, simple functions, and common usage including sorting and searching.

1. **Accessing Values:**

   - You can access individual elements of a list or tuple using indexing. Indexing starts from 0 for the first element and -1 for the last element.

   Example:

   ```python
   # List
   my_list = [1, 2, 3, 4, 5]
   print(my_list[0])  # Output: 1
   print(my_list[-1])  # Output: 5

   # Tuple
   my_tuple = (10, 20, 30, 40, 50)
   print(my_tuple[2])  # Output: 30
   print(my_tuple[-2])  # Output: 40
   ```

2. **Simple Functions:**

   - Lists and tuples support various built-in functions like `len()`, `min()`, and `max()`.

   Example:

   ```python
   # List
   my_list = [10, 20, 30, 40, 50]
   print(len(my_list))  # Output: 5
   print(min(my_list))  # Output: 10
   print(max(my_list))  # Output: 50

   # Tuple
   my_tuple = (5, 10, 15, 20)
   print(len(my_tuple))  # Output: 4
   print(min(my_tuple))  # Output: 5
   print(max(my_tuple))  # Output: 20
   ```

3. **Common Usage - Sorting:**

   - You can sort lists using the `sort()` method or the `sorted()` function. Tuples cannot be modified, so you need to use `sorted()` to sort them.

   Example:

   ```python
   # List sorting
   my_list = [5, 3, 7, 1, 4]
   my_list.sort()  # Sorts the list in place
   print(my_list)  # Output: [1, 3, 4, 5, 7]

   # Tuple sorting
   my_tuple = (10, 30, 20, 50, 40)
   sorted_tuple = sorted(my_tuple)  # Returns a new sorted list
   print(sorted_tuple)  # Output: [10, 20, 30, 40, 50]
   ```

4. **Common Usage - Searching:**

   - You can use the `index()` method to find the index of a specific element in a list or tuple.

   Example:

   ```python
   # List searching
   my_list = ['apple', 'banana', 'cherry', 'apple']
   print(my_list.index('banana'))  # Output: 1

   # Tuple searching
   my_tuple = (10, 20, 30, 40, 50)
   print(my_tuple.index(30))  # Output: 2
   ```

---

**Python Modules and Imports** tests understanding of how to use external modules in Python 3, how modules are defined, and how to use modules to enforce data hiding practices.

1. **Using External Modules:**

   - You can use external modules by importing them into your Python script using the `import` statement.

   Example:

   ```python
   # Importing the math module
   import math

   # Using functions from the math module
   print(math.sqrt(16))  # Output: 4.0
   print(math.pi)  # Output: 3.141592653589793
   ```

2. **Defining Modules:**

   - You can create your own modules by saving Python code in a `.py` file and then importing that file as a module.

   Example:

   ```python
   # File: mymodule.py
   def greet(name):
       print(f"Hello, {name}!")

   def farewell(name):
       print(f"Goodbye, {name}!")
   ```

   ```python
   # Importing the custom module
   import mymodule

   # Using functions from the custom module
   mymodule.greet('Alice')  # Output: Hello, Alice!
   mymodule.farewell('Bob')  # Output: Goodbye, Bob!
   ```

3. **Using Modules for Data Hiding:**

   - You can use modules to encapsulate data and functions, hiding implementation details from the user.

   Example:

   ```python
   # File: mymodule.py
   _hidden_variable = 'This is a hidden variable'

   def public_function():
       print("This is a public function.")

   def _hidden_function():
       print("This is a hidden function.")
   ```

   ```python
   # Importing and using the custom module
   import mymodule

   print(mymodule._hidden_variable)  # Output: This is a hidden variable
   mymodule.public_function()  # Output: This is a public function.

   # Attempting to access a hidden function
   mymodule._hidden_function()  # Raises an AttributeError
   ```

---

**Python Regular Expression Usage** measures the definition and application of Python 3 regular expressions to locate, extract, and change text in context.

1. **Matching Patterns:**

   - You can use regex to match specific patterns in strings using the `re` module.

   Example:

   ```python
   import re

   # Search for a specific pattern in a string
   text = "The quick brown fox jumps over the lazy dog"
   pattern = r'fox'
   match = re.search(pattern, text)
   if match:
       print("Pattern found")
   ```

2. **Extracting Text:**

   - You can use regex to extract specific substrings from strings.

   Example:

   ```python
   # Extract email addresses from a string
   text = "Contact us at email@example.com or support@example.com"
   pattern = r'[\w\.-]+@[\w\.-]+'
   emails = re.findall(pattern, text)
   print(emails)  # Output: ['email@example.com', 'support@example.com']
   ```

3. **Changing Text:**

   - You can use regex to find and replace text in a string.

   Example:

   ```python
   # Replace all occurrences of a pattern with a new string
   text = "The cat sat on the mat"
   pattern = r'cat'
   new_text = re.sub(pattern, 'dog', text)
   print(new_text)  # Output: "The dog sat on the mat"
   ```

4. **Using Groups:**

   - You can use regex groups to capture specific parts of a matched pattern.

   Example:

   ```python
   # Extract username and domain separately from an email address
   email = "user@example.com"
   pattern = r'(\w+)@(\w+\.\w+)'
   match = re.match(pattern, email)
   if match:
       username = match.group(1)
       domain = match.group(2)
       print("Username:", username)  # Output: "Username: user"
       print("Domain:", domain)  # Output: "Domain: example.com"
   ```

---

**Python Classes** tests knowledge of object-oriented programming using Python 3 and object-oriented features like inheritance and polymorphism as well as subclassing, static methods, and private attributes.

1. **Defining a Class and Creating Objects:**

   - You can define a class in Python using the `class` keyword, and then create objects (instances) of that class using the class name followed by parentheses.

   Example:

   ```python
   class Dog:
       def __init__(self, name):
           self.name = name

       def bark(self):
           return "Woof!"

   # Create objects of the Dog class
   dog1 = Dog("Buddy")
   dog2 = Dog("Max")

   print(dog1.name)  # Output: "Buddy"
   print(dog2.name)  # Output: "Max"
   print(dog1.bark())  # Output: "Woof!"
   ```

2. **Inheritance and Polymorphism:**

   - You can create subclasses that inherit from a parent class, allowing them to reuse code and extend functionality. Polymorphism allows objects of different classes to be treated as objects of a common superclass.

   Example:

   ```python
   class Animal:
       def speak(self):
           pass

   class Dog(Animal):
       def speak(self):
           return "Woof!"

   class Cat(Animal):
       def speak(self):
           return "Meow!"

   # Polymorphism
   animals = [Dog(), Cat()]
   for animal in animals:
       print(animal.speak())  # Output: "Woof!" (for Dog) and "Meow!" (for Cat)
   ```

3. **Subclassing and Overriding Methods:**

   - You can subclass built-in Python classes and override their methods to customize their behavior.

   Example:

   ```python
   class MyInt(int):
       def __add__(self, other):
           return self * other  # Override addition to perform multiplication

   num1 = MyInt(5)
   num2 = MyInt(3)
   print(num1 + num2)  # Output: 15 (instead of 8)
   ```

4. **Static Methods and Private Attributes:**

   - You can define static methods using the `@staticmethod` decorator, and create private attributes by prefixing them with double underscores `__`.

   Example:

   ```python
   class Calculator:
       @staticmethod
       def add(a, b):
           return a + b

   class BankAccount:
       def __init__(self, balance):
           self.__balance = balance  # Private attribute

       def deposit(self, amount):
           self.__balance += amount

       def withdraw(self, amount):
           self.__balance -= amount

       def get_balance(self):
           return self.__balance

   account = BankAccount(1000)
   account.withdraw(500)
   print(account.get_balance())  # Output: 500
   ```

---

**Python Control Flow** determines knowledge of the Python flow control statements (i.e., while, if, for, break, range, pass, etc.) and what instructions are executed or evaluated depending on the value of the contextual data or the resulting expressions.

1. **if Statement:**

   - The `if` statement is used to execute a block of code if a condition is true.

   Example:

   ```python
   x = 10
   if x > 5:
       print("x is greater than 5")
   ```

2. **if-else Statement:**

   - The `if-else` statement is used to execute one block of code if the condition is true, and another block of code if the condition is false.

   Example:

   ```python
   x = 10
   if x > 5:
       print("x is greater than 5")
   else:
       print("x is not greater than 5")
   ```

3. **if-elif-else Statement:**

   - The `if-elif-else` statement is used to check multiple conditions.

   Example:

   ```python
   x = 10
   if x > 10:
       print("x is greater than 10")
   elif x == 10:
       print("x is equal to 10")
   else:
       print("x is less than 10")
   ```

4. **while Loop:**

   - The `while` loop is used to repeatedly execute a block of code as long as a condition is true.

   Example:

   ```python
   i = 0
   while i < 5:
       print(i)
       i += 1
   ```

5. **for Loop:**

   - The `for` loop is used to iterate over a sequence (e.g., list, tuple, string).

   Example:

   ```python
   for i in range(5):
       print(i)
   ```

6. **break Statement:**

   - The `break` statement is used to exit a loop prematurely.

   Example:

   ```python
   for i in range(10):
       if i == 5:
           break
       print(i)
   ```

7. **continue Statement:**

   - The `continue` statement is used to skip the rest of the loop and continue with the next iteration.

   Example:

   ```python
   for i in range(10):
       if i % 2 == 0:
           continue
       print(i)
   ```

8. **range Function:**

   - The `range()` function is used to generate a sequence of numbers.

   Example:

   ```python
   for i in range(5):
       print(i)
   ```

9. **pass Statement:**

   - The `pass` statement is used as a placeholder for future code.

   Example:

   ```python
   x = 10
   if x > 5:
       pass  # Placeholder for future code
   ```

---

**Python Exception** Handling evaluates skills needed to guarantee that errors reported during the execution of a Python 3 program are properly processed to ensure proper application cleanup while maintaining useful error reporting.

1. **Handling Specific Exceptions:**

   - You can handle specific exceptions using `try-except` blocks.

   Example:

   ```python
   try:
       x = 10 / 0
   except ZeroDivisionError:
       print("Division by zero error occurred")
   ```

2. **Handling Multiple Exceptions:**

   - You can handle multiple exceptions using multiple `except` blocks or by specifying a tuple of exceptions.

   Example:

   ```python
   try:
       x = int("abc")
   except ValueError:
       print("ValueError occurred")
   except TypeError:
       print("TypeError occurred")
   ```

3. **Using `else` Block:**

   - You can use the `else` block to execute code if no exceptions occur in the `try` block.

   Example:

   ```python
   try:
       x = int("10")
   except ValueError:
       print("ValueError occurred")
   else:
       print("No exceptions occurred")
   ```

4. **Using `finally` Block:**

   - The `finally` block is used to execute cleanup code regardless of whether an exception occurred or not.

   Example:

   ```python
   try:
       file = open("example.txt", "r")
       # Perform file operations...
   except FileNotFoundError:
       print("File not found")
   finally:
       file.close()  # Close the file even if an exception occurred
   ```

5. **Raising Custom Exceptions:**

   - You can raise custom exceptions using the `raise` statement.

   Example:

   ```python
   def divide(a, b):
       if b == 0:
           raise ValueError("Division by zero")
       return a / b

   try:
       result = divide(10, 0)
   except ValueError as e:
       print(e)
   ```

6. **Handling Uncaught Exceptions:**

   - You can use a bare `except` block to catch all uncaught exceptions.

   Example:

   ```python
   try:
       x = 10 / 0
   except:
       print("An error occurred")
   ```

---

**Python Comprehensions** tests knowledge of how to derive new lists, dictionaries, sets, and iterators using Python 3 s comprehension syntax, as well as the use of functional tools like map and filter to build more expressive comprehensions.

1. **List Comprehensions:**

   - List comprehensions allow you to create new lists based on existing iterables.

   Example:

   ```python
   # Create a list of squares of numbers from 0 to 9 using list comprehension
   squares = [x**2 for x in range(10)]
   print(squares)  # Output: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
   ```

2. **Dictionary Comprehensions:**

   - Dictionary comprehensions allow you to create new dictionaries based on existing iterables.

   Example:

   ```python
   # Create a dictionary mapping numbers to their squares using dictionary comprehension
   squares_dict = {x: x**2 for x in range(1, 6)}
   print(squares_dict)  # Output: {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
   ```

3. **Set Comprehensions:**

   - Set comprehensions allow you to create new sets based on existing iterables.

   Example:

   ```python
   # Create a set of even numbers from 0 to 9 using set comprehension
   even_numbers = {x for x in range(10) if x % 2 == 0}
   print(even_numbers)  # Output: {0, 2, 4, 6, 8}
   ```

4. **Generator Expressions:**

   - Generator expressions are similar to list comprehensions but produce a generator object, which is an iterable.

   Example:

   ```python
   # Create a generator of squares of numbers from 0 to 9 using generator expression
   squares_generator = (x**2 for x in range(10))
   print(list(squares_generator))  # Output: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
   ```

5. **Using `map()` and `filter()`:**

   - `map()` and `filter()` functions can be used with lambda functions or other functions to achieve similar results to comprehensions.

   Example:

   ```python
   # Using map() to double each element of a list
   numbers = [1, 2, 3, 4, 5]
   doubled_numbers = list(map(lambda x: x * 2, numbers))
   print(doubled_numbers)  # Output: [2, 4, 6, 8, 10]

   # Using filter() to filter even numbers from a list
   even_numbers = list(filter(lambda x: x % 2 == 0, numbers))
   print(even_numbers)  # Output: [2, 4]
   ```

---

**Python Strings** evaluates knowledge of how to manipulate Python 3 strings, including slicing operations and Unicode encoding.

1. **Basic String Manipulation:**

   - You can perform basic string manipulation such as concatenation and repetition.

   Example:

   ```python
   # Concatenation
   string1 = "Hello"
   string2 = "World"
   result = string1 + ", " + string2
   print(result)  # Output: "Hello, World"

   # Repetition
   repeated_string = "abc" * 3
   print(repeated_string)  # Output: "abcabcabc"
   ```

2. **String Slicing:**

   - String slicing allows you to extract substrings from a string.

   Example:

   ```python
   text = "Python is awesome"
   print(text[0:6])  # Output: "Python"
   print(text[7:])   # Output: "is awesome"
   print(text[:6])   # Output: "Python"
   ```

3. **Unicode Encoding and Decoding:**

   - You can encode and decode strings to and from Unicode using the `encode()` and `decode()` methods.

   Example:

   ```python
   # Encoding from str to bytes
   text = "Python"
   encoded_text = text.encode('utf-8')
   print(encoded_text)  # Output: b'Python'

   # Decoding from bytes to str
   decoded_text = encoded_text.decode('utf-8')
   print(decoded_text)  # Output: "Python"
   ```

4. **Formatted Strings:**

   - Formatted strings allow you to embed expressions inside a string.

   Example:

   ```python
   name = "Alice"
   age = 30
   message = f"My name is {name} and I am {age} years old."
   print(message)  # Output: "My name is Alice and I am 30 years old."
   ```

5. **String Methods:**

   - Python provides various built-in methods for string manipulation, such as `upper()`, `lower()`, `strip()`, `split()`, and `join()`.

   Example:

   ```python
   text = "   Hello, World!   "
   print(text.upper())       # Output: "   HELLO, WORLD!   "
   print(text.strip())       # Output: "Hello, World!"
   print(text.split(','))    # Output: ['   Hello', ' World!   ']
   print('-'.join(['a', 'b', 'c']))  # Output: "a-b-c"
   ```

---

**Python Concurrency** assesses knowledge of Python 3 s facilities for concurrent code execution, including inter-thread communication and safety, such as are found in the threading, multiprocessing, and asyncio modules.

1. **Threading (using the `threading` module):**

   - Threading allows you to run multiple threads concurrently within the same process.

   Example:

   ```python
   import threading
   import time

   def print_numbers():
       for i in range(5):
           print(i)
           time.sleep(1)

   thread = threading.Thread(target=print_numbers)
   thread.start()
   ```

2. **Multiprocessing (using the `multiprocessing` module):**

   - Multiprocessing allows you to run multiple processes concurrently, taking advantage of multiple CPU cores.

   Example:

   ```python
   import multiprocessing

   def square(x):
       return x * x

   pool = multiprocessing.Pool(processes=4)
   result = pool.map(square, range(10))
   print(result)
   ```

3. **Asynchronous I/O (using the `asyncio` module):**

   - Asynchronous I/O allows you to perform I/O-bound operations concurrently without blocking the execution of other tasks.

   Example:

   ```python
   import asyncio

   async def print_numbers():
       for i in range(5):
           print(i)
           await asyncio.sleep(1)

   asyncio.run(print_numbers())
   ```

4. **Inter-Thread Communication:**

   - You can use synchronization primitives such as `Lock`, `Semaphore`, `Event`, and `Condition` to facilitate communication and coordination between threads.

   Example (using `Lock`):

   ```python
   import threading

   total = 0
   lock = threading.Lock()

   def increment():
       global total
       with lock:
           total += 1

   threads = []
   for _ in range(10):
       thread = threading.Thread(target=increment)
       threads.append(thread)
       thread.start()

   for thread in threads:
       thread.join()

   print(total)
   ```

---

**Python Generators and Coroutines** analyzes knowledge of generators and coroutine function syntax, how control flow differs from normal functions, and their application as iterators and in asynchronous programming.

1. **Generators (using the `yield` keyword):**

   - Generators allow you to generate a sequence of values lazily.

   Example:

   ```python
   def countdown(n):
       while n > 0:
           yield n
           n -= 1

   # Using the generator as an iterator
   for num in countdown(5):
       print(num)
   ```

2. **Coroutine Functions (using the `async def` syntax):**

   - Coroutine functions allow you to define asynchronous code blocks that can be paused and resumed.

   Example:

   ```python
   import asyncio

   async def greet():
       print("Hello")
       await asyncio.sleep(1)
       print("World")

   asyncio.run(greet())
   ```

3. **Asynchronous Generators (combining generators and coroutines):**

   - Asynchronous generators allow you to produce asynchronous streams of values lazily.

   Example:

   ```python
   async def async_countdown(n):
       while n > 0:
           yield n
           await asyncio.sleep(1)
           n -= 1

   # Using the asynchronous generator as an asynchronous iterator
   async for num in async_countdown(3):
       print(num)
   ```

4. **Coroutine Control Flow:**

   - Coroutine functions can be paused and resumed using `await` and `asyncio.sleep()`.

   Example:

   ```python
   async def my_coroutine():
       print("Start")
       await asyncio.sleep(1)
       print("Middle")
       await asyncio.sleep(1)
       print("End")

   asyncio.run(my_coroutine())
   ```

5. **Chaining Coroutines:**

   - Coroutines can be chained together using `await` to perform sequential asynchronous operations.

   Example:

   ```python
   async def greet():
       return "Hello"

   async def add_name(message):
       return message + ", World"

   async def main():
       message = await greet()
       message_with_name = await add_name(message)
       print(message_with_name)

   asyncio.run(main())
   ```

---

**Python Inheritance** determines ability to define a class that inherits all the methods and properties from another class within Python 3 code. This is part of object-oriented programming in Python

```python
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        raise NotImplementedError("Subclasses must implement this method")


class Dog(Animal):
    def speak(self):
        return "Woof!"


class Cat(Animal):
    def speak(self):
        return "Meow!"


# Creating instances of subclasses
dog = Dog("Buddy")
cat = Cat("Whiskers")

# Calling methods inherited from superclass
print(dog.name)  # Output: "Buddy"
print(cat.name)  # Output: "Whiskers"

# Calling subclass-specific methods
print(dog.speak())  # Output: "Woof!"
print(cat.speak())  # Output: "Meow!"
```

In the example above:

- `Animal` is the superclass, which has an `__init__` method to initialize the `name` attribute and a `speak` method. The `speak` method raises a `NotImplementedError` because it's meant to be implemented by subclasses.
- `Dog` and `Cat` are subclasses of `Animal`. They inherit all the methods and properties from `Animal`.
- Subclasses override the `speak` method to provide their own implementation.

This example demonstrates how to define classes that inherit from other classes in Python, as part of object-oriented programming.

---

**Python Precedence and Associativity** measures understanding of the order in which an expression is evaluated that has multiple operators of the same precedence in Python 3 code.

Precedence and associativity are fundamental concepts in Python (and in programming languages in general) that dictate the order in which operators are evaluated in an expression. Operators with higher precedence are evaluated first, and operators with the same precedence are evaluated based on their associativity, which can be left-to-right or right-to-left.

In Python, the precedence and associativity rules are consistent with most programming languages, but it's essential to understand them for writing correct and predictable code. Below is a summary of Python's precedence and associativity rules:

1. **Precedence:**

   - Operators with higher precedence are evaluated first.
   - Parentheses can be used to override the default precedence and force a specific evaluation order.

2. **Associativity:**
   - For operators with the same precedence, associativity determines the order of evaluation.
   - Most binary operators in Python are left-associative, meaning they are evaluated from left to right.
   - Exponentiation (`**`) is right-associative, meaning it is evaluated from right to left.

Here's an example illustrating precedence and associativity in Python:

```python
result = 2 + 3 * 4 ** 2 - 1
print(result)  # Output: 39
```

Explanation:

- Exponentiation (`**`) has the highest precedence, so `4 ** 2` is evaluated first, resulting in `16`.
- Multiplication (`*`) has higher precedence than addition (`+`), so `3 * 16` is evaluated next, resulting in `48`.
- Addition (`+`) and subtraction (`-`) have the same precedence, but they are left-associative, so `2 + 48` is evaluated first, resulting in `50`.
- Finally, `50 - 1` is evaluated, resulting in the final output `39`.

Understanding precedence and associativity is crucial for writing expressions that produce the desired results and avoiding ambiguity in the evaluation order. It's recommended to refer to Python's official documentation for a comprehensive list of operator precedence and associativity.

---

**Python Formatting and Decorators** tests knowledge of dynamically altering the functionality of a function, method, or class without having to directly use subclasses or change the Python 3 source code of the function being decorated.

1. **Function Decoration:**

   - Decorators allow you to modify or extend the behavior of functions or methods without changing their source code directly.

   Example:

   ```python
   def my_decorator(func):
       def wrapper():
           print("Something is happening before the function is called.")
           func()
           print("Something is happening after the function is called.")
       return wrapper

   @my_decorator
   def say_hello():
       print("Hello!")

   say_hello()
   ```

2. **Class Decoration:**

   - Decorators can also be applied to classes to modify their behavior.

   Example:

   ```python
   def my_class_decorator(cls):
       class NewClass(cls):
           def new_method(self):
               print("This is a new method.")
       return NewClass

   @my_class_decorator
   class MyClass:
       def existing_method(self):
           print("This is an existing method.")

   obj = MyClass()
   obj.existing_method()
   obj.new_method()
   ```

3. **Parameterized Decorators:**

   - Decorators can take arguments, allowing for more flexibility.

   Example:

   ```python
   def repeat(num_times):
       def decorator(func):
           def wrapper(*args, **kwargs):
               for _ in range(num_times):
                   result = func(*args, **kwargs)
               return result
           return wrapper
       return decorator

   @repeat(num_times=3)
   def greet(name):
       print(f"Hello, {name}!")

   greet("Alice")
   ```

4. **Built-in Decorators:**

   - Python provides built-in decorators like `@staticmethod`, `@classmethod`, and `@property` for modifying class methods.

   Example:

   ```python
   class MyClass:
       def __init__(self, value):
           self._value = value

       @property
       def value(self):
           return self._value

       @value.setter
       def value(self, new_value):
           self._value = new_value

   obj = MyClass(10)
   print(obj.value)  # Output: 10
   obj.value = 20
   print(obj.value)  # Output: 20
   ```

These examples demonstrate how to use decorators in Python to dynamically alter the functionality of functions, methods, or classes without directly modifying their source code. Decorators provide a powerful mechanism for adding cross-cutting concerns such as logging, caching, authentication, and more, making your code cleaner, more modular, and easier to maintain.

---

**Python Encapsulation** assesses ability to hide an object from view outside of the object's definition within Python 3 code. This is part of implementing object-oriented programming (OOP) in Python.

Encapsulation is one of the fundamental principles of object-oriented programming (OOP) that allows you to hide the internal state and implementation details of an object from the outside world. In Python, encapsulation can be achieved using private attributes and methods, which are not directly accessible from outside the class.

Here's an example demonstrating encapsulation in Python:

```python
class Car:
    def __init__(self, make, model):
        self.__make = make  # Private attribute
        self.__model = model  # Private attribute

    def get_make(self):
        return self.__make

    def set_make(self, make):
        self.__make = make

    def get_model(self):
        return self.__model

    def set_model(self, model):
        self.__model = model


# Creating an instance of the Car class
car = Car("Toyota", "Camry")

# Accessing private attributes directly will raise an AttributeError
# print(car.__make)  # Raises AttributeError

# Accessing private attributes using getter methods
print(car.get_make())  # Output: "Toyota"
print(car.get_model())  # Output: "Camry"

# Modifying private attributes using setter methods
car.set_make("Honda")
car.set_model("Accord")

print(car.get_make())  # Output: "Honda"
print(car.get_model())  # Output: "Accord"
```

In the example above:

- `__make` and `__model` are private attributes of the `Car` class, indicated by the double underscores (`__`) prefix.
- Getter and setter methods (`get_make`, `set_make`, `get_model`, `set_model`) are provided to access and modify the private attributes.
- Direct access to private attributes from outside the class will raise an `AttributeError`, enforcing encapsulation.

Encapsulation helps to protect the internal state of an object and provides a clear interface for interacting with it, improving code maintainability and reducing the risk of unintended side effects.

---

**Python Functional Programming** determines knowledge of and using functional programming patterns in Python 3 code. Includes avoiding state changes as much as possible and writing functions that take and return instances representing objects in an application.

Functional programming is a programming paradigm that treats computation as the evaluation of mathematical functions and avoids changing state and mutable data. While Python is not a purely functional programming language, it supports many functional programming concepts and patterns. Below are examples demonstrating functional programming patterns in Python 3:

1. **Avoiding State Changes:**

   - Use immutable data structures like tuples and frozensets to avoid changing state.
   - Prefer pure functions that do not modify global state or have side effects.

   Example:

   ```python
   # Pure function
   def add(a, b):
       return a + b

   # Immutable data structure (tuple)
   point = (1, 2)
   ```

2. **Using Higher-Order Functions:**

   - Functions that take other functions as arguments or return functions are called higher-order functions.

   Example:

   ```python
   # Higher-order function
   def apply(func, value):
       return func(value)

   result = apply(lambda x: x ** 2, 3)
   print(result)  # Output: 9
   ```

3. **List Comprehensions and Functional Tools:**

   - List comprehensions and functional tools like `map()`, `filter()`, and `reduce()` can be used for functional programming in Python.

   Example:

   ```python
   # List comprehension
   squares = [x ** 2 for x in range(5)]

   # Using map()
   numbers = [1, 2, 3, 4, 5]
   squares = list(map(lambda x: x ** 2, numbers))

   # Using filter()
   evens = list(filter(lambda x: x % 2 == 0, numbers))
   ```

4. **Lambda Functions:**

   - Lambda functions are small anonymous functions that can be used where function objects are required.

   Example:

   ```python
   # Lambda function
   add = lambda x, y: x + y
   result = add(3, 4)
   print(result)  # Output: 7
   ```

5. **Recursion:**

   - Functional programming encourages the use of recursion for solving problems.

   Example:

   ```python
   # Recursive function
   def factorial(n):
       if n == 0:
           return 1
       else:
           return n * factorial(n - 1)
   ```

These examples demonstrate how to apply functional programming concepts and patterns in Python 3 code. While Python is not a purely functional programming language, it provides support for many functional programming features, allowing you to write clean, concise, and expressive code.

---
