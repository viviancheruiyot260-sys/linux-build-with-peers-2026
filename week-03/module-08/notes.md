Globbing and File Management

## 8.1 Introduction

Globbing allows the shell to use patterns to match filenames before a command is executed.

Common glob characters:

* `*` → matches zero or more characters
* `?` → matches exactly one character
* `[ ]` → matches characters from a set or range
* `[! ]` → excludes characters from a set or range

Example:

```bash
echo /etc/*.conf
```

The shell expands the pattern before `echo` runs.

## 8.2 Listing With Globs

When using globs with `ls`, the `-d` option is useful because it displays matching directory names instead of their contents.

```bash
ls -d /etc/x*
```

## 8.3 Copying Files

The `cp` command copies files.

```bash
cp source destination
```

Useful options:

```text
-v → verbose
-i → ask before overwriting
-n → do not overwrite
-r → copy directories recursively
```

Example:

```bash
cp /etc/hosts ~
cp -v /etc/hosts ~/hosts.copy
```

## 8.4 Moving and Renaming Files

The `mv` command moves or renames files and directories.

```bash
mv source destination
```

Example:

```bash
mv example.txt Documents/
mv oldname.txt newname.txt
```

Options:

```text
-i → ask before overwriting
-n → do not overwrite
-v → show the move
```

Unlike `cp`, `mv` does not require `-r` to move directories.

## 8.5 Creating Files

The `touch` command creates an empty file.

```bash
touch sample.txt
```

A new file created with `touch` contains no data and normally has a size of 0 bytes.

## 8.6 Removing Files

The `rm` command deletes files.

```bash
rm sample.txt
```

Use `-i` for confirmation:

```bash
rm -i *.txt
```

Be careful because files deleted with `rm` are not normally sent to a trash/recycle bin.

## 8.6.1 Removing Directories

The `rm -r` command removes a directory and its contents.

```bash
rm -r directory
```

For confirmation:

```bash
rm -ri directory
```

The `rmdir` command removes only empty directories.

```bash
rmdir directory
```

## 8.7 Creating Directories

The `mkdir` command creates a new directory.

```bash
mkdir test
```

### Key Takeaways

```text
*        → zero or more characters
?        → exactly one character
[abc]    → one character from the set
[!abc]   → excludes the characters
cp       → copy
mv       → move/rename
touch    → create an empty file
rm       → remove files
rm -r    → remove directories recursively
rmdir    → remove empty directories
mkdir    → create directories
```


