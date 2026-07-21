# Reverse Engineering

## Disclaimer

This repository was created for educational purposes as part of the Holberton School cybersecurity curriculum.

All exercises are performed in controlled and authorized environments. The content focuses on understanding program behavior, low-level concepts, and defensive security analysis.

No malware, unauthorized software cracking, license bypass techniques, or operational code intended to compromise real systems is provided in this repository.

## Description

This repository contains projects related to **reverse engineering**, binary analysis, assembly language, and low-level program behavior.

The objective is to understand how compiled programs operate internally by examining their instructions, registers, memory usage, control flow, and interactions with the operating system.

The projects combine theoretical concepts with practical exercises performed in controlled laboratory environments.

## Educational Context

This work is part of the Holberton School cybersecurity specialization.

Reverse engineering provides important knowledge for several cybersecurity fields, including:

* malware analysis;
* vulnerability research;
* incident response;
* digital forensics;
* exploit development;
* software debugging;
* threat analysis;
* application security.

The repository documents my progression from fundamental low-level concepts toward more advanced binary analysis techniques.

## Learning Objectives

Through the projects in this repository, I aim to strengthen my understanding of:

* how source code is transformed into machine code;
* how processors execute instructions;
* assembly language syntax and instructions;
* CPU registers and their purposes;
* stack and heap memory organization;
* memory addresses and pointers;
* function calls and calling conventions;
* binary file structure;
* program control flow;
* static and dynamic analysis;
* debugging and disassembly tools;
* security weaknesses visible at the binary level.

## Projects

### [Reverse Engineering Fundamentals](./re_fundamentals)

Introduction to the core concepts required to understand and analyze compiled programs.

Key topics include:

* binary and hexadecimal representations;
* computer architecture fundamentals;
* CPU registers;
* memory organization;
* stack behavior;
* x86-64 assembly instructions;
* operands and addressing modes;
* function calls;
* basic disassembly and debugging concepts.

Additional projects will be added as the reverse engineering learning path progresses.

## Tools and Environment

Depending on the project, the following tools and environments may be used:

* Linux
* Kali Linux
* GCC
* GNU Debugger (`gdb`)
* GDB Enhanced Features (`GEF`)
* GNU Binutils
* `objdump`
* `readelf`
* `strings`
* `file`
* NASM
* x86-64 assembly

Each project directory contains its own README with the specific tools, requirements, and concepts covered.

## Repository Structure

```text
.
├── README.md
└── re_fundamentals
    └── README.md
```

The repository structure may evolve as additional reverse engineering projects are completed.

## Skills Developed

* Low-level program analysis
* Assembly code comprehension
* CPU register analysis
* Stack and memory reasoning
* Binary inspection
* Static analysis fundamentals
* Dynamic analysis fundamentals
* Debugging methodology
* Technical documentation
* Security-oriented analytical thinking

## Security Relevance

Reverse engineering helps security professionals understand what software actually does beyond its source code or documented behavior.

These skills can support both offensive and defensive security activities:

### Offensive Security

* identifying insecure program behavior;
* understanding memory corruption vulnerabilities;
* analyzing execution paths;
* studying binary protections;
* supporting vulnerability research.

### Defensive Security

* analyzing suspicious executables;
* investigating malware behavior;
* identifying indicators of compromise;
* supporting incident response and digital forensics;
* validating software behavior and security controls.

## Documentation Approach

This repository is designed as a professional learning portfolio.

The documentation focuses on:

* explaining technical concepts clearly;
* presenting the methodology used during the exercises;
* demonstrating understanding rather than only providing answers;
* connecting reverse engineering concepts to practical cybersecurity use cases;
* avoiding the publication of sensitive, unsafe, or directly reusable offensive material.

## Project Status

This repository is currently in progress and will be expanded throughout the Holberton School reverse engineering learning path.

## Author

Pierre-Yves
