

## 1. Man Pages

The `man` command provides detailed documentation for Linux commands.

```bash
man command
```

Example:

```bash
man ls
```

Important sections include:

* NAME — short description
* SYNOPSIS — command syntax
* DESCRIPTION — detailed explanation
* OPTIONS — available options
* SEE ALSO — related documentation

Useful commands:

```bash
man -f command
man section command
man -k keyword
```

* `man -f` finds manual entries by name.
* `man section command` opens a specific manual section.
* `man -k` searches manual pages using a keyword.

## 2. Finding Commands and Documentation

Different commands help locate information:

```bash
type ls
which ls
whereis ls
whatis ls
```

* `type` shows how Bash identifies a command.
* `which` shows the executable found through the PATH.
* `whereis` searches for the executable, source, and manual pages.
* `whatis` gives a short description from the manual database.

## 3. Locate

The `locate` command searches a database of files and directories.

```bash
locate filename
locate -c filename
locate -b filename
```

The database may not immediately contain newly created files.

## 4. Info Documentation

The `info` command provides structured documentation organized into connected topics or **nodes**.

```bash
info
info ls
```

Unlike man pages, Info documentation works more like a book with a table of contents and linked sections.

Useful navigation keys include:

* `Enter` — open a link
* `U` — move up one level
* `L` — return to the previous location
* `N` — next node
* `P` — previous node
* `H` — help
* `Q` — quit

## 5. The `--help` Option

Many Linux commands provide quick usage information through:

```bash
command --help
```

Example:

```bash
cat --help
```

This usually displays the command's syntax, description, options, and sometimes examples.

## 6. Additional System Documentation

Software may include documentation files such as:

```text
README
README.txt
readme.txt
```

Common documentation locations include:

```bash
/usr/share/doc
/usr/doc
```

For example:

```bash
ls /usr/share/doc/bash
```

These files can provide software-specific installation, configuration, and usage information.

## Key Takeaway

Linux provides several ways to get help instead of requiring users to memorize commands.

The main tools I learned are:

```text
--help  → quick help
man     → detailed reference
info    → structured documentation
whatis  → short description
whereis → locate command and documentation
locate  → find files using a database
/usr/share/doc → additional software documentation
```



