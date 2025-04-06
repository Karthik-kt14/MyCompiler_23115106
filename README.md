# MyCompiler_23115106



```markdown
# ⚙️ Arithmetic Expression Compiler (Flex + Bison + C++)

This project is a simple arithmetic compiler that parses algebraic expressions and generates:

- ✅ Three Address Code (TAC)
- 🔁 Optimized Instructions
- 🖥️ Register-Based Assembly Code

Built using **Flex**, **Bison**, and **C++**, this project showcases basic compiler design, optimization techniques, and code generation.

---

## 🧠 Sample Expression

```c
x = (a + b) * (c - d) + (a + b);
```

---

## ✅ Example Output

| Section | Output |
|--------|--------|
| **Input** | `x = (a + b) * (c - d) + (a + b);` |
| **Three Address Code** | `t1 = a + b`<br>`t2 = c - d`<br>`t3 = t1 * t2`<br>`t4 = a + b`<br>`t5 = t3 + t4`<br>`x = t5` |
| **Optimized Instructions** | `t1 = a + b`<br>`t2 = c - d`<br>`t3 = t1 * t2`<br>`t4 = t3 + t1`<br>`x = t4` |
| **Assembly Code** | `MOV R1, a`<br>`ADD R1, b`<br>`MOV R2, R1`<br>`MOV R3, c`<br>`SUB R3, d`<br>`MUL R4, R2, R3`<br>`ADD R5, R4, R2`<br>`STORE x, R5` |

---

## ▶️ How to Run

1. **Build the project** using:

```bash
make
```

2. **Run the compiler**:

```bash
./compiler
```

3. **Enter your expression** (remember the `;` at the end):

```c
x = (a + b) * (c - d) + (a + b);
```

---

## 📁 Project Structure

```
.
├── calc.l         # Lexer (Flex)
├── calc.y         # Parser (Bison) + Code Generator
├── main.cpp       # Entry point (optional, if used)
├── Makefile       # Build script
├── output.asm     # Final Assembly Output
├── compiler       # Final executable
└── README.md      # You're here!
```

---

## 🧠 Optimizations Applied

| Optimization | Description |
|--------------|-------------|
| **Common Subexpression Elimination** | `a + b` is computed once and reused |
| **Reduced Temporary Usage** | Removed redundant temporaries (like `t4`) |
| **Direct Register Reuse** | Registers used to hold intermediate values and reused across instructions |

---

## 📸 Screenshots
![Running Example](C:\Users\Karthik Teja\OneDrive\圖片\Screenshots\Screenshot 2025-04-06 162105.png)


The above are the two examples
---
---

## 📜 License

MIT License – use, learn, modify, and build on top of it!
```

---

Let me know if you want me to:

- Export this `README.md` as a file
- Add `.gitignore` or `output.asm` examples
- Help you generate the screenshot images with mock content

You’re all set to push this to GitHub! 🚀
