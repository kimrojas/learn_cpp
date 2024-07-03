# Introduction / Getting Started

## 0.1 — Introduction to these tutorials

> Programming can be a lot of fun, and if you’re not generally having fun, you’re not in the right mindset to be programming. Tired or unhappy programmers make mistakes, and debugging code tends to take much longer than writing it correctly in the first place!

## 0.2 — Introduction to programming languages

### Machine language

Computers understand instruction set (not coding language, c++ or fortran). 

These instruction set are composed of sequences of bits (1s and 0s).

Instruction set length is dependent on the system type (x32 or x86/x64)

Different computers have different instruction set, meaning programs made for each system are not portable. 

### Assembly language

Each instruction is identified by short abbreviations instead of bits.

These abbreviation are translated back to machine language using an `assembler`. 

Its fast but tend to need lots of code for simple tasks.

Still not portable. 

### High-level languages

Fixes the portability problem.

Examples are C, C++, Pascal etc.

A `compiler` is a program that translates source code (written in high-level language) to another language (low-level language like assembly or machine language). These new set of files are compiled into an `executable` that can be distrubuted or run without the compiler.

An `interpreter` does not need to pass by the compilation step. 

Two exception to portability:

1. plaform-spepcific features 
2. compiler-specific features

## 0.3 — Introduction to C/C++

Long history

Philosophy of C/C++:

- trust the programmer

What are C++ good at?

- Video games
- Real-time systems (e.g. transportation, manufacturing, etc.)
- High-performance financial applications (e.g. high frequency trading)
- Graphical applications
- embedded software
- Audio and video processing
- AI and NN

## 0.4 — Introduction to C++ development

### 1. Define the problem 

"I want to write a program that will allow me to enter many numbers, then calculate the average."

### 2. Determine how you're going to solve the problem

A good solution

- straightforward (not overly complicated)
- well documented
- built modularly
- robust and can recover useful error messages in unexpected incidents

### 3. write the program

extension will be `.cpp` that indicates that the file is a C++ source file.

Use a code editor for writing code due to the following reasons

1. Line numbering
2. Syntax highlighting 
3. fixed-width font

## 0.5 — Introduction to the compiler, linker, and libraries

### 4. Compiling your source code

C++ sequentially goes though the source code

It has two task:

1. Check code to make sure rules are followed (and show error message)
2. Translates source code to machine language. This translation is saved in an **object file** (extension = `.o` or `.obj`). Filename will be the same (`test.cpp` > `test.o`)

### 5. Linking object files and libraries

After the `compiler` the `linker` will combine all objects and produce the output file (typically the executable)

Linking steps:

1. Check object file/s validity
2. Validates cross-file dependencies. Error leads to linker errors. 
3. Also links necessary library files (collection of standard pre-compiled codes)

C++ comes with **C++ standard library**

#### Building

**Building** = refers to the full process of converting source code to executable

Some build automations used in more complex projects are `make`, `cmake`, and `build2`. 

### 6 & 7. Testing and debugging

#### Integrated development environment (IDEs)

An IDE bundles the editor, compiler, linker, and debugger. 

It makes it easy to develop, build and debug your programs.





