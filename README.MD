# **AngloScript Documentation**

**Version 1.3**  
**Author:** AngloScript Development Team  
**Last Updated:** December 2024  

---

## **Table of Contents**

1. Overview  
2. Key Features  
3. Syntax  
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
4. Keywords Reference  
5. Module Types  
6. AngloScript and Other Languages  
   - Comparison to Python  
   - Comparison to Assembly  
   - Comparison to BASIC  
7. Interpreting and Running Code  
   - Compilable and Non-Compilable Nature  
   - JIT Compatibility  
8. Advanced Features Explained  
   - Event-Driven Programming  
   - Cross-Language Translatability  
   - Dynamic Typing and Type Inference  
   - Error Handling with Built-in Retry Logic  
   - Multi-Threading and Asynchronous Processing  
   - Inline Scripting and Embedded Code Blocks  
   - Data Structures: Lists, Maps, and Trees  
   - Built-in Game Development Tools  
   - Advanced String Manipulation  
   - System-Level Programming Features  
9. Example Code  
10. Features from Holy C, Python, and BASIC  
11. AngloScript’s Unique Flexibility  
12. Future Directions  

---

## **1. Overview**

AngloScript is a high-level programming language built with the vision of balancing simplicity and power. It draws inspiration from **Holy C**, **Python**, **C#**, **BASIC**, and **Scratch-style programming concepts**, while delivering a unique set of features that make it universally translatable and adaptable.  

AngloScript stands out due to its ability to operate in **compilable**, **non-compilable**, **JIT-based**, or even **interpreted environments**. Its flexibility means it can seamlessly translate or map its syntax into virtually any other language. This design allows AngloScript to run on platforms ranging from bare-metal systems (via low-level Assembly integration) to high-level scripting platforms like Python or Lua.

---

## **2. Key Features**

### **1. Simplicity**
- The language is as simple as writing natural English. 
- Uses clear, self-explanatory keywords (e.g., `mark` for variables, `write` for printing, `does` for function declaration).  
- Its straightforward syntax ensures a minimal learning curve, even for children.

### **2. Modularity**
- Code is structured into **runes** (classes, modules, events, or interfaces).  
- Modules enable reusable, organized codebases for complex programs.

### **3. Event-Driven Programming**
- Built-in event listeners handle triggers for interactivity.  
- Modeled after the event-based logic found in Scratch and GameMaker.  

### **4. Dynamic Typing**
- Variables automatically adapt to their assigned values, reducing the need for explicit type declarations.

### **5. Error Handling**
- AngloScript introduces **try-catch blocks** with built-in retry mechanisms.  
- Errors are gracefully handled, and optional fallback behaviors can be defined.

### **6. External Code Integration**
- Inline **Assembly**, **JavaScript**, and **Lua** can be embedded directly into AngloScript programs.  
- This makes AngloScript extensible and capable of interacting with system-level operations or external libraries.

### **7. Cross-Language Translatability**
- AngloScript can be translated into any other language, including Python, C#, Lua, Assembly, and more.  
- This feature ensures that programs written in AngloScript can run in nearly any environment.  

### **8. Compilation and Execution Modes**
- AngloScript can be:  
  - **Compiled** into standalone binaries.  
  - **JIT-compiled** for improved runtime performance.  
  - **Interpreted** dynamically by host environments that support basic scripting languages.  

### **9. Built-in Game Development Tools**
- Event-driven logic, game loops, and asset management systems are integrated.  
- These tools make it easy to create games without needing additional frameworks.  

### **10. Data Structure Support**
- Native support for **lists**, **maps**, **queues**, **stacks**, and **binary trees**.  
- Built-in methods simplify data manipulation.  

### **11. System-Level Programming**
- Developers can access low-level system operations, including memory manipulation, via inline Assembly.  
- System modules provide OS-level functionality like file I/O, threading, and networking.  

---

## **3. Syntax**

### **1. Basic Program Structure**

```angloscript
rune Main class {
    does main() {
        write "Hello, World!";
    }
}
```

### **2. Comments**
- Single-line comments:  
  ```angloscript
  # This is a comment
  ```
- Multi-line comments:  
  ```angloscript
  ## This is a
     multi-line comment ##
  ```

### **3. Variable Declarations**
- **Mutable Variables** (`mark`):  
  ```angloscript
  mark score = 0;
  ```
- **Immutable Constants** (`bind`):  
  ```angloscript
  bind Pi = 3.14159;
  ```

### **4. Control Flow**
- **If Statements**:
  ```angloscript
  if x > 5 then
      write "x is greater than 5";
  elif x == 5 then
      write "x equals 5";
  else
      write "x is less than 5";
  ```

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

---

## **7. Interpreting and Running Code**

### **Compilable and Non-Compilable Nature**
AngloScript’s unique flexibility allows it to be executed in two primary modes:
1. **Compiled Mode**:  
   Code is compiled into a standalone executable binary, enabling faster execution. This is ideal for systems that require performance or standalone applications.
   
2. **Non-Compiled Mode**:  
   The code is dynamically interpreted at runtime. This is particularly useful for prototyping or running scripts in environments like web browsers, Python, or embedded systems.  

### **JIT Compatibility**
AngloScript can leverage **Just-In-Time (JIT) compilation** to dynamically convert AngloScript code into optimized machine code during execution. This allows a balance between the flexibility of interpretation and the performance of compilation.

---

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

---

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

---

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

AngloScript is designed to evolve as a **modular**, **multi-platform**, and **beginner-friendly** programming language while introducing new innovations to meet the demands of both novice and advanced programmers. The future roadmap includes the following planned features and advancements:  

### **1. Visual Programming Integration**
- Develop a visual programming IDE with a block-based editor inspired by Scratch, allowing users to write AngloScript code by assembling logic visually.  
- Support bidirectional conversion between visual and text-based code.

### **2. AI-Assisted Code Generation**
- Integrate AI to provide real-time suggestions, debugging tips, and automated code generation, helping beginners create complex programs effortlessly.  
- AI will analyze code contextually to ensure syntax correctness and logic flow.

### **3. AngloScript WebAssembly (WASM)**
- Compile AngloScript directly to WebAssembly for high-performance web applications.  
- Extend the runtime to allow seamless integration with JavaScript and HTML5.

### **4. Advanced Game Development Framework**
- Expand the built-in game development tools to include:
  - **Physics engine** for real-time simulations.  
  - **Animation tools** for character movement.  
  - **Asset pipeline** for importing and managing textures, sounds, and 3D models.  

### **5. Native Multi-Language Support**
- Enhance the language’s translation engine to support live conversion of AngloScript code into:
  - **C++** for performance-critical applications.  
  - **Ruby** and **PHP** for web development.  
  - **Rust** for secure system-level programming.  

### **6. Distributed Computing and Networking**
- Introduce native constructs for distributed computing:
  - `node` for defining cluster nodes.  
  - `message` for inter-node communication.  
  - `net` for creating client-server models.  

### **7. Embedded Systems Support**
- Optimize the interpreter and runtime for low-resource environments like microcontrollers and IoT devices.  
- Introduce `hardware` modules for direct access to GPIO pins, sensors, and actuators.

### **8. Custom Compiler Toolchain**
- Expand the compiler to allow developers to customize the compilation process.  
- Add support for intermediate bytecode representations for portability across different architectures.

### **9. Full Unicode Support**
- Add native Unicode support for text processing, enabling AngloScript to handle internationalization and localization seamlessly.

### **10. Education-Focused Features**
- Develop beginner-friendly IDE tutorials and interactive lessons.  
- Include gamified programming challenges to teach concepts such as recursion, sorting algorithms, and data structures.

### **11. Community-Driven Extensions**
- Launch a plugin marketplace where developers can share and integrate community-built modules.  
- Create a versioning system for third-party packages to ensure compatibility and reliability.

### **12. Advanced AI and Machine Learning Libraries**
- Incorporate native support for AI/ML libraries like TensorFlow or PyTorch.  
- Add pre-built modules for data preprocessing, neural network training, and deployment.

### **13. Quantum Computing Framework**
- Research and develop a quantum simulation module to allow experimentation with quantum logic gates and algorithms.  

---

## **Conclusion**

AngloScript is not only a language but a vision for the future of programming. Its simplicity enables accessibility for beginners, while its modularity and flexibility open doors for advanced applications. With its ambitious roadmap, AngloScript aims to become a universal programming standard, blending the best features of existing languages while innovating in new domains.  

Whether you’re a child writing your first line of code or an experienced developer building high-performance applications, AngloScript is your gateway to a world of possibilities.  

---

**End of Documentation.**
