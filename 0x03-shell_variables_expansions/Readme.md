# Bash Init Files, Variables and Expansions

This repository contains a collection of Bash scripts demonstrating various shell concepts including aliases, variables, arithmetic operations, and text processing.

## Tasks

### 0. alias
**File:** `0-alias`

Creates an alias that makes the `ls` command execute `rm *` instead. This is a dangerous alias that would delete all files in the current directory when running `ls`.

**Warning:** This is for educational purposes only. Never use this alias in a real environment.

### 1. Hello You
**File:** `1-hello_you`

Prints a greeting message with the current user's username using the `whoami` command.

**Output:** `hello <username>`

### 2. Path
**File:** `2-path`

Adds the `/action` directory to the end of the PATH environment variable, making executables in that directory accessible from anywhere.

### 3. Paths
**File:** `3-paths`

Counts and displays the number of directories in the PATH environment variable. It splits the PATH by colons, filters out empty lines, and counts the results.

### 4. Global Variables
**File:** `4-global_variables`

Lists all environment variables (global variables) using the `printenv` command.

### 5. Local Variables
**File:** `5-local_variables`

Lists all variables, including local variables, environment variables, and shell functions using the `set` command.

### 6. Create Local Variable
**File:** `6-create_local_variable`

Creates a local variable named `BEST` with the value "School". This variable is only available in the current shell session.

### 7. Create Global Variable
**File:** `7-create_global_variable`

Creates and exports a global variable named `BEST` with the value "School", making it available to child processes.

### 8. True Knowledge
**File:** `8-true_knowledge`

Performs arithmetic addition of 128 with the value stored in the `TRUEKNOWLEDGE` environment variable and prints the result.

### 9. Divide and Rule
**File:** `9-divide_and_rule`

Divides the value of the `POWER` environment variable by the value of the `DIVIDE` environment variable and prints the result.

### 10. Love Exponent Breath
**File:** `10-love_exponent_breath`

Calculates `BREATH` raised to the power of `LOVE` (exponentiation) and prints the result.

### 11. Binary to Decimal
**File:** `11-binary_to_decimal`

Converts a binary number stored in the `BINARY` environment variable to its decimal equivalent using base conversion syntax `2#`.

### 12. Combinations
**File:** `12-combinations`

Generates all possible two-letter combinations from 'a' to 'z', prints each on a new line, and excludes the combination "oo". Uses brace expansion and text processing.

**Output:** aa, ab, ac, ..., zz (excluding oo)

### 13. Print Float
**File:** `13-print_float`

Prints the value of the `NUM` environment variable formatted as a floating-point number with exactly 2 decimal places using `printf`.

## Usage

Make each script executable:
```bash
chmod +x <script_name>
```

Run a script:
```bash
./<script_name>
```

Some scripts require environment variables to be set before execution. For example:
```bash
export TRUEKNOWLEDGE=1209
./8-true_knowledge
```

## Requirements

- All scripts are tested on Ubuntu
- All scripts are exactly 2 lines long
- All files start with `#!/bin/bash`
- Bash version 4.0 or higher recommended