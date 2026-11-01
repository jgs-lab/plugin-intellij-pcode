# P-Code VM

![Java 21+](https://img.shields.io/badge/Java-21%2B-blue)
![Version 1.0.2](https://img.shields.io/badge/version-1.0.2-green)
[![JetBrains Marketplace](https://img.shields.io/badge/JetBrains-Marketplace-purple)](https://plugins.jetbrains.com/plugin/31858)

P-Code VM is an educational virtual machine and debugger plugin for IntelliJ IDEA. It helps students explore compiler-generated intermediate code, stack-based execution, method calls, and recursion.

[Install P-Code VM from the JetBrains Marketplace](https://plugins.jetbrains.com/plugin/31858)

## Features

- P-Code syntax highlighting for `.pcode` files
- Execute P-Code programs from the editor
- Step through execution one instruction at a time
- Inspect the operand stack, symbol table, call stack, and runtime frames
- Explore method calls, recursion, and return values

## Preview

![P-Code execution and runtime visualization](screenshots/execution.png)

## Getting Started

1. Install **P-Code VM** from the [JetBrains Marketplace](https://plugins.jetbrains.com/plugin/31858) in IntelliJ IDEA.
2. Create or open a file with the `.pcode` extension.
3. Add a P-Code program, such as the example below.
4. Right-click in the editor and select **Execute P-Code** to run the program, or **Step P-Code** to advance instruction by instruction.
5. Use the **P-Code Console** tool window to inspect execution and runtime state.

The editor actions also have default shortcuts: **F5** for execution and **F10** for stepping. Shortcut availability may depend on your IDE keymap.

## Example: Recursive Factorial

This P-Code program computes the factorial of 5:

```text
factorial-int,method,global,1
n,int,factorial-int,0
#P,label,global,15
#E1,label,global,8
@
STO n,0
LOD n,0
LIT 1,0
OPR 15,0
JMC #E1,false
LIT 1,0
OPR 1,0
LOD n,0
LOD n,0
LIT 1,0
OPR 3,0
CAL factorial-int,0
OPR 4,0
OPR 1,0
LIT 5,0
CAL factorial-int,0
OPR 21,0
OPR 0,0
```

Expected output:

```text
120
```

## Documentation

- [Instruction Set](docs/instruction-set.md) — P-Code instructions and their meaning
- [Runtime Model](docs/runtime-model.md) — How program execution and runtime state work
- [Sample Programs](docs/sample-programs.md) — Additional examples for learning and experimentation

## Educational Use

P-Code VM is intended for compiler construction and programming language courses. It provides a way to observe how intermediate instructions are executed, how calls and returns work, and how recursion affects runtime state.
