
 Archiving and Compression — Lab

## 1. Create a Practice Directory

```bash
mkdir -p ~/module9-lab
cd ~/module9-lab
```

Create some practice files:

```bash
echo "Linux file one" > file1.txt
echo "Linux file two" > file2.txt
echo "Linux file three" > file3.txt
```

Check the files:

```bash
ls
```

---

## 2. Compress a File with gzip

```bash
gzip file1.txt
```

Check the result:

```bash
ls
```

View compression information:

```bash
gzip -l file1.txt.gz
```

Decompress it:

```bash
gunzip file1.txt.gz
```

---

## 3. Create a tar Archive

```bash
tar -cf files.tar file1.txt file2.txt file3.txt
```

Check the archive:

```bash
ls
```

---

## 4. List tar Contents

```bash
tar -tf files.tar
```

This shows the files stored in the archive without extracting them.

---

## 5. Create a Compressed tar Archive

Using gzip:

```bash
tar -czf files.tar.gz file1.txt file2.txt file3.txt
```

Using bzip2:

```bash
tar -cjf files.tar.bz2 file1.txt file2.txt file3.txt
```

---

## 6. Extract a tar Archive

Create a directory for extraction:

```bash
mkdir extracted
```

Extract the archive there:

```bash
tar -xf files.tar -C extracted
```

Check the extracted files:

```bash
ls extracted
```

---

## 7. Create a ZIP Archive

```bash
zip files.zip file1.txt file2.txt file3.txt
```

Check:

```bash
ls
```

---

## 8. List ZIP Contents

```bash
unzip -l files.zip
```

---

## 9. Extract ZIP Files

Create another directory:

```bash
mkdir zip-extracted
```

Extract the ZIP archive:

```bash
unzip files.zip -d zip-extracted
```

Check the files:

```bash
ls zip-extracted
```

