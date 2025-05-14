Hinglish Compiler
A simple compiler for a custom programming language called Hinglish, built using Flex and Bison as part of the Compiler Design Laboratory (CSE605) course.

🔤 What is Hinglish?
Hinglish is a beginner-friendly programming language that uses Hindi-inspired keywords. It supports basic programming constructs such as:

Assignments

Arithmetic operations

Conditionals (if-else)

Loops (while)

Output statements

Example syntax:

shuru
sum = 0;
i = 1;
jabtak (i <= 3) {
    sum = sum + i;
    i = i + 1;
}
bolo sum;
⚙️ How It Works
The compiler performs the following steps:

Lexical Analysis using Flex

Tokenizes keywords like shuru, bolo, agar, jabtak, etc.

Recognizes operators, numbers, and identifiers.

Parsing & TAC Generation using Bison

Uses grammar rules to validate syntax.

Generates Three-Address Code (TAC).

Input/Output Handling

Reads code from input.txt

Outputs TAC to output.txt

Example TAC:

makefile
Copy
Edit
t1 = 20
x = t1
t2 = 5
y = t2
...
print sum
🧪 Test Case Highlights
Supported features in a single example:

Arithmetic and logical expressions

if-else conditions

while loop

Output using bolo

🚀 How to Run
Install Flex and Bison on your system.

Compile the code:

flex lex.l
bison -d yacc.y
gcc lex.yy.c yacc.tab.c -o compiler
Create a file input.txt with your Hinglish code.

Run the compiler:

./compiler
See the output TAC in output.txt.

Or you can just simply type:
gcc lex.yy.c yacc.tab.c
It will create a default named file a.exe
Run the compiler:

./compiler
See the output TAC in output.txt.

📁 Files
lex.l – Lexical analyzer (Flex)

yacc.y – Parser and TAC generator (Bison)

input.txt – Sample Hinglish program

output.txt – Generated Three-Address Code

👨‍💻 Authors
Nirav Lad (22000743)

Supervised by Prof. Vaibhavi Patel
Navrachana University, Spring Semester 2024-25




[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/bPoO8GTw)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=19516090&assignment_repo_type=AssignmentRepo)
