Voici un README prêt à placer dans `re_fundamentals/README.md`.

# Reverse Engineering Fundamentals

## Disclaimer

This project was completed for educational purposes as part of the Holberton School cybersecurity curriculum.

All analyses were performed locally in a controlled environment using authorized binaries provided for the project. No online analysis services were used.

This repository documents the project scope, methodology, and learning objectives without publishing extracted answers, binary-specific findings, or challenge solutions.

## Description

This project introduces the fundamentals of **reverse engineering** through the static analysis of ELF binaries.

The objective is to understand how compiled programs are structured and how security analysts can inspect a binary even when its source code and documentation are unavailable.

The exercises focus on examining executable metadata, identifying binary sections, and determining external dependencies using standard Linux analysis tools.

## Scenario

During a security investigation, an unknown program was discovered running on a company server.

The application had no documentation, and its purpose was unclear. System logs showed unusual activity, but the program did not generate any obvious error or alert.

To understand the potential risk, security analysts needed to inspect the binary structure, identify its dependencies, and look for unusual characteristics that could indicate hidden or suspicious functionality.

This project reproduces the initial stages of that analysis process in a controlled environment.

## Educational Context

This project is part of the Holberton School reverse engineering learning path.

It introduces the low-level concepts and analysis methods required for areas such as:

* malware analysis;
* vulnerability research;
* incident response;
* digital forensics;
* software security testing;
* binary inspection;
* exploit research;
* software compatibility analysis.

The project focuses on static analysis and does not require executing or modifying the target binaries.

## Learning Objectives

By completing this project, I developed a better understanding of:

* reverse engineering in a software security context;
* the structure of compiled executable files;
* the difference between source code, machine code, and assembly;
* ELF headers and their main fields;
* 32-bit and 64-bit binary classifications;
* little-endian and big-endian byte ordering;
* executable entry points;
* binary sections and their roles;
* unusual sections as potential indicators of hidden functionality;
* external and dynamically linked libraries;
* local static analysis methodology;
* binary integrity and safe handling practices.

## Project Scope

The project focuses on analyzing provided ELF binaries using locally installed Linux tools.

The authorized tools for the exercises are:

* `readelf`;
* `objdump`;
* `ldd`.

The analysis includes:

* extracting selected ELF header information;
* enumerating executable sections;
* identifying an unusual section and documenting its size;
* determining an external library required by a binary.

Binary-specific answers and extracted values are intentionally not included in this README.

## Tasks

### Task 0 - Binary Section Analysis

The first task focuses on the ELF header of a provided binary.

The objective is to create an executable Bash script that accepts a file as a command-line argument and extracts selected metadata from its ELF header.

The script must handle both valid and invalid input and display the results using reusable formatting functions.

The analysis covers:

* ELF file identification;
* architecture class;
* byte order;
* program entry point;
* file existence validation;
* ELF format validation;
* formatted command-line output.

Expected file:

```text
get_entry_point.sh
```

### Task 1 - Section Enumeration

The second task focuses on the internal sections of an ELF binary.

The objective is to enumerate the sections, identify one that appears unusual, and determine its size.

This task introduces the role of sections in executable files and demonstrates how section metadata can help reveal added, obfuscated, or unexpected content.

The analysis covers:

* ELF section enumeration;
* section names and attributes;
* section offsets and sizes;
* identification of unusual binary structures;
* documentation of analysis commands and findings.

Expected files:

```text
size.txt
command.txt
```

The extracted section name, size, and analysis command are not documented in this README.

### Task 2 - External Libraries

The third task focuses on external dependencies used by a binary.

The objective is to identify the external library required by the provided target.

This task introduces dynamic linking and shows how binary dependencies can provide useful information about a program's expected behavior and runtime environment.

The analysis covers:

* shared library dependencies;
* dynamic linking;
* binary dependency inspection;
* interpretation of external library requirements.

Expected file:

```text
external_library.txt
```

The identified library is intentionally not disclosed in this README.

## Tools and Environment

* Kali Linux
* Bash
* ELF binaries
* `readelf`
* `objdump`
* `ldd`
* Local virtual machine or sandbox

All analyses were conducted without using online tools or external binary-analysis services.

## Repository Structure

```text
re_fundamentals/
├── README.md
├── get_entry_point.sh
├── size.txt
├── command.txt
└── external_library.txt
```

The target binaries used during the exercises are provided separately as part of the controlled learning environment.

## Analysis Methodology

The project follows a simple static analysis workflow:

1. Validate the target file and preserve its integrity.
2. Confirm the executable format and architecture.
3. Inspect the ELF header.
4. Enumerate the binary sections.
5. Review unusual structural characteristics.
6. Identify external dependencies.
7. Record findings in a clear and reproducible format.

This methodology helps establish a reliable foundation before moving to more advanced techniques such as disassembly, debugging, control-flow analysis, and decompilation.

## Security Relevance

Binary metadata can provide valuable information during a security investigation.

An ELF header may reveal the target architecture and execution entry point. Section analysis can expose unusual or unexpected structures, while dependency analysis can help identify the libraries and capabilities required by the program.

These techniques are useful for both defensive and offensive security work.

### Defensive Security

* triaging unknown executables;
* investigating suspicious files;
* identifying unexpected dependencies;
* supporting malware analysis;
* validating software integrity;
* preparing incident response investigations.

### Offensive Security

* understanding executable structure;
* identifying potential attack surfaces;
* preparing binaries for deeper analysis;
* supporting vulnerability research;
* locating unusual or custom program components.

## Skills Demonstrated

* ELF binary inspection
* Linux command-line analysis
* Static reverse engineering
* Bash scripting
* Input validation
* Executable metadata interpretation
* Section analysis
* Dependency analysis
* Technical documentation
* Controlled security analysis methodology

## Limitations

This project represents an introductory level of reverse engineering.

It does not yet include:

* assembly code analysis;
* function identification;
* dynamic debugging;
* decompilation;
* control-flow graph analysis;
* anti-debugging analysis;
* packing or obfuscation analysis;
* binary patching.

These topics may be addressed in later projects within the reverse engineering learning path.

## Project Status

Completed as part of the Holberton School cybersecurity curriculum.

## Author

Pierre-Yves
