## Presentation: C++ Interpreter for C-like Code

### Slide 1: Title Slide
**Title:** C++ Interpreter for C-like Code  
**Subtitle:** Handling Arithmetic Operations and Print Statements  
**Presented by:** Rahul Prasad

---

### Slide 2: Introduction
**Objective:**  
Develop a C++ interpreter capable of executing a subset of C-like code, including arithmetic operations and `printf` statements.

**Scope:**  
- Tokenize and parse the input code.
- Evaluate arithmetic expressions.
- Handle variable assignments and `printf` statements.

---

### Slide 3: Overview of the Interpreter

**Components:**
1. **Lexer:** Tokenizes the input code into recognizable components.
2. **Interpreter:** Executes the parsed tokens, performing arithmetic operations and handling `printf` statements.

---

### Slide 4: Lexer Class
**Purpose:**  
The `Lexer` class breaks down the input code into tokens. It identifies keywords, identifiers, numbers, operators, and separators.

**Key Methods:**
- `peek()`: Returns the next character without advancing.
- `advance()`: Moves to the next character.
- `skipWhitespace()`: Skips over whitespace.
- `lexNumber()`: Lexes numeric values.
- `lexIdentifierOrKeyword()`: Lexes identifiers and keywords.
- `lexStringLiteral()`: Lexes string literals.
- `lexCharLiteral()`: Lexes character literals.
- `lexOperatorOrSeparator()`: Lexes operators and separators.

---

### Slide 5: Token Types
**Token Types Include:**
- `KEYWORD`: Reserved words (e.g., `int`).
- `IDENTIFIER`: Variable names (e.g., `a`, `b`).
- `NUMBER`: Numeric values (e.g., `5`, `3.14`).
- `OPERATOR`: Arithmetic operators (e.g., `+`, `*`).
- `SEPARATOR`: Punctuation (e.g., `;`, `,`).
- `STRING_LITERAL`: Text enclosed in quotes (e.g., `"Hello"`).
- `CHAR_LITERAL`: Single character literals (e.g., `'a'`).
- `END`: End of input.

---

### Slide 6: Interpreter Class
**Purpose:**  
The `Interpreter` class processes tokens to execute statements and evaluate expressions.

**Key Methods:**
- `advanceToken()`: Moves to the next token.
- `evaluateTerm()`: Evaluates a term (number or variable).
- `evaluateFactor()`: Handles multiplication, division, and modulo.
- `evaluateExpression()`: Manages addition and subtraction.
- `processAssignment()`: Processes variable assignments.
- `processPrintf()`: Handles `printf` statements.

---

### Slide 7: Handling Arithmetic Operations
**Supported Operations:**
1. **Addition (`+`)**
2. **Subtraction (`-`)**
3. **Multiplication (`*`)**
4. **Division (`/`)**
5. **Modulo (`%`)**

**Example Code:**
```cpp
#include<stdio.h>
int main() 
{
    int a = 10;
    int b = 20;
    int c = a + b;
    printf("sum: %d", c);
    return 0;
}
EOF
```

---

### Slide 8: Handling Print Statements
**Functionality:**
- Outputs formatted strings and variable values.
- Handles strings and numbers, including variables.

**Example Code:**
```cpp
#include<stdio.h>
int main() 
{
    int score = 95;
    printf("Your score: %d", score);
    return 0;
}
EOF
```

**Output:**
```
Your score: 95
```

---

### Slide 9: Handling Variable Declarations and Assignments
**Functionality:**
- Declares and assigns values to variables.
- Stores variable values in a symbol table.

**Example Code:**
```cpp
#include<stdio.h>
int main() 
{
    int a = 15;
    int b = 5;
    int c = a - b;
    printf("difference: %d", c);
    return 0;
}
EOF
```

---

### Slide 10: Error Handling
**Error Scenarios:**
1. **Undefined Variables**: Throws an error if a variable is not defined.
2. **Division by Zero**: Throws an error for division by zero.
3. **Syntax Errors**: Handles unknown tokens and format issues.

**Example Error Message:**
```
Error: Division by zero
```

---

### Slide 11: Example Runs
**1. Addition:**
```cpp
#include<stdio.h>
int main() 
{
    int a = 10;
    int b = 20;
    int c = a + b;
    printf("sum: %d", c);
    return 0;
}
EOF
```
**Output:**
```
sum: 30
```

**2. Multiplication:**
```cpp
#include<stdio.h>
int main()
{
    int a = 5;
    int b = 4;
    int c = a * b;
    printf("product: %d", c);
    return 0;
}
EOF
```
**Output:**
```
product: 20
```

---

### Slide 12: Future Enhancements
**Planned Improvements:**
- Support for more complex expressions and statements.
- Enhanced error handling and debugging features.
- Extending the interpreter to handle additional C++ features.

---

### Slide 13: Conclusion
**Summary:**
- Developed a basic C++ interpreter to handle arithmetic operations and `printf` statements.
- The interpreter supports variable assignments, arithmetic operations, and formatted output.
- Future plans include expanding functionality and improving robustness.

**Thank You!**

---
