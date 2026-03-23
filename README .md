# SPEEK Interpreter

A fully functional interpreter for **SPEEK** (Simple Plain English Execution Kit),  
a simple English-like scripting language — implemented in pure Java.

> "Understanding interpreters is one thing. Building one is another."
---

## What is SPEEK?

SPEEK is a simple scripting language that reads like plain English:

```speek
let value1 be 12
let value2 be 2
let result be value1 / value2 + 3
say result
```

Output:
```
9
```

---

## How the Interpreter Works

The interpreter is a three-stage pipeline:
```
Source Code (.speek file)
↓
[ Tokenizer ] → breaks SPEEK code into tokens
↓
[ Parser ] → builds a structured instruction tree (AST)
↓
[ Evaluator ] → executes the program and produces output
```

---

## 📁 Project Structure
```
src/
├── tokenizer/       
│   → Handles SPEEK keywords (let, be, say, if, is greater than...)

├── expressions/     
│   → Expression tree nodes (Number, String, Variable, BinaryOp)

├── execution/       
│   → Environment + Instruction classes (Assign, Say, If, Repeat)

├── parserlogic/     
│   → Converts tokens into instructions (SPEEK grammar)

├── runner/          
│   → Runs full pipeline (tokenize → parse → execute)

└── SpeekMain.java   
    → Entry point for .speek files

testcases/          
→ .speek sample programs

documentation/      
→ Design explanation (SPEEK rules, tokens, flow)
```

---

## 👥 Team

| Member  | Role                            | Owns                                                      |
| ------- | ------------------------------- | --------------------------------------------------------- |
| Praveen | Tokenizer                       | `tokenizer/`                                              |
| Anandh  | Parser                          | `parserlogic/`                                            |
| Prabhat | Execution, Expressions & Runner | `execution/`, `expressions/`, `runner/`, `SpeekMain.java` |


---

*Sitare University — Advanced OOP in Java — Group Project*