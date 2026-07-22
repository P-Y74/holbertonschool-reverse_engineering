# Static Analysis in Reverse Engineering

## Disclaimer

This project was completed for educational purposes as part of the Holberton School cybersecurity curriculum.

All binaries were provided for authorized analysis and examined locally in a controlled virtual machine or sandbox. No online analysis services were used.

This repository presents the project scope, methodology, and skills developed without disclosing flags, binary-specific answers, verification values, or complete challenge solutions.

## Description

This project focuses on **static analysis**, a reverse engineering technique used to examine a program without executing it.

Static analysis allows security professionals to extract information from a binary by studying its:

* embedded strings;
* executable structure;
* functions;
* assembly instructions;
* imported libraries;
* control flow;
* mathematical operations;
* validation logic.

The objective is to progressively move from simple binary inspection to deeper analysis of program logic, security weaknesses, decryption routines, obfuscation mechanisms, and raw assembly code.

## Scenario

During a security investigation, analysts may receive an unknown executable without source code or documentation.

Running the file immediately could expose the analysis environment to unnecessary risk. Before execution, the binary must therefore be inspected to determine its structure, possible purpose, dependencies, and potentially suspicious behavior.

This project reproduces that initial investigation process through a series of controlled reverse engineering challenges.

## Educational Context

This project is part of the `holbertonschool-reverse_engineering` repository and follows the introductory `re_fundamentals` project.

While the previous project focused on ELF headers, sections, entry points, and external libraries, this project goes further by examining the internal logic of compiled programs.

The exercises introduce practical techniques relevant to:

* malware triage;
* vulnerability research;
* security auditing;
* incident response;
* binary analysis;
* software debugging;
* CTF challenges;
* exploit research;
* low-level program comprehension.

## Learning Objectives

By completing this project, I developed a stronger understanding of:

* static analysis in reverse engineering;
* the role of static analysis in malware investigation and security auditing;
* string extraction and interpretation;
* disassembly and decompilation;
* executable formats such as ELF, PE, and Mach-O;
* function identification in compiled binaries;
* control flow analysis;
* cross-references between functions, variables, and data;
* vulnerability identification through code inspection;
* mathematical and cryptographic operations in binaries;
* inefficient algorithm recognition and optimization;
* obfuscation and collision-related analysis;
* x86 and x86-64 assembly instructions;
* reconstruction of high-level program logic;
* professional documentation of reverse engineering findings.

## Project Scope

The project consists of five progressively more advanced tasks.

The analysis begins with human-readable strings and continues through:

1. binary reconnaissance;
2. function and vulnerability analysis;
3. decryption algorithm optimization;
4. mathematical obfuscation analysis;
5. raw assembly interpretation.

The target binaries and challenge-specific results are not explained in this README.

## Tasks

### Task 0 - Extracting and Analyzing Strings

The first task introduces string extraction as an initial binary triage technique.

Human-readable strings embedded in a compiled program may reveal valuable information before more advanced analysis begins. These can include:

* error messages;
* file paths;
* function names;
* configuration values;
* URLs and network indicators;
* user prompts;
* debugging information;
* potentially sensitive data.

The objective is to extract the available strings, review them carefully, and identify information that may help explain the binary's purpose or guide further investigation.

Key concepts:

* initial binary reconnaissance;
* string extraction;
* indicator identification;
* contextual interpretation;
* prioritization of further analysis.

Expected file:

```text
0-flag.txt
```

The extracted result is intentionally not disclosed in this documentation.

### Task 1 - Static Analysis of a Security-Critical Program

The second task moves beyond strings and focuses on the internal logic of a compiled C program.

The objective is to analyze the binary's functions, understand its overall behavior, and identify potential security weaknesses.

The analysis requires attention to all relevant code paths because vulnerabilities or sensitive behavior may be located in functions that initially appear unimportant.

Key concepts:

* function identification;
* decompiled code analysis;
* cross-reference inspection;
* insecure memory handling;
* hardcoded sensitive information;
* input validation;
* security-focused code review;
* vulnerability documentation.

Expected file:

```text
1-flag.txt
```

No vulnerable function, sensitive value, or challenge solution is included in this README.

### Task 2 - Optimizing a Decryption Algorithm

The third task focuses on the analysis of a computationally expensive decryption routine.

The objective is to understand the algorithm implemented by the binary, identify inefficient operations, and reproduce the necessary logic in a more efficient form.

This task demonstrates that reverse engineering is not limited to recovering hidden values. It can also be used to understand algorithmic behavior and improve performance.

Key concepts:

* decryption routine analysis;
* mathematical operation identification;
* algorithmic complexity;
* performance bottlenecks;
* modular arithmetic;
* efficient exponentiation;
* implementation validation.

Expected file:

```text
2-flag.txt
```

The optimized implementation, decrypted content, and final result are not documented here.

### Task 3 - Reverse Engineering an Obfuscated Value

The fourth task introduces mathematical obfuscation.

The target binary contains a verification mechanism that transforms input through a series of operations before comparing it with expected values.

The objective is to reconstruct the verification logic and understand how non-reversible transformations and collisions can complicate the recovery of the original input.

Key concepts:

* obfuscated validation logic;
* mathematical transformations;
* collision analysis;
* constrained input recovery;
* verification function analysis;
* search-space reduction;
* result validation.

Expected file:

```text
3-flag.txt
```

The expected value, transformation constants, and verification solution are intentionally omitted.

### Task 4 - Understanding Raw Assembly Code

The final task focuses on reading and interpreting raw assembly instructions.

The objective is to identify key functions, follow data transformations, understand input and output handling, and reconstruct the program's higher-level logic.

This task reinforces the ability to analyze compiled code even when decompilation is incomplete or misleading.

Key concepts:

* x86 and x86-64 assembly;
* registers and operands;
* memory addressing;
* arithmetic and logical instructions;
* comparisons and conditional jumps;
* loops and branches;
* function calls;
* stack usage;
* program logic reconstruction.

Expected file:

```text
4-flag.txt
```

The reconstructed logic and final output are not published in this README.

## Tools and Environment

The project uses local reverse engineering tools such as:

* Ghidra
* IDA Pro
* Radare2
* Cutter
* Binary Ninja
* Hex-Rays Decompiler
* Binwalk
* Strings
* GNU Debugger (`gdb`)
* GNU `objdump`
* Hex editors
* x86 and x86-64 instruction references

Not every tool is required for every task. Different tools may be used to compare results and confirm interpretations.

## Repository Structure

```text
static_analysis/
├── README.md
├── 0-flag.txt
├── 1-flag.txt
├── 2-flag.txt
├── 3-flag.txt
└── 4-flag.txt
```

The target binaries are provided separately as part of the authorized training environment or may be stored locally for analysis.

## Static Analysis Workflow

A typical workflow followed during the project includes:

### 1. Preserve and Validate the Binary

Before analysis, the target is stored safely and its integrity is verified to ensure that the file does not change during the investigation.

### 2. Perform Initial Triage

Basic properties are reviewed, including:

* file format;
* architecture;
* embedded strings;
* sections;
* dependencies;
* symbols, when available.

### 3. Load the Binary into an Analysis Tool

A disassembler or decompiler is used to identify functions, data, references, and potential entry points into the program logic.

### 4. Identify Relevant Functions

Functions related to user input, comparisons, cryptographic operations, file access, or memory handling are prioritized.

### 5. Follow Cross-References and Control Flow

References between functions, strings, variables, and code paths are examined to understand how data moves through the program.

### 6. Reconstruct the Program Logic

Assembly and decompiled output are translated into higher-level reasoning, pseudocode, or a local analysis script when necessary.

### 7. Validate the Findings

The interpretation is checked against other parts of the binary and, where authorized by the task, through controlled local verification.

### 8. Document the Analysis

Findings are organized clearly so that the methodology and conclusions can be reviewed and reproduced.

## Static Analysis Techniques

### String Analysis

Embedded text can provide early clues about functionality, error handling, network activity, or sensitive information.

Strings alone do not prove program behavior, but they can help identify areas requiring deeper inspection.

### Disassembly

Disassembly translates machine instructions into assembly language.

It provides a direct representation of the instructions executed by the processor but requires knowledge of registers, memory addressing, calling conventions, and control flow.

### Decompilation

Decompilation attempts to reconstruct higher-level pseudocode from assembly instructions.

The result is easier to read than raw assembly, but it is an approximation rather than the original source code. Variable names, comments, data types, and some structural information are usually lost during compilation.

### Control Flow Analysis

Control Flow Graphs help represent:

* conditional branches;
* loops;
* function exits;
* alternative execution paths;
* error-handling paths.

They make complex program logic easier to follow visually.

### Cross-Reference Analysis

Cross-references connect code and data throughout the binary.

They help determine:

* where a function is called;
* where a string is used;
* which code accesses a variable;
* how data reaches a security-sensitive operation.

### Pattern Recognition

Known patterns can help identify:

* compiler-generated code;
* common library functions;
* unsafe memory operations;
* cryptographic routines;
* encoding or decoding logic;
* input-validation mechanisms;
* obfuscation techniques.

## Security Relevance

Static analysis is relevant to both defensive and offensive cybersecurity roles.

### Defensive Security

Static analysis can support:

* malware triage before execution;
* suspicious binary investigation;
* incident response;
* threat identification;
* extraction of potential indicators of compromise;
* software integrity verification;
* vulnerability assessment;
* secure code auditing without source access.

### Offensive Security

Static analysis can also support:

* vulnerability research;
* attack-surface identification;
* understanding validation mechanisms;
* binary exploitation preparation;
* analysis of protections and mitigations;
* CTF challenge solving;
* exploit behavior analysis.

The exercises in this project were performed exclusively in controlled and authorized environments.

## Skills Demonstrated

* Binary reconnaissance
* Static malware-analysis fundamentals
* String extraction and interpretation
* Disassembly
* Decompilation
* Function identification
* Cross-reference analysis
* Control flow analysis
* Security-focused binary auditing
* Vulnerability recognition
* Algorithm analysis
* Performance optimization
* Mathematical reasoning
* Obfuscation analysis
* x86 and x86-64 assembly comprehension
* High-level logic reconstruction
* Local analysis scripting
* Technical documentation

## Limitations

Static analysis provides valuable information without running the target, but it also has limitations.

Analysis may be complicated by:

* stripped symbols;
* compiler optimizations;
* indirect function calls;
* dynamically generated values;
* encrypted or encoded data;
* packed binaries;
* code obfuscation;
* anti-analysis techniques;
* behavior that only appears at runtime.

For this reason, static analysis is often combined with controlled dynamic analysis in more advanced investigations.

## Documentation Approach

This repository is designed as a professional learning portfolio.

The documentation focuses on:

* the purpose of each exercise;
* the methodology used;
* the technical concepts explored;
* the security relevance of the work;
* the skills demonstrated.

Challenge answers, flags, vulnerable constants, complete algorithms, and directly reusable solutions are intentionally excluded.

## Project Status

Completed as part of the Holberton School cybersecurity curriculum.

## Author

Pierre-Yves
