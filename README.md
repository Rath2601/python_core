# Python Notes
## 📌 Syntax Basics
- **Comments**: Use `\n` or triple quotes (`'''` or `"""`).  single -> `# comment`
- **Indentation** is crucial (standard: 4 spaces). Inconsistent indentation causes errors.
- Python uses indentation instead of `{}` for blocks. No semicolons `;` needed.
- No package declaration required. `import` can be placed anywhere.
- Functions do not need declared return types.
---
## 🔤 Data Types
1. Numeric: `int`, `float`, `complex`
2. Boolean: `bool`
3. String: `str`
4. Sequence: `list`, `tuple`
5. Set types: `set`, `frozenset`
6. Mapping: `dict`
---
## 📦 Variables
- Dynamic typing: variables can change types.
- Use `type()` to find a variable's datatype.
- Strings can use single `'` or double `"` quotes.
- Variable & method naming: `lowercase_with_underscores` (PEP 8).
- Case sensitive.
---
## 🧰 Built-in Functionality
- Strings are immutable (like Java).
- Supports ASCII: `ord('a')` → 97, `chr(97)` → `'a'`
---
## ➕ Arithmetic Operators

| Operator | Description          |
|----------|----------------------|
| `+`      | Addition             |
| `-`      | Subtraction          |
| `*`      | Multiplication       |
| `/`      | Division (float)     |
| `//`     | Floor Division       |
| `%`      | Modulus              |
| `**`     | Power                |

---

## 🧮 Comparison & Logical Operators

| Category         | Operators                                     |
|------------------|-----------------------------------------------|
| Comparison       | `==`, `!=`, `<`, `>`, `<=`, `>=`              |
| Logical          | `not`, `and`, `or`                            |
| Identity         | `is`, `is not`                                |
| Membership       | `in`, `not in`                                |
| Bitwise          | `&`, `|`, `^`, `~`, `<<`, `>>`                |

---

## 🧱 Data Structures
### 🔹 List
- Mutable, supports mixed types and indexing.
- Negative indexing: `-1` refers to last item.
- Slice: `my_list[start:end]`
**Common List Methods:**
- `extend()`, `append()`, `insert(index, item)`
- `remove(item)`, `clear()`, `pop()`
- `index(item)`, `count(item)`
- `sort()`, `reverse()`, `copy()`
### 🔹 Tuple
- Immutable version of list
- Uses `()` brackets
### 🔹 Dictionary
- Key-value pairs using `{}`.
- Keys must be unique (can include `None`).
- Use `.get(key, default)` for safe retrieval.
---
## 🔁 Loops
- `for` loops can iterate over: list, string, dict, range, `enumerate`, `zip`
- `range(start, stop, step)` – `stop` value is excluded
- List comprehensions supported
---
## ❗ Exception Handling
- Use `try-except`, `try-finally`, or `try-except-finally` blocks
---
## 📁 File Handling
- `open(file_path, mode)` → returns file object
- `read()`, `readline()`, `readlines()`, `write()`, `writelines()`
- `close()`, `with open() as f:` preferred for auto-close
- Modes: `r`, `w`, `a`, `r+`
- Encoding: `utf-8`, `ascii`, `latin-1`, etc.
---
## 📦 Modules & pip
- A module = `.py` file with functions, variables, classes.
- `import` imports module, not class/function by default.
  - Use `from module import ClassName`
- Built-in, standard library, and 3rd-party (site-packages)
- `pip install <package>`, `pip uninstall <package>`
### 🔸 Virtual Environments (.venv)
- Isolated project environments
- Prevents dependency conflicts
- Recommended for multi-project development
---
## 👨‍💻 OOP in Python
### 🔹 Classes & Objects
- Attributes can be added dynamically (use `__slots__` to restrict)
- Use `__init__()` with  hint type, default values and `assert`
- Use `__dict__` to inspect attributes
- class variable can be set individually for all instances seperately without affecting other instances.
- `__repr__()` → debug representation
- `__str__()` → user-friendly display
### 🔹 Method Types
 **Instance Method**: Defined with `def method(self)` — has access to instance variables via `self`.
- **Class Method**: Defined with `@classmethod def method(cls)` — has access to class variables via `cls`.
- **Static Method**: Defined with `@staticmethod def method()` — has no automatic access to instance or class variables.
- Use `*args` and `**kwargs` for flexible arguments
- Private members: prefix with `__` (name mangling) (private not like Java)
- there is no final variable in python.
- @final in  `from typing import final` can be used to avoid overriding or inheritance of method and class respectively
---
## 🧬 Inheritance
- Supports single, multi-level, and multiple inheritance
- Child inherits class-level attributes
- Parent doesn't access child attributes
- Use `f"{self.__class__.__name__}({self.__dict__})"` for generic `__repr__`
- MRO (Method Resolution Order): C3 Linearization algorithm
---
## 🧴 Encapsulation
- Pythonic way: `@property`, `@<field>.setter`
- Use `_field` naming convention
- Also supports traditional getters/setters
---
## 🔒 Abstraction
- Use `ABC` from `abc` module
- Abstract methods: `@abstractmethod`. abstract must be overriden (in polymorphism its optional)
- Can include concrete methods, static method & class method
- Cannot instantiate directly
- Interface: all methods abstract
- Unlike Java, abstract methods can have body
---
## 🔁 Polymorphism
- Runtime (duck typing) and Compile-time
- duck typing is form of runtime (dynamic binding but without strict override)
- Use `@dispatch` from `multipledispatch` for true overloading. default value & *args can be used for overloading
---

## Python Built-in Methods and Features
### 🔤 String Methods (`str`)
- `capitalize()`
- `casefold()`
- `center()`
- `count()`
- `encode()`
- `endswith()`
- `expandtabs()`
- `find()`
- `format()`
- `format_map()`
- `index()`
- `isalnum()`
- `isalpha()`
- `isascii()`
- `isdecimal()`
- `isdigit()`
- `isidentifier()`
- `islower()`
- `isnumeric()`
- `isprintable()`
- `isspace()`
- `istitle()`
- `isupper()`
- `join()`
- `ljust()`
- `lower()`
- `lstrip()`
- `maketrans()`
- `partition()`
- `replace()`
- `rfind()`
- `rindex()`
- `rjust()`
- `rpartition()`
- `rsplit()`
- `rstrip()`
- `split()`
- `splitlines()`
- `startswith()`
- `strip()`
- `swapcase()`
- `title()`
- `translate()`
- `upper()`
- `zfill()`
---
### 📜 List Methods (`list`)
- `append()`
- `clear()`
- `copy()`
- `count()`
- `extend()`
- `index()`
- `insert()`
- `pop()`
- `remove()`
- `reverse()`
- `sort()`
---
### 📦 Dictionary Methods (`dict`)
- `clear()`
- `copy()`
- `fromkeys()`
- `get()`
- `items()`
- `keys()`
- `pop()`
- `popitem()`
- `setdefault()`
- `update()`
- `values()`
---
### 🎯 Set Methods (`set`)
- `add()`
- `clear()`
- `copy()`
- `difference()`
- `difference_update()`
- `discard()`
- `intersection()`
- `intersection_update()`
- `isdisjoint()`
- `issubset()`
- `issuperset()`
- `pop()`
- `remove()`
- `symmetric_difference()`
- `symmetric_difference_update()`
- `union()`
- `update()`
---
### 🧵 Tuple Methods (`tuple`)
- `count()`
- `index()`
---
### ⚙️ Built-in Functions
- `len()`
- `type()`
- `str()`
- `int()`
- `float()`
- `list()`
- `tuple()`
- `set()`
- `dict()`
- `bool()`
- `sum()`
- `max()`
- `min()`
- `sorted()`
- `reversed()`
- `enumerate()`
- `zip()`
- `map()`
- `filter()`
- `any()`
- `all()`
---
### 🧠 Built-in Features
1. **Slicing**
   - Syntax: `sequence[start:stop:step]`
   - Works on: `str`, `list`, `tuple` (works only on DS supports index based access)
