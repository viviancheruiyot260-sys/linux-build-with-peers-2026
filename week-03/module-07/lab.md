Files and Directories — Lab

## 1. Working Directory

```bash
pwd
```

Shows the current working directory.

```bash
echo $HOME
```

Shows the home directory of the current user.

---

## 2. Absolute Path

```bash
cd /home
pwd
```

Moves to `/home` using an absolute path.

An absolute path starts from the root directory `/`.

---

## 3. Home Directory

```bash
cd ~
pwd
```

`~` represents the home directory of the current user.

---

## 4. Relative Path

```bash
cd ../dict
pwd
```

`..` represents the parent directory.

The command moves up one directory and then into the `dict` directory.

---

## 5. Listing Files and Directories

```bash
cd
ls
```

Returns to the home directory and lists its contents.

---

## 6. Hidden Files

```bash
ls -a
```

Displays all files and directories, including hidden files.

Hidden files usually begin with `.`.

```text
.   → current directory
..  → parent directory
```

---

## 7. Detailed File Information

```bash
ls -l /etc/hosts
```

Displays detailed information about the file, including:

* File type
* Permissions
* Owner
* Group
* Size
* Modification date
* File name

---

## 8. Recursive Listing

```bash
ls -R /etc/udev
```

`-R` means recursive. It displays the contents of a directory and its subdirectories.

> Avoid using `ls -R /` because it can produce a very large amount of output.

---

## 9. File Globbing

### Using `*`

```bash
ls -d /etc/s*
```

Displays items in `/etc` whose names begin with `s`.

`*` matches zero or more characters.

### Using `?`

```bash
ls -d /etc/????
```

Displays items with exactly four characters in their names.

`?` matches exactly one character.

### Using `[ ]`

```bash
ls -d /etc/[abcd]*
```

Displays items whose names begin with `a`, `b`, `c`, or `d`.

`[abcd]` matches one character from the specified set.

---

## Key Commands

| Command  | Purpose                          |
| -------- | -------------------------------- |
| `pwd`    | Shows the current directory      |
| `cd`     | Changes directory                |
| `cd ~`   | Goes to the home directory       |
| `cd ..`  | Moves to the parent directory    |
| `ls`     | Lists files and directories      |
| `ls -a`  | Shows hidden files               |
| `ls -l`  | Shows detailed information       |
| `ls -R`  | Lists recursively                |
| `*`      | Matches zero or more characters  |
| `?`      | Matches exactly one character    |
| `[abcd]` | Matches one character from a set |



