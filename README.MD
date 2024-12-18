# AngloScript Full Documentation

**Version 1.4**  
**Author:** AngloScript Development Team  
**Last Updated:** December 2024  

---

## **Table of Contents**

1. [Overview](#1-overview)  
2. [Key Features](#2-key-features)  
3. [Syntax](#3-syntax)  
   - Basic Program Structure  
   - Comments  
   - Declarations  
   - Data Types  
   - Control Flow  
   - Functions  
   - Classes and Runes  
   - Modules  
   - Input/Output  
   - Error Handling  
   - External Code Integration  
   - Built-in Modules  
4. [Keywords Reference](#4-keywords-reference)  
5. [Module Types](#5-module-types)  
6. [AngloScript and Other Languages](#6-angloscript-and-other-languages)  
   - Comparison to Python  
   - Comparison to Assembly  
   - Comparison to BASIC  
7. [Interpreting and Running Code](#7-interpreting-and-running-code)  
   - Compilable and Non-Compilable Nature  
   - JIT Compatibility  
8. [Advanced Features Explained](#8-advanced-features-explained)  
   - Event-Driven Programming  
   - Multi-Threading and Asynchronous Processing  
9. [Example Code](#9-example-code)  
10. [Features from Holy C, Python, and BASIC](#10-features-from-holy-c-python-and-basic)  
11. [AngloScript’s Unique Flexibility](#11-angloscripts-unique-flexibility)  
12. [Future Directions](#12-future-directions)  

---

## **1. Overview**

AngloScript is a high-level programming language designed for ease of use, particularly for beginners transitioning from BASIC or Scratch. It combines elements from various programming languages, including **Holy C**, **Python**, **C#**, and **GameMaker Language**, while incorporating a unique Anglo-Saxon theme. The language aims to be modular, intuitive, and accessible, making it suitable for educational purposes and game development.

AngloScript’s syntax is designed to be incredibly intuitive, taking inspiration from various languages to balance simplicity and complexity.

### **1. Basic Program Structure**

```angloscript
rune MyRune class {
    does main() {
        write "Hello, World!";
    }
}
```

This structure consists of:

- **rune**: Used to declare classes, modules, or events.
- **does**: Defines a function or method.
- **main()**: The entry point of the program.
- **write()**: A built-in function to output text.

### **2. Comments**

- **Single-line comment**:
```angloscript
# This is a single-line comment
```

- **Multi-line comment**:
```angloscript
## This is a multi-line comment
   that spans across lines ##
```

### **3. Declarations**

- **Mutable Variable Declaration** (using `mark`):
```angloscript
mark x = 10;  # Declares a mutable variable x
```

- **Immutable Constant Declaration** (using `bind`):
```angloscript
bind Pi = 3.14159;  # Declares a constant Pi
```

### **4. Data Types**

- **number**: Integer or floating point.
- **text**: String of characters enclosed in quotation marks.
- **boolean**: Boolean value (`True` or `False`).
- **list**: Ordered collection, similar to arrays.
- **map**: Unordered collection of key-value pairs (similar to dictionaries in Python).
- **function**: A function itself can be a variable.

### **5. Control Flow**

- **Conditionals**:

```angloscript
if x > 10 then
    write "Big!";
elif x == 10 then
    write "Exactly!";
else
    write "Small!";
```

- **Loops**:
    - **For Loop**:
    ```angloscript
    loop mark i = 1 to 10 {
        write i;
    }
    ```

    - **While Loop**:
    ```angloscript
    while x > 0 {
        write x;
        x = x - 1;
    }
    ```

### **6. Functions**

- **Function Declaration**:

```angloscript
does greet(name) {
    write "Hello, " + name;
}
```

- **Return Values**:

```angloscript
does add(a, b) {
    give a + b;
}
```

### **7. Classes and Runes**

- **Class Declaration** (`rune class`):

```angloscript
rune Player class {
    has health = 100;
    
    does heal(amount) {
        health = health + amount;
    }
}
```

- **Inheritance** (`rune class > ParentClass`):

```angloscript
rune NPC class > Player {
    has dialogue = "Hello!";
    does speak() {
        write dialogue;
    }
}
```

### **8. Modules**

- **Module Declaration**:

```angloscript
rune Math module {
    does add(a, b) {
        give a + b;
    }
}
```

- **Module Usage**:

```angloscript
mark result = Math.add(2, 3);
```

### **9. Input/Output**

- **Writing to the Console**:

```angloscript
write "Hello!";
```

- **Reading User Input**:

```angloscript
mark name = ask "What is your name?";
write "Hello, " + name;
```

### **10. Error Handling**

- **Try-Catch**:

```angloscript
try {
    mark x = 10 / 0;
} catch Error {
    write "Something went wrong!";
}
```

### **11. External Code Integration**

- **Embedding Assembly**:

```angloscript
asm {
    mov eax, 10;
}
```

- **Embedding JavaScript**:

```angloscript
js {
    console.log("Hello from JavaScript!");
}
```

- **Embedding Lua**:

```angloscript
lua {
    print("Hello from Lua!");
}
```

### **12. Built-in Modules**

- **Math Module**: Includes basic arithmetic functions.
```angloscript
rune Math module {
    does add(a, b) { give a + b; }
    does subtract(a, b) { give a - b; }
    does multiply(a, b) { give a * b; }
    does divide(a, b) { give a / b; }
    does round(n) { give round(n); }
    does random(min, max) { give random(min, max); }
}
```

## **4. Keywords Reference**

| Keyword  | Purpose | Assembly Equivalent | Python Equivalent |
|----------|---------|---------------------|-------------------|
| mark     | Mutable variable declaration. | `mov` | `=` |
| bind     | Immutable constant declaration. | `dw` | Constant declaration (uppercase) |
| rune     | Class/module/event/interface keyword. | `.text` or `.data` | `class` or `import` |
| does     | Function definition. | `label:` | `def` |
| give     | Return value from a function. | `mov eax, return_value` | `return` |
| write    | Print to console. | `call printf` | `print()` |
| ask      | Get user input. | `call scanf` | `input()` |
| loop     | Start a loop structure. | `cmp, jmp, inc/dec` | `for/while` |
| if       | Conditional branching. | `cmp, jne` | `if` |
| try      | Error handling block. | `cmp eax, 0` | `try:` |
| catch    | Error handler. | `jmp catch_block` | `except:` |
| asm      | Inline assembly. | Raw ASM | Custom integration required. |
| js       | Inline JavaScript execution. | Not applicable. | Custom integration required. |

## **5. Module Types**

| AngloScript Module Type | Purpose | Assembly Equivalent | Python Equivalent |
|--------------------------|---------|---------------------|-------------------|
| rune [class]             | Defines a class with properties and methods. | `.data section for variables, .text for methods.` | `class MyClass:` |
| rune [module]            | Declares a module for reusable functions. | `.text section for function logic.` | `class ModuleName: with @staticmethod` |
| rune [interface]         | Defines a shared behavior structure. | None directly. Similar to jump tables. | Abstract base class with abc module. |
| rune [event]             | Event listener for handling triggers. | None directly. Implemented as callbacks. | `def event_handler(event):` |

## **6. AngloScript and Other Languages**

### **Comparison to Python**

| Feature | Python | AngloScript |
|---------|--------|-------------|
| Variables | Declared with `=` | `mark` for mutable variables, `bind` for constants |
| Functions | Declared with `def` | Declared with `does` |
| Classes | Declared with `class` | Declared with `rune` |
| Looping | `for` / `while` loops | `loop` / `while` loops |
| Input | `input()` | `ask` |
| Output | `print()` | `write` |

### **Comparison to Assembly**

| Feature | Assembly | AngloScript |
|---------|----------|-------------|
| Variables | `mov eax, value` | `mark x = value` |
| Constants | `dw CONSTANT` | `bind CONSTANT = value` |
| Functions | Labels and `call` instructions | `does` keyword for function declaration |
| Classes/Modules | Data sections for variables, Text sections for methods | `rune` defines classes, modules |
| Inline Assembly | Direct inline assembly code | `asm {}` block for inline assembly |

## **7. Interpreting and Running Code**

### **Compilable and Non-Compilable Nature**
AngloScript’s unique flexibility allows it to be executed in two primary modes:
1. **Compiled Mode**:  
   Code is compiled into a standalone executable binary, enabling faster execution. This is ideal for systems that require performance or standalone applications.  
   
2. **Non-Compiled Mode**:  
   The code is dynamically interpreted at runtime. This is particularly useful for prototyping or running scripts in environments like web browsers, Python, or embedded systems.  

### **JIT Compatibility**
AngloScript can leverage **Just-In-Time (JIT) compilation** to dynamically convert AngloScript code into optimized machine code during execution. This allows a balance between the flexibility of interpretation and the performance of compilation.

## **8. Advanced Features Explained**

### **1. Event-Driven Programming**
- Events can be declared and listened to using `rune event`.  
- Example:
  ```angloscript
  rune OnClick event {
      does trigger() {
          write "Button clicked!";
      }
  }
  ```

### **2. Multi-Threading and Asynchronous Processing**
- The `async` keyword enables concurrent tasks.
  ```angloscript
  does fetchData() async {
      write "Fetching data...";
      wait 2 seconds;
      write "Data fetched!";
  }
  ```

## **9. Example Code**

A simple program that prints numbers and handles user input:

```angloscript
rune MyGame class {
    has score = 0;
    
    does start() {
        write "Game Start!";
        mark x = 10;
        loop mark i = 1 to x {
            write "Loop " + i;
        }
        does play();
    }
    
    does play() {
        write "Playing...";
        score = score + 10;
        write "Score: " + score;
    }
}
```

## **10. Features from Holy C, Python, and BASIC**

### **From Holy C**
- Inline assembly for low-level operations.
- Direct manipulation of system memory and registers.
- Minimalistic and optimized execution.

### **From Python**
- Dynamic typing and duck typing.
- Clean and readable syntax.
- Support for high-level data structures and functional programming.

### **From BASIC**
- Natural language-like keywords and structure.
- Simple control flow constructs (`if`, `loop`).  
- Built-in support for beginner-friendly programming.

## **11. AngloScript’s Unique Flexibility**

AngloScript’s **universally mappable syntax** ensures its ability to run on virtually any system. Its design prioritizes **ease of use** while allowing developers to:
- Write simple scripts for educational purposes.  
- Develop complex applications with system-level capabilities.  
- Interact seamlessly with existing codebases in Python, JavaScript, or Assembly.  

**Key Benefits**:
- **Adaptability**: Mapable to any language.
- **Cross-Platform**: Runs on both high- and low-level systems.
- **Universal Application**: Ideal for web, desktop, mobile, and embedded systems.

## **12. Future Directions**

- **Expanded Documentation**: Further detail on advanced features.
- **Better Performance**: For large-scale projects and mobile/web integration.
- **Cross-Platform Support**: Expansion to web and mobile platforms.

---

**End of Documentation.**
