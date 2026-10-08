Bash Scripting

## Overview

Bash scripting allows us to put Linux commands into a file and run them together. It helps automate repetitive tasks.

### Shell Scripts

A shell script usually starts with:

```bash
#!/bin/bash
```

This tells Linux to use Bash to run the script.

### Variables

Variables store information that can be used later.

```bash
NAME="Vivian"
echo "$NAME"
```

### Conditionals

Conditionals allow a script to make decisions.

```bash
if [ condition ]; then
    command
else
    command
fi
```

- `if` → checks a condition.
- `else` → runs when the condition is false.
- `fi` → ends the condition.

### Loops

Loops repeat commands.

- `for` → repeats for each item in a list.
- `while` → repeats while a condition is true.

Example:

```bash
for NAME in Linux Bash Cloud; do
    echo "$NAME"
done
```

### Editing Scripts

`nano` can be used to create and edit scripts.

Useful shortcuts:

- `Ctrl + O` → Save
- `Ctrl + X` → Exit
- `Ctrl + W` → Search

