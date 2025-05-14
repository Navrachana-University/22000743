# Hinglish Compiler

A simple compiler for a custom programming language called **Hinglish**, developed using **Flex** and **Bison** as part of the *Compiler Design Laboratory (CSE605)* course at Navrachana University.

## 🔤 What is Hinglish?

**Hinglish** is a beginner-friendly programming language that uses Hindi-inspired keywords. It supports fundamental programming constructs, including:

- Variable assignments
- Arithmetic operations
- Conditional statements (`if-else`)
- Loops (`while`)
- Output statements

### 🧾 Example Hinglish Code
```hinglish
shuru
sum = 0;
i = 1;
jabtak (i <= 3) {
    sum = sum + i;
    i = i + 1;
}
bolo sum;
```

## ⚙️ How It Works

The Hinglish compiler processes code through the following stages:

1. **Lexical Analysis (Flex)**  
   - Tokenizes Hinglish keywords (e.g., `shuru`, `bolo`, `agar`, `jabtak`).  
   - Identifies operators, numbers, and identifiers.

2. **Parsing & TAC Generation (Bison)**  
   - Parses tokenized code according to defined grammar rules.  
   - Generates **Three-Address Code (TAC)** using temporary variables and labels.

3. **Input/Output Handling**  
   - Reads Hinglish source code from `input.txt`.  
   - Outputs the generated TAC to `output.txt`.

### 📋 Sample TAC Output
```
sum = 0
i = 1
L1:
t1 = i <= 3
if t1 goto L2
goto L3
L2:
t2 = sum + i
sum = t2
t3 = i + 1
i = t3
goto L1
L3:
print sum

```

## 🧪 Test Case Highlights

The compiler supports:

- Arithmetic and logical expressions
- `if-else` conditional blocks
- `while` loops using `jabtak`
- Output statements using `bolo`

## 🚀 How to Run

### ✅ Prerequisites
- Install **Flex** and **Bison** on your system.
- Ensure a C compiler (e.g., `gcc`) is available.

### 🛠️ Compilation Steps
1. Run the following commands to generate the compiler:
   ```bash
   flex lex.l
   bison -d yacc.y
   gcc lex.yy.c yacc.tab.c -o compiler
   ```
2. Place your Hinglish source code in a file named `input.txt`.
3. Run the compiler:
   ```bash
   ./compiler
   ```
4. The generated **Three-Address Code** will be written to `output.txt`.

### 💡 Alternative Compilation
Compile and run using:
```bash
gcc lex.yy.c yacc.tab.c
./a.out
```

## 📁 Project Files

| File         | Description                              |
|--------------|------------------------------------------|
| `lex.l`      | Lexical analyzer (Flex)                  |
| `yacc.y`     | Parser and TAC generator (Bison)         |
| `input.txt`  | Sample Hinglish program                  |
| `output.txt` | Generated Three-Address Code             |

## 👨‍💻 Authors

- **Nirav Lad** (22000743)

**Course In-Charge**: Prof. Vaibhavi Patel  
**Institution**: Navrachana University  
**Semester**: Spring 2024–25
