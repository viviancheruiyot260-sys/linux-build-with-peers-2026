Lab — Bash Scripting

## Lab Overview

In this lab, I learned how to write simple Bash scripts, use variables, make decisions with conditions, and repeat tasks using loops.

## 1. Creating a Bash Script

```bash
nano hello.sh
```

**What it does:** Opens a text editor where I can write a Bash script.

Add this code to the file:

```bash
#!/bin/bash
echo "Hello, Linux!"
```

**What it does:**
- `#!/bin/bash` tells Linux to use Bash to run the script.
- `echo` displays a message on the screen.

Save the file using `Ctrl + O`, press `Enter`, then exit with `Ctrl + X`.

```bash
chmod +x hello.sh
./hello.sh
```

**What they do:**
- `chmod +x hello.sh` makes the script executable.
- `./hello.sh` runs the script.

## 2. Using Variables

```bash
NAME="Vivian"
echo "$NAME"
```

**What it does:** Stores a name in a variable and displays it on the screen.

## 3. Using Conditions

```bash
if [ 5 -gt 3 ]; then
    echo "5 is greater than 3"
else
    echo "5 is not greater than 3"
fi
```

**What it does:** Checks whether 5 is greater than 3 and displays the appropriate message.

## 4. Using a `for` Loop

```bash
for NAME in Vivian Linux Bash; do
    echo "Learning $NAME"
done
```

**What it does:** Repeats a command for each item in the list.

## 5. Using a `while` Loop

```bash
i=0
while [ "$i" -lt 5 ]; do
    echo "$i"
    i=$((i + 1))
done
```

**What it does:** Displays numbers from 0 to 4 and stops when the condition is no longer true.


Bash scripting is a useful skill because it helps reduce repetitive work and makes everyday tasks easier to automate.
