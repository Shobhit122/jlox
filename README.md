# My jlox Interpreter

This repository contains my personal implementation of the jlox interpreter, as described in Robert Nystrom's excellent book, "Crafting Interpreters." This project is built using Maven for dependency management and project structure.

## About

This project is a learning exercise, and I've aimed to follow the book's guidance while adding my own touches and understanding to the process. The jlox interpreter is a tree-walk interpreter written in Java, designed to execute programs written in the Lox language.

## Features

* **Lexical Analysis (Scanning):** Converts source code into a stream of tokens.
* **Syntactic Analysis (Parsing):** Builds an abstract syntax tree (AST) from the tokens.
* **Semantic Analysis (Interpretation):** Traverses the AST to execute the Lox program.
* **Expression Evaluation:** Handles various Lox expressions, including arithmetic, logical, and comparison.
* **Variable Scoping:** Implements proper variable scoping and environment management.
* **Function Calls:** Supports user-defined functions and function calls.
* **Error Handling:** Provides informative error messages for scanning, parsing, and runtime errors.

## Getting Started

### Prerequisites

* Java Development Kit (JDK) 8 or later.
* Maven.
* Git (optional, for cloning the repository).

### Installation

1.  **Clone the repository:**

    ```bash
    git clone <repository_url>
    cd <repository_name>
    ```

2.  **Build the project using Maven:**

    ```bash
    mvn clean install
    ```

    This command will download dependencies, compile the code, and create a JAR file in the `target` directory.

### Running the Interpreter

1.  **Run from the command line:**

    ```bash
    java -cp target/jlox-tree-walk-interpreter-1.0-SNAPSHOT.jar com.shobhit.java.lox.Lox <path_to_lox_file>
    ```

2.  **Run in interactive mode (REPL):**

    ```bash
    java -cp target/jlox-tree-walk-interpreter-1.0-SNAPSHOT.jar com.shobhit.java.lox.Lox
    ```

    This will start the interpreter in interactive mode, allowing you to enter Lox code directly.

## Example Lox Code

```lox
// Example Lox code
var a = 10;
var b = 20;

print a + b;

fun add(x, y) {
  return x + y;
}

print add(a, b);

