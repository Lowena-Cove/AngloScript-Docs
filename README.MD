# **AngloScript Full Documentation**

**Version 1.2**  
**Author:** AngloScript Development Team  
**Last Updated:** December 2024

---

## Table of Contents:
1. **Overview**
2. **Key Features**
3. **Syntax**
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
4. **Keywords Reference**
5. **Module Types**
6. **AngloScript and Other Languages**
7. **Interpreting and Running Code**
8. **Example Code**
9. **Features from Holy C, Python, C#, and BASIC**
10. **Future Directions**
11. **Detailed Explanation of Core Concepts**

---

## 1. **Overview**

**AngloScript** is a high-level programming language designed to be intuitive and easy to use while also incorporating a wealth of features from powerful languages such as Holy C, Python, C#, BASIC, and Scratch-like systems. It focuses on enabling beginners to write code in simple, English-based syntax while also providing powerful, advanced features under the hood.

What sets AngloScript apart from many other programming languages is its ability to be *interoperable* across different platforms and environments. By leveraging a broad and flexible syntax, the language can be **mapped to any other language**, making it highly adaptable for various use cases and platforms. AngloScript is essentially designed to be **universally translatable**, enabling it to be run in any environment that can handle even the simplest scripting languages. 

This feature makes it incredibly versatile: while it’s simple enough for a child to learn, it’s also capable of complex operations that make it useful for more advanced programming tasks. It’s as easy to use as BASIC or Scratch, but as powerful as Python, C#, or even Assembly when necessary.

---

## 2. **Key Features**

- **Simplicity & Accessibility**: English-based keywords and natural language syntax make it incredibly easy for newcomers to start programming immediately.
- **Universally Mappable Syntax**: The language is designed to be adaptable across different platforms and environments. Any platform capable of running basic code can execute AngloScript.
- **Modular Design**: Supports reusable classes (runes), modules, and functions to help organize complex programs.
- **Event-Driven Programming**: Simplified event handling (inspired by Scratch and GameMaker) makes it easy to create interactive programs.
- **Dynamic Typing**: Variables can change types at runtime for more flexible coding.
- **Error Handling**: Built-in `try-catch` blocks handle runtime errors gracefully.
- **External Code Integration**: Allows embedding of lower-level code such as **Assembly**, **JavaScript**, and **Lua**.
- **Cross-Language Translatability**: AngloScript can be automatically translated or mapped into any other programming language. This feature allows it to run on virtually any platform.
- **Advanced Features for Expert Users**: Inspired by powerful languages like Python and C#, it has support for advanced features like object-oriented programming, lambda functions, LINQ-style queries, asynchronous programming, and more.
- **Game Development Support**: Built-in event handling and modular system make it an ideal language for game development, especially for educational and beginner game creators.

---

## 3. **Syntax**

AngloScript’s syntax is designed to be incredibly intuitive, taking inspiration from various languages to balance simplicity and complexity.

### 1. **Basic Program Structure**

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

### 2. **Comments**

- **Single-line comment**:
```angloscript
# This is a single-line comment
```

- **Multi-line comment**:
```angloscript
## This is a multi-line comment
   that spans across lines ##
```

### 3. **Declarations**

- **Mutable Variable Declaration** (using `mark`):
```angloscript
mark x = 10;  # Declares a mutable variable x
```

- **Immutable Constant Declaration** (using `bind`):
```angloscript
bind Pi = 3.14159;  # Declares a constant Pi
```

### 4. **Data Types**

- **number**: Integer or floating point.
- **text**: String of characters enclosed in quotation marks.
- **boolean**: Boolean value (`True` or `False`).
- **list**: Ordered collection, similar to arrays.
- **map**: Unordered collection of key-value pairs (similar to dictionaries in Python).
- **function**: A function itself can be a variable.

### 5. **Control Flow**

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

### 6. **Functions**

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

### 7. **Classes and Runes**

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

### 8. **Modules**

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

### 9. **Input/Output**

- **Writing to the Console**:

```angloscript
write "Hello!";
```

- **Reading User Input**:

```angloscript
mark name = ask "What is your name?";
write "Hello, " + name;
```

### 10. **Error Handling**

- **Try-Catch**:

```angloscript
try {
    mark x = 10 / 0;
} catch Error {
    write "Something went wrong!";
}
```

### 11. **External Code Integration**

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

### 12. **Built-in Modules**

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

---

## 4. **Keywords Reference**

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

---

## 5. **Module Types**

| AngloScript Module Type | Purpose | Assembly Equivalent | Python Equivalent |
|--------------------------|---------|---------------------|-------------------|
| rune [class]             | Defines a class with properties and methods. | `.data section for variables, .text for methods.` | `class MyClass:` |
| rune [module]            | Declares a module for reusable functions. | `.text section for function logic.` | `class ModuleName: with @staticmethod` |
| rune [interface]         | Defines a shared behavior structure. | None directly. Similar to jump tables. | Abstract base class with abc module. |
| rune [event]             | Event listener for handling triggers. | None directly. Implemented as callbacks. | `def event_handler(event):` |

---

## 6. **AngloScript and Other Languages**

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
| Constants |

 `dw CONSTANT` | `bind CONSTANT = value` |
| Functions | Labels and `call` instructions | `does` keyword for function declaration |
| Classes/Modules | Data sections for variables, Text sections for methods | `rune` defines classes, modules |
| Inline Assembly | Direct inline assembly code | `asm {}` block for inline assembly |

---

## 7. **Interpreting and Running Code**

AngloScript can be interpreted by an environment that understands basic programming instructions. Due to its *universally mappable syntax*, any platform capable of executing basic code can run AngloScript, making it highly adaptable across different systems.

---

## 8. **Example Code**

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

---

## 9. **Features from Holy C, Python, C#, and BASIC**

- **Object-Oriented Programming**: Classes (`rune`) and inheritance (`>` operator).
- **Error Handling**: `try-catch` blocks (similar to Python and C#).
- **Dynamic Typing**: Variables can change types during runtime.
- **Event Handling**: Simplified syntax for events (inspired by Scratch/Blockly).
- **Interoperability**: External code integration for Assembly, JavaScript, and Lua.

---

## 10. **Future Directions**

- **Expanded Documentation**: Further detail on advanced features.
- **Better Performance**: For large-scale projects and mobile/web integration.
- **Cross-Platform Support**: Expansion to web and mobile platforms.

---

**End of Documentation.**
