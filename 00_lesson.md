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

## 0.7 — Compiling your first program

**Project** is a container that holds all files associated with the thing you're doing (source files, datafiles, etc. )

Instruction of VScode

```
To start a new project, go to the View > Explorer menu (or press Ctrl-Shift-E). This will open the explorer pane. If you haven’t previously opened a project, you should see an Open Folder button in the explorer pane -- press it. If there is already an open project and you want to start a new one, choose File > Open Folder from the top nav.

Inside the dialog that opens, create a new folder named HelloWorld and then select this folder. This folder will be your project folder.

Next, we need to create the file that will contain our source code. Choose File > New File from the top nav, or click the New File icon to the right of HELLOWORLD in the explorer pane.

Name your file main.cpp and add the following contents to it:
```

## 0.8 — A few common C++ problems

https://www.learncpp.com/cpp-tutorial/a-few-common-cpp-problems/

Ask 
1. search engines
2. chatgpt via Bing

## 0.9 — Configuring your compiler: Build configurations

**Build configuration** - settings for how IDE will build the target

**Debug configuration**
- turns off all optimization
- makes the program larger and slower, but easier to debug

**Release configuration** 
- designed for public release
- optimal size and performance 
- useful for testing

For VScode

in tasks.json

Build
- add `"-ggdb"` before `${file}`
  
Release
- add `"-O2"` and `"-DNDEBUG"`  before  `${file}`


## 0.10 — Configuring your compiler: Compiler extensions

Disable compiler extensions since extensions are not compliant with C++ standards.

In VSCODE

- add `"-pedantic-errors"` before `${file}`
- in vscode settings:
  - search (in GUI): "insert final newline"
  - activate checkbox: "Files Insert final Newline"
  
## 0.11 — Configuring your compiler: Warning and error levels


**diagnostic message (diagnostic)** - violation of language rules

**error** when compilation cannot continue due to violation

> Best practice: fix warnings as you encounter it. 

During learning: there are many levels of warnings. Use the maximum to help identify possible issues. 

In VSCODE:

add above `"${file}"`

```
"-Wall",
"-Weffc++",
"-Wextra",
"-Wconversion",
"-Wsign-conversion",
```


### Treating warnings as error

In VSCODE,

add `"-Werror"`

## 0.12 — Configuring your compiler: Choosing a language standard

Typically the default language standard is not the latest version (most default to C++14, which is lacking).

documents target c++17 standard. I'm using c++20 via gcc-10/g++-11

PrintStandard.cpp output:

`Your compiler is using C++20 (language standard code 202002L)`
