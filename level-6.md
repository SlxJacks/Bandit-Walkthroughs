# Bandit Level 6

## Goal

The password for next level is stored in a file somewhere under the inhere directory and has all of the following properties:

- human-readable
- 1033 bytes in size
- not executable

## Command Used

### To list out directory and confirm the directory
```bash
ls -l
```

### To go into the directory
```bash
cd inhere/
```

### To list out all files or directories just to check 
```bash
ls -la
```

### By using the below command we can find the exact file which has the password the options are given based on their hints from question
```bash
find ./ -type f -size 1033c ! -executable
```

### The above command will return something like this 
```bash
bandit5@bandit:~/inhere$ find ./ -type f -size 1033c ! -executable
./maybehere07/.file2
```

### Based on above data we can just read the file to know the password for the next level 
```bash
cat ./maybehere07/.file2
```

### Last output would be something like this only containing password for the next game
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
