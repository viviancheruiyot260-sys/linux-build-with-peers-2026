Linux Text Processing

## 10.1 Overview

Linux provides many commands for viewing, searching, filtering, and processing text files.

### Viewing Text

- `cat` — displays the contents of a file.
- `less` — views large files page by page.
- `head` — shows the first 10 lines by default.
- `tail` — shows the last 10 lines by default.
- `tail -f` — follows a file as new content is added, useful for logs.

### Pipes

The `|` symbol sends the output of one command to another command.

```bash
cat file1.txt | grep "Linux"
```

This displays only the lines containing **Linux**.

### Input and Output Redirection

Linux uses three standard streams:

- **STDIN (0)** — input
- **STDOUT (1)** — normal output
- **STDERR (2)** — error messages

Common redirection operators:

- `>` — writes output to a file and overwrites existing content.
- `>>` — adds output to the end of a file.
- `2>` — sends error messages to a file.
- `&>` — sends both normal output and errors to a file.
- `<` — takes input from a file.

### Sorting and Counting

- `sort` — arranges lines alphabetically or numerically.
- `wc` — counts lines, words, and bytes.

Examples:

```bash
sort file1.txt
wc file1.txt
wc -l file1.txt
```

### Extracting Text

`cut` extracts specific parts of each line.

```bash
cut -d, -f1 file1.txt
```

- `-d` specifies the delimiter.
- `-f` specifies the field to extract.
- `-c` extracts characters by position.

### Searching with grep

`grep` searches for matching text in files or command output.

```bash
grep "Linux" file1.txt
```

Useful options:

- `-i` — ignore uppercase/lowercase.
- `-n` — show line numbers.
- `-c` — count matching lines.
- `-v` — show lines that do not match.
- `-w` — match whole words.

### Regular Expressions

Regular expressions help create more specific search patterns.

Common symbols:

- `.` — any single character
- `[ ]` — characters from a specified set
- `^` — beginning of a line
- `$` — end of a line
- `*` — zero or more occurrences

For extended regular expressions, `grep -E` supports patterns such as `?`, `+`, and `|`.

