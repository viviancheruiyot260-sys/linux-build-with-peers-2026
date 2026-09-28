
## Files and Directories

```bash
ls
```

Lists files and directories in the current location.

```bash
ls -l
```

Displays files and directories with detailed information.

```bash
ls -l /home
```

Displays detailed contents of the `/home` directory.

```bash
pwd
```

Shows the current working directory.

## User and System Information

```bash
whoami
```

Shows the username of the current user.

```bash
uname
```

Displays the Linux system/kernel name.

```bash
uname -n
```

Displays the system hostname.

```bash
uname --nodename
```

Also displays the system hostname.

## Command History

```bash
history 5
```

Displays the five most recent commands.

```bash
echo Hi
```

Displays the text `Hi`.

```bash
!9
```

Runs the command stored at history entry number 9.

```text
↑ / ↓
```

The arrow keys are used to move through previous commands.

## Shell Variables

```bash
echo $HISTSIZE
```

Displays the number of commands Bash stores in history.

```bash
echo $PATH
```

Displays the directories Bash searches when looking for executable commands.

```bash
which date
```

Shows the location of the `date` executable.

## Command Types

```bash
type cd
```

Identifies `cd` as a shell built-in command.

```bash
which ls
```

Shows the location of the `ls` executable.

```bash
type ls
```

Identifies the type and location of `ls`.

```bash
type -a ls
```

Shows all known forms or locations of `ls`.

```bash
type vi
```

Checks the type and location of the `vi` executable.

```bash
type vlc
```

Checks whether Bash can find the `vlc` command.

```bash
cd /bin
```

Moves into the `/bin` directory.

```bash
cd
```

Returns to the user's home directory.

## Aliases

```bash
alias
```

Displays the aliases currently configured in the shell.

```bash
type ll
```

Checks whether `ll` is an alias and shows what it represents.

## Quoting

```bash
echo 'Hello $USER'
```

Prints `$USER` literally because single quotes prevent variable expansion.

```bash
echo "Hello $USER"
```

Expands `$USER` and displays the current username.

```bash
echo "The price is \$100"
```

Uses `\` to treat `$` as a normal character.

```bash
echo "Today is $(date)"
```

Runs `date` and inserts its output into the sentence.

## Logical AND

```bash
echo Success && false && echo Bye
```

Runs the next command only when the previous command succeeds. Since `false` fails, `echo Bye` is not executed.

