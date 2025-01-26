# Bash Scripting Guide

This repository contains a comprehensive guide to Bash scripting, covering everything from basic commands to advanced scripting techniques. Whether you're a beginner or an experienced developer, this guide will help you master Bash scripting.

---

## Table of Contents

1. [Introduction to Bash](#introduction-to-bash)
2. [Basic Bash Commands](#basic-bash-commands)
3. [Variables and Data Types](#variables-and-data-types)
4. [Control Structures](#control-structures)
5. [Functions](#functions)
6. [Input and Output](#input-and-output)
7. [File Handling](#file-handling)
8. [Advanced Scripting](#advanced-scripting)
9. [Debugging and Error Handling](#debugging-and-error-handling)
10. [Best Practices](#best-practices)
11. [Resources](#resources)

---

## Introduction to Bash

Bash (Bourne Again Shell) is a Unix shell and command language. It is widely used for scripting, automation, and system administration tasks. Bash scripts are text files containing a series of commands that are executed by the Bash interpreter.

---

## Basic Bash Commands

- `echo`: Print text to the terminal.
- `ls`: List files and directories.
- `cd`: Change directory.
- `pwd`: Print the current working directory.
- `mkdir`: Create a new directory.
- `rm`: Remove files or directories.
- `cp`: Copy files or directories.
- `mv`: Move or rename files or directories.
- `cat`: Display the contents of a file.
- `grep`: Search for text in files.

---

## Variables and Data Types

- **Variables**: Store data for later use.
  ```bash
  name="John"
  echo "Hello, $name"
  ```
- **Environment Variables**: Predefined variables that store system information.
  ```bash
  echo $HOME
  echo $PATH
  ```
- **Quotes**: Use single quotes (`'`) for literal strings and double quotes (`"`) for strings with variable expansion.

---

## Control Structures

- **If-Else Statements**: Make decisions based on conditions.
  ```bash
  if [ "$age" -gt 18 ]; then
      echo "You are an adult."
  else
      echo "You are a minor."
  fi
  ```
- **Loops**: Repeat commands.
  - **For Loop**:
    ```bash
    for i in {1..5}; do
        echo "Iteration $i"
    done
    ```
  - **While Loop**:
    ```bash
    count=1
    while [ $count -le 5 ]; do
        echo "Count: $count"
        ((count++))
    done
    ```

---

## Functions

- Define reusable blocks of code.
  ```bash
  greet() {
      echo "Hello, $1!"
  }
  greet "Alice"
  ```

---

## Input and Output

- **Read Input**: Get user input.
  ```bash
  echo "Enter your name:"
  read name
  echo "Hello, $name!"
  ```
- **Redirect Output**: Save output to a file.
  ```bash
  echo "Hello, World!" > output.txt
  ```
- **Append Output**: Add output to a file.
  ```bash
  echo "Goodbye, World!" >> output.txt
  ```

---

## File Handling

- **Read Files**: Process file contents line by line.
  ```bash
  while IFS= read -r line; do
      echo "$line"
  done < input.txt
  ```
- **Write Files**: Create or overwrite files.
  ```bash
  echo "New content" > file.txt
  ```

---

## Advanced Scripting

- **Command Substitution**: Use the output of a command as a variable.
  ```bash
  current_date=$(date)
  echo "Today is $current_date"
  ```
- **Arrays**: Store multiple values.
  ```bash
  fruits=("Apple" "Banana" "Cherry")
  echo "First fruit: ${fruits[0]}"
  ```
- **Case Statements**: Handle multiple conditions.
  ```bash
  case "$fruit" in
      "Apple") echo "It's an apple." ;;
      "Banana") echo "It's a banana." ;;
      *) echo "Unknown fruit." ;;
  esac
  ```

---

## Debugging and Error Handling

- **Debug Mode**: Run a script with debugging enabled.
  ```bash
  bash -x script.sh
  ```
- **Error Handling**: Check the exit status of commands.
  ```bash
  if ! command; then
      echo "Command failed."
      exit 1
  fi
  ```

---

## Best Practices

1. **Use Shebang**: Always start scripts with `#!/bin/bash`.
2. **Quote Variables**: Prevent unexpected behavior with spaces or special characters.
3. **Use Comments**: Explain your code for better readability.
4. **Validate Input**: Check user input to avoid errors.
5. **Use Functions**: Break down scripts into reusable functions.
6. **Test Scripts**: Test your scripts in a safe environment before deployment.

---

## Resources

- [Bash Reference Manual](https://www.gnu.org/software/bash/manual/)
- [Advanced Bash-Scripting Guide](https://tldp.org/LDP/abs/html/)
- [ShellCheck](https://www.shellcheck.net/): A tool for linting Bash scripts.

---
