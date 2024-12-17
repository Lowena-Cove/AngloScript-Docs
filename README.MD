### AngloScript Documentation

**Version 1.1**

---

### Table of Contents:

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
9. **Future Directions**

---

### 1. Overview

AngloScript is a high-level programming language designed for ease of use, particularly for beginners transitioning from BASIC or Scratch. It combines elements from various programming languages, including **Holy C**, **Python**, **C#**, and **GameMaker Language**, while incorporating a unique Anglo-Saxon theme. The language aims to be modular, intuitive, and accessible, making it suitable for educational purposes and game development.

---

### 2. Key Features

- **Simplicity**: Uses English-based keywords and a straightforward syntax.
- **Modularity**: Supports classes (runes), modules, and functions for organized code.
- **Event-Driven**: Built-in support for event handling, inspired by Scratch and GameMaker.
- **Dynamic Typing**: Variables are dynamically typed, allowing for flexibility.
- **Error Handling**: Provides mechanisms for handling exceptions gracefully.
- **External Code Integration**: Allows embedding of **Assembly**, **JavaScript**, and **Lua** code.

---

### 3. Syntax

#### 1. **Basic Program Structure**

```angloscript
rune MyRune class {
    does main() {
        write "Hello, World!";
    }
}
```

#### 2. **Comments**

- **Single-line**: 
```angloscript
# This is a comment
```
- **Multi-line**:
```angloscript
## This is a multi-line comment. ##
```

#### 3. **Declarations**

- **Mutable Variable**:
```angloscript
mark x = 10;  # Number
```
- **Immutable Constant**:
```angloscript
bind Pi = 3.14159;
```

#### 4. **Data Types**

- **Basic Types**:
    - `number` (e.g., 10, 3.14)
    - `text` (e.g., "Hello World")
    - `boolean` (e.g., `True`, `False`)
    - `list` (e.g., `[1, 2, 3]`)
    - `map` (e.g., `{"key": "value"}`)

#### 5. **Control Flow**

- **Conditionals**:
```angloscript
if x > 10 then write "Big!";
elif x == 10 then write "Exactly!";
else write "Small!";
```

- **Loops**:
  - **For Loop**:
  ```angloscript
  loop mark i = 1 to 10 { write i; }
  ```
  - **While Loop**:
  ```angloscript
  while x > 0 { write x; x = x - 1; }
  ```

#### 6. **Functions**

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

#### 7. **Classes and Runes**

- **Class Declaration**:
```angloscript
rune Player class {
    has health = 100;
    does heal(amount) {
        health = health + amount;
    }
}
```

- **Inheritance**:
```angloscript
rune NPC class > Player {
    has dialogue = "Hello!";
    does speak() {
        write dialogue;
    }
}
```

#### 8. **Modules**

- **Module Declaration**:
```angloscript
rune Math module {
    does add(a, b) {
        give a + b;
    }
}
```

- **Usage**:
```angloscript
mark result = Math.add(2, 3);
```

#### 9. **Input/Output**

- **Writing to Console**:
```angloscript
write "Hello!";
```

- **Reading Input**:
```angloscript
mark name = ask "What is your name?";
write "Hello, " + name;
```

#### 10. **Error Handling**

- **Try-Catch**:
```angloscript
try {
    mark x = 10 / 0;
} catch Error {
    write "Something went wrong!";
}
```

#### 11. **External Code Integration**

- **Embedding Assembly**:
```angloscript
asm {
    mov eax, 10;
}
```

- **Embedding JavaScript**:
```angloscript
js {
    console.log("Hello from JS!");
}
```

- **Embedding Lua**:
```angloscript
lua {
    print("Hello from Lua!");
}
```

#### 12. **Built-in Modules**

- **Math Module**:
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

- **String Module**:
```angloscript
rune String module {
    does length(text) { give len(text); }
    does upper(text) { give text.upper(); }
    does lower(text) { give text.lower(); }
    does contains(text, sub) { give sub in text; }
}
```

- **System Module**:
```angloscript
rune System module {
    does exit(code) { sys_exit(code); }
    does time() { give sys_time(); }
}
```

- **File Module**:
```angloscript
rune File module {
    does read(path) {
        give file_read(path);
    }
    does write(path, content) {
        file_write(path, content);
    }
}
```

---

### 4. **Keywords Reference**

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

### 5. **Module Types**

| AngloScript Module Type | Purpose | Assembly Equivalent | Python Equivalent |
|--------------------------|---------|---------------------|-------------------|
| rune [class]             | Defines a class with properties and methods. | `.data section for variables, .text for methods.` | `class MyClass:` |
| rune [module]            | Declares a module for reusable functions. | `.text section for function logic.` | `class ModuleName: with @staticmethod` |
| rune [interface]         | Defines a shared behavior structure. | None directly. Similar to jump tables. | Abstract base class with abc module. |
| rune [event]             | Event listener for handling triggers. | None directly. Implemented as callbacks. | `def event_handler(event):` |

---

### 6. **AngloScript and Other Languages**

| AngloScript                          | Python                           | Assembly (x86)                    |
|--------------------------------------|----------------------------------|-----------------------------------|
| `mark x = 5`                         | `x = 5`                          | `mov eax, 5`                      |
| `write "Hello, World!"`              | `print("Hello, World!")`         | `mov eax, "Hello, World!"`        |
| `rune greet(name) { ... }`           | `def greet(name): ...`           | `greet: ...`                      |
| `if x > y then ... else ... end`      | `if x > y: ... else: ...`        | `cmp eax, ebx`                    |
| `for i = 1 to 10 do ... end`          | `for i in range(1, 11): ...`     | `mov ecx, 10`                    |

---

### 7. **Interpreting and Running Code**

To run AngloScript code, it can be executed in an interpreter that reads the script line by line and processes each command. This can be done through an integrated IDE or terminal-based interface.

- **IDE Usage**: Users can type commands into an editor, then run the code and see the output printed to the console.
- **Terminal Usage**: Users can directly input commands or write scripts and execute them in the terminal.

---

### 8. **Example Code**

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
for i

 = 1 to 5 do
    write i
end
```

---

### 9. **Future Directions**

Future updates will include expanded documentation, additional built-in libraries, and support for more languages and platforms. New features such as better error handling, more powerful modules, and performance optimizations are also planned.

---

End of Documentation.
