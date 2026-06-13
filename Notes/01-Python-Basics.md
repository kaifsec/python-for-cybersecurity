# Python Foundations

## What is Python?
Python is a high-level, interpreted programming language known for its clean syntax and readability. It allows you to write code faster and with fewer lines compared to older languages.

### Features of Python:
* **Easy to Use:** The syntax looks like simple English, making it fast to learn and write.
* **Versatile:** It can be used for web development, cloud automation, data science, and security.
* **Extensive Libraries:** It has thousands of pre-written code packages (libraries) so you don't have to code tools from scratch.
* **Cross-Platform Compatibility:** The same Python script runs on Windows, Linux, or macOS without modifications.
* **Community Support:** It is one of the most popular languages in the world, meaning every error or question already has an answer online.

### The Role of Python in Cybersecurity:
In security, time is everything. Python is the ultimate language for **automation**. Cybersecurity professionals use it to:
1. Automate repetitive tasks (like parsing giant firewall log files for malicious IPs).
2. Write custom network port scanners to find vulnerabilities.
3. Automate cloud security checks in AWS.
4. Interact with APIs to block threats instantly across routers and firewalls.

## Python Syntax Basics

Syntax rules dictate how code must be written so the Python interpreter can understand it.

### 1. Statements and Line Breaks
* **One line per statement:** By default, each instruction goes on its own line.
  * *Example:*
    ```python
    print("Scanning Network...")
    print("Scan Complete.")
    ```
* **Semicolon (`;`):** We can use it to force multiple statements onto a single line.
  * *Example:* `ip = "10.0.0.1" ; port = 80`
* **Line Continuation (`\`):** We can use it to break a long line of code into multiple lines without breaking the program.
  * *Example:*
    ```python
    long_string = "This is a very long security alert " \
                  "that needs to be split up."
    ```

### 2. Indentation and White Space
* **Indentation matters:** Python does not use curly brackets `{}` to group blocks of code (like functions or loops). Instead, it uses **4 spaces** of indentation.
* **White Space:** Blank lines are ignored by Python. We can use them freely to make your code easier to read. 

### 3. Comments (`#`)
* Text starting with a `#` is completely ignored by Python. It can be used to explain what the script is doing.
  * *Example:* `# This line connects to the database`

### 4. Functions
* Blocks of reusable code that only run when called. They start with the `def` keyword.
  * *Example:*
    ```python
    def alert_admin():
        print("ALERT: Unauthorized Access!")
    ```

### 5. Imports
* Used to bring in external code libraries so the user doesn't have to code tools from scratch.
  * *Example:* `import os` or `import socket`

### 6. Keywords
* Special reserved words in Python that have built-in meanings (like `def`, `import`, `if`, `True`, `print`). We cannot use these words as names for the variables.


## Variables and Data Types Deep Dive

Variables are containers for storing data values, and data types define what kind of value is inside that container.

### Variable Naming Rules
To write valid Python code, variable names must follow these strict guidelines:
* **Must start with** a letter or an underscore (`_`). They cannot start with a number.
* **Can only contain** alphanumeric characters and underscores (`A-z`, `0-9`, and `_`). No spaces or special characters allowed.
* **Case-Sensitive:** `target_ip`, `Target_Ip`, and `TARGET_IP` are treated as three completely different variables.
* **No Keywords:** You cannot use words like `import`, `def`, or `if` as variable names.

### Comprehensive Data Types Summary
Here are the essential built-in data types in Python with easy examples:

#### 1. Numeric Types
* **int (Integer):** Whole numbers, positive or negative, without decimals.
  * *Example:* `port = 80`
* **float (Floating Point):** Numbers containing one or more decimals.
  * *Example:* `version = 3.11`

#### 2. Sequence Types
* **str (String):** Text data wrapped inside single or double quotes.
  * *Example:* `attacker_ip = "192.168.1.105"`
* **list:** An ordered, changeable collection of items wrapped in square brackets `[]`.
  * *Example:* `open_ports = [22, 80, 443]`
* **tuple:** An ordered collection that **cannot be changed** once created, wrapped in parentheses `()`.
  * *Example:* `server_coordinates = (12.97, 77.59)`

#### 3. Mapping Type
* **dict (Dictionary):** Stores data in "Key: Value" pairs inside curly brackets `{}`. Great for looking up specific data.
  * *Example:* `target_info = {"os": "Linux", "status": "Online"}`

#### 4. Boolean Type
* **bool:** Represents logical values. Can only be `True` or `False`. (Note the capital T and F!).
  * *Example:* `is_vulnerable = True`

### Python Number Types
* **int (Integer):** Whole numbers without decimals.
  * *Example:* `ports = 80`
* **float (Floating Point):** Numbers containing decimal points.
  * *Example:* `version = 3.11`
* **complex (Complex Numbers):** Numbers with a real and an imaginary part ending in `j`.
  * *Example:* `wave = 3 + 5j`

### Strings in Python
* **Strings:** Text data wrapped in quotes.
* **Single or Double Quotes:** Used for normal, single-line text.
  * *Example:* `name = 'Kaif'` or `role = "Admin"`
* **Triple Quotes (`'''` or `"""`):** Used if your text spans across multiple lines.
  * *Example:*
    ```python
    banner = """WARNING:
    Unauthorized access prohibited!"""
    ```

### Booleans in Python
* **Boolean:** A data type that can only be `True` or `False`. (Must use capital T and F).
  * *Example:* `is_admin = True`

### Boolean Operations
* **and:** Returns `True` only if **both** sides are true.
  * *Example:* `True and False` gives `False`
* **or:** Returns `True` if **at least one** side is true.
  * *Example:* `True or False` gives `True`
* **not:** Flips the value to its opposite.
  * *Example:* `not True` gives `False`

### Tuples in Python
* **Tuple:** A collection of items that **cannot be changed** (immutable) once created.
* **Creating a Tuple:** Uses normal parentheses `()`.
  * *Example:* `ports = (22, 80, 443)`
* **Without Parentheses:** Python automatically turns comma-separated values into a tuple.
  * *Example:* `ips = "10.0.0.1", "10.0.0.2"`
* **Single Item Tuple:** We **must** put a trailing comma at the end, or Python thinks it's just a normal number/string.
  * *Example:* `my_tuple = (5,)`

### Lists in Python
* **List:** A collection of items that **can be changed** (mutable) and keeps its order. Uses square brackets `[]`.
  * *Example:* `ips = ["10.0.0.1", "192.168.1.1"]`

### Accessing & Slicing
* **Index:** Access a single item starting from position `0`.
  * *Example:* `ips[0]` gives `"10.0.0.1"`
* **Slicing:** Grabs a chunk of the list `[start:stop]`. (Stop position is not included).
  * *Example:* `ips[0:2]`

### Modifying Lists
* **append(item):** Adds an item to the absolute end.
  * *Example:* `ips.append("172.16.0.1")`
* **insert(index, item):** Inserts an item at a specific position.
  * *Example:* `ips.insert(1, "8.8.8.8")`
* **extend([items]):** Adds multiple items at once to the end.
* **remove(value):** Deletes an item by its name/value.
  * *Example:* `ips.remove("10.0.0.1")`
* **pop(index):** Deletes an item by its position number.
* **clear():** Wipes out everything, leaving the list completely empty `[]`.

### Dictionaries in Python
* **Dictionary:** A collection that stores data in **Key-Value pairs** inside curly brackets `{}`. 
* **Creating:** You assign a label (Key) to a piece of data (Value) using a colon `:`.
  * *Example:* `user = {"name": "Kaif", "role": "Admin"}`
* **Accessing:** You call the data by using its specific Key name inside square brackets `[]`.
  * *Example:* `user["role"]` gives `"Admin"`

### Sets in Python
* **Set:** An unordered collection of **unique items**. It uses curly brackets `{}`, but no colons.
* **Removes Duplicates:** If you put duplicate items in a set, Python automatically throws the duplicates away.
  * *Example:* `my_set = {1, 2, 1, 3}` becomes `{1, 2, 3}`
* **Empty Set:** You must use `set()` to make an empty set. (Using `{}` makes an empty dictionary instead).
  * *Example:* `bad_ips = set()`

### Conditional Statements in Python
* **Conditional Statements:** Let your code make decisions and execute actions based on specific conditions.

### Syntax Components
* **if:** Evaluates a condition. If true, the code inside runs.
* **elif (else if):** Checked only if the previous conditions were false.
* **else:** Runs automatically if none of the above conditions match.
* **Nested Conditionals:** An `if` statement written inside another `if` statement.

### Code Example
```python
score = 85

if score >= 90:
    print("Grade A")
elif score >= 75:
    print("Grade B")
else:
    print("Fail")
```

### Loops
* **For Loop**

* **What it does:** Runs a code block for each item in a sequence(like a list or a range)

fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)

                 
