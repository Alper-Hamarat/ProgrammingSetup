# Functional Requirements

## The executable format

- The generator shall be delivered as a single executable .exe file for Windows 10+.

## Command line interface (CLI)

- The generator shall accept command line arguments
- The generator shall provide a --help or -h option that lists all supported arguments
- The generator shall support at least the following arguments:
  - --language language: Defines the target programming language (eg. cpp, c , python).
  - --name projectname: Defines the name of the root project folder.
  - --with-makefile: optionally generates a Makefile (if supported by the selected language).
  - --interactive: starts the tool in interactive mode (if no other args provided)

## Folder Generation

- The generator shall create a root project foler named after the provided project name
- The generator shall create a subfolder structure according to common best practices for the selected language (e.g., src/, include/, build/ for C/C++)

## File Generation

- The generator shall create a main source file with a minimum boilerplate (e.g main.cpp, main.c, main.py).
- The generator shall optionally create a README.md with project information
- The generator shall optionally create .gitignore file

# Non-Functional Requirements

## Usability

- The executables shall be usable from the windows command line
- The generator shal print meaningful error messages if requires arguments are missing or invalid

## Protability

- The generated projects shall be portable to other systems (e.g. Linux) if language allows (e.g. C/C++ with Makefile).

## Extensibility

- The generator shall allow easy extension to support additional programming languages in the future.
