### AngloScript Language Documentation

**Version 1.0**

---

### Table of Contents:

1. **Overview**
2. **Key Design Principles**
3. **Language Syntax**
    - Basic Syntax
    - Variable Declarations
    - Functions and Methods
    - Control Flow
    - Error Handling
4. **Data Types and Operations**
    - Supported Data Types
    - Operators
    - Arrays and Lists
5. **Code Structure and Formatting**
    - Single-Line Code Formatting
    - Multi-Line Code Formatting
6. **Example Code**
    - Hello World Example
    - Variable Declaration and Assignment
    - Functions and Methods
    - Control Flow (if, while, for)
    - Error Handling
7. **AngloScript and Other Languages**
    - Python Comparison
    - Assembly Comparison
8. **Interpreting and Running Code**
    - Code Execution
    - IDE and Terminal Use
9. **Modules and Built-in Functions**
    - System Module
    - Custom Functions
10. **Future Directions**

---

### 1. Overview

AngloScript is a high-level programming language inspired by various popular languages such as **Holy C**, **Python**, **C#**, **Scratch**, **BASIC**, and **GameMakerLanguage**. The language is designed to be extremely simple, intuitive, and modular, with a syntax that is both beginner-friendly and powerful enough for advanced users. AngloScript is tailored to be the easiest programming language in the world, suitable for children and beginners transitioning from languages like **Scratch** or **BASIC**.

The language features a structure and set of commands designed to be as simple as possible, relying heavily on the English language and Anglo-Saxon culture for naming conventions. Key aspects of the language include:
- A simple and human-readable syntax
- The use of **Runes** to denote modules, classes, and other elements
- A highly modular and flexible design, allowing easy addition of features
- Support for both single-line and multi-line code formatting

---

### 2. Key Design Principles

1. **Simplicity**: AngloScript prioritizes easy readability and simplicity, with a focus on making it beginner-friendly and easy to use. Its syntax is designed to resemble plain English, making it more accessible to non-programmers.
2. **Modularity**: AngloScript supports modular programming, allowing users to create and use pre-defined functions, classes, and modules easily. It enables users to write reusable code, making it ideal for larger projects.
3. **Intuitive Syntax**: The keywords, operators, and structure of the language are designed to be intuitive and easy to understand. For example, variable declarations use keywords like `mark` and function declarations use `rune`.
4. **Minimalist**: The language avoids unnecessary complexity. It does not have complicated concepts such as pointers or low-level memory management, making it more accessible to beginners.
5. **Flexibility**: AngloScript supports flexible code formatting, allowing for both compact, single-line code and traditional multi-line code.

---

### 3. Language Syntax

#### **Basic Syntax**
The basic syntax of AngloScript follows simple English phrases and concepts. Key elements include:
- **Variable Declarations**: `mark x = 5`
- **Function Declarations**: `rune greet(name) { write "Hello, " + name + "!" }`
- **Output/Printing**: `write "Hello World!"`

#### **Variable Declarations**
In AngloScript, variables are declared using the `mark` keyword. For example:
```angloscript
mark x = 5
mark y = 10
```
This assigns the value `5` to `x` and `10` to `y`.

#### **Functions and Methods**
Functions are defined using the `rune` keyword, followed by the function name and parameters. For example:
```angloscript
rune greet(name)
    write "Hello, " + name + "!"
end
```
This function takes a `name` parameter and prints a greeting message.

#### **Control Flow**
AngloScript supports basic control flow structures:
- **Conditionals**: `if`, `else`
- **Loops**: `while`, `for`
```angloscript
if x > y then
    write "x is greater than y"
else
    write "y is greater than x"
end

for i = 1 to 10 do
    write i
end
```

#### **Error Handling**
Errors are handled simply through exception-based syntax, where the interpreter will display error messages when invalid operations are encountered.

---

### 4. Data Types and Operations

#### **Supported Data Types**
AngloScript supports basic data types including:
- **Integers**: `mark x = 5`
- **Strings**: `"Hello"`
- **Booleans**: `True`, `False`
- **Lists/Arrays**: `mark numbers = [1, 2, 3]`

#### **Operators**
AngloScript supports the following operators:
- **Arithmetic**: `+`, `-`, `*`, `/`, `%`
- **Comparison**: `==`, `!=`, `<`, `>`, `<=`, `>=`
- **Logical**: `and`, `or`, `not`
- **Concatenation**: `+` (for strings)

---

### 5. Code Structure and Formatting

#### **Single-Line Code Formatting**
AngloScript supports writing code in a compact, single-line format. For example:
```angloscript
mark x = 5 mark y = 10 write x + y
```

#### **Multi-Line Code Formatting**
For readability, traditional multi-line formatting is also supported:
```angloscript
mark x = 5
mark y = 10
write x + y
```

This flexibility allows developers to structure their code however they prefer, depending on the environment they are working in (e.g., terminal-based or IDE).

---

### 6. Example Code

#### **Hello World Example**
```angloscript
write "Hello, World!"
```

#### **Variable Declaration and Assignment**
```angloscript
mark x = 5
mark y = 10
write x + y
```

#### **Functions and Methods**
```angloscript
rune greet(name)
    write "Hello, " + name + "!"
end

greet("AngloScript")
```

#### **Control Flow**
```angloscript
mark x = 5
mark y = 10

if x > y then
    write "x is greater than y"
else
    write "y is greater than x"
end
```

#### **Loops**
```angloscript
for i = 1 to 10 do
    write i
end
```

---

### 7. AngloScript and Other Languages

#### **Python Comparison**

| AngloScript                          | Python                           |
|--------------------------------------|----------------------------------|
| `mark x = 5`                         | `x = 5`                          |
| `write "Hello, World!"`              | `print("Hello, World!")`         |
| `rune greet(name) { ... }`           | `def greet(name): ...`           |
| `if x > y then ... else ... end`      | `if x > y: ... else: ...`        |
| `for i = 1 to 10 do ... end`          | `for i in range(1, 11): ...`     |

#### **Assembly Comparison**

| AngloScript                          | Assembly (x86)                    |
|--------------------------------------|-----------------------------------|
| `mark x = 5`                         | `mov eax, 5`                      |
| `write "Hello, World!"`              | `mov eax, "Hello, World!"`        |
| `rune greet(name) { ... }`           | `greet: ...`                      |
| `if x > y then ... else ... end`      | `cmp eax, ebx`                    |
| `for i = 1 to 10 do ... end`          | `mov ecx, 10`                    |

---

### 8. Interpreting and Running Code

To run AngloScript code, it can be executed in an interpreter that reads the script line by line and processes each command. This can be done through an integrated IDE or terminal-based interface.

- **IDE Usage**: Users can type commands into an editor, then run the code and see the output printed to the console.
- **Terminal Usage**: Users can directly input commands or write scripts and execute them in the terminal.

---

### 9. Modules and Built-in Functions

#### **System Module**
AngloScript includes a built-in `System` module that contains common system functions such as:
- **System.time()**: Returns the current system time.
```angloscript
write System.time()
```

#### **Custom Functions**
Users can define custom functions using the `rune` keyword. Functions can accept parameters and return values:
```angloscript
rune greet(name)
    write "Hello, " + name + "!"
end
greet("AngloScript")
```

---

### 10. Future Directions

While the language is currently focused on simplicity and beginner-friendliness, there are plans to expand its capabilities:
- **More Built-in Modules**: Support for more complex tasks (e.g., file I/O, networking, etc.)
- **Better Error Handling**: Enhanced mechanisms for catching and handling errors
- **IDE Enhancements**: A fully integrated IDE with syntax highlighting, debugging tools, and more
- **Performance Improvements**: Optimizing the interpreter for larger applications

---

### Conclusion

AngloScript is designed to be a highly intuitive, flexible, and easy-to-use programming language that emphasizes readability and simplicity. Its ability to support both single-line and multi-line code allows for flexible use in a variety of environments, from beginner to advanced levels. This documentation has provided an in-depth look into the language's features, syntax, and functionality, and we look forward to its continued evolution.

