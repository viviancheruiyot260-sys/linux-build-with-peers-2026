 Lab

## 1. Practice Globbing

```bash
cd ~
echo *
echo *.txt
echo /etc/t*
echo /etc/[a-d]*
echo /etc/[!a-t]*
```

## 2. List Files Using Globs

```bash
ls -d /etc/a*
ls -d /etc/x*
```

The `-d` option displays matching directory names instead of their contents.

## 3. Copy a File

```bash
cp /etc/hosts ~/hosts
ls -l ~/hosts
```

Verbose mode:

```bash
cp -v /etc/hosts ~/hosts.copy
```

## 4. Practice Safe Copying

```bash
touch example.txt
cp -i /etc/hosts example.txt
```

Answer `y` or `n` when prompted.

Also test:

```bash
cp -n /etc/hosts example.txt
```

## 5. Copy a Directory

Create a practice directory:

```bash
mkdir testdir
touch testdir/file.txt
```

Copy it:

```bash
cp -r testdir testdir-copy
ls
```

## 6. Move and Rename

```bash
mv testdir/file.txt testdir/newfile.txt
ls testdir
```

## 7. Create and Remove Files

```bash
touch sample.txt
ls -l sample.txt
rm -i sample.txt
```

## 8. Create and Remove Directories

```bash
mkdir practice
ls
rmdir practice
```



