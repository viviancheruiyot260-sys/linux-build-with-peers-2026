Archiving and Compression

## 9.1 Introduction

Archiving combines multiple files or directories into one archive. Compression reduces the size of data.

Linux commonly uses tools such as:

* `tar` — creates and extracts archives
* `gzip` — compresses files
* `zip` — creates ZIP archives
* `unzip` — extracts ZIP archives

Archiving puts files together, while compression makes them smaller.

---

## 9.2 Compressing Files

Compression reduces the amount of storage space needed.

### Lossless vs Lossy

* **Lossless:** No data is lost when compressed and decompressed.
* **Lossy:** Some data is removed to reduce file size.

### gzip

```bash
gzip filename
```

This compresses a file and creates a `.gz` file.

To decompress:

```bash
gunzip filename.gz
```

or:

```bash
gzip -d filename.gz
```

To view compression information:

```bash
gzip -l filename.gz
```

Other compression tools include:

```text
bzip2
xz
```

---

## 9.3 Archiving with tar

`tar` is used to combine multiple files and directories into one archive.

### Create an archive

```bash
tar -cf archive.tar files
```

* `-c` → create
* `-f` → specify archive filename

### Create a gzip-compressed archive

```bash
tar -czf archive.tar.gz files
```

### Create a bzip2-compressed archive

```bash
tar -cjf archive.tar.bz2 files
```

### List archive contents

```bash
tar -tf archive.tar
```

For a bzip2 archive:

```bash
tar -tjf archive.tbz
```

### Extract an archive

```bash
tar -xf archive.tar
```

For a bzip2 archive:

```bash
tar -xjf archive.tbz
```

### Verbose extraction

```bash
tar -xjvf archive.tbz
```

The `-v` option shows the files being processed.

### Extract a specific file

```bash
tar -xjvf archive.tbz path/to/file
```

---

## 9.4 ZIP Files

ZIP is a widely used archive format, especially on Windows.

### Create a ZIP archive

```bash
zip archive.zip files
```

Example:

```bash
zip alpha_files.zip alpha*
```

### ZIP a directory

Use `-r` to include files inside subdirectories:

```bash
zip -r School.zip School
```

### List ZIP contents

```bash
unzip -l School.zip
```

### Extract a ZIP archive

```bash
unzip School.zip
```

### Extract a specific file

```bash
unzip School.zip School/Math/numbers.txt
```

Wildcards can also be used when selecting files.

## Key Takeaways

* `tar` is mainly used for creating and extracting archives.
* `gzip`, `bzip2`, and `xz` are compression tools.
* `zip` creates compressed ZIP archives.
* `unzip` extracts ZIP archives.
* `tar` automatically includes subdirectories, while `zip` needs `-r`.
* `-t` lists archive contents.
* `-x` extracts files.
* `-c` creates an archive.
* `-f` specifies the archive filename.
* `-v` shows files being processed.
