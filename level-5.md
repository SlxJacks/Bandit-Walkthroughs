# Bandit Level 5

## Goal

Get the password for next level is in only human-readable file in the inhere directory.

## Command Used

### To list out directory and confirm the directory
```bash
ls -l
```

### To go into the directory
```bash
cd inhere/
```

### To list out all files
```bash
ls -la
```

### By using the below command we have can find the encoding for each files 
```bash
file ./*
```

### The above command will return something like this 
```bash
bandit4@bandit:~/inhere$ file ./*
./-file00: data
./-file01: data
./-file02: data
./-file03: DOS executable (COM), start instruction 0x8c887e10 c3ee96c9
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
```

### Based on above data we can just read the ASCII text file to know the password for the next level 
```bash
cat ./-file07
```

### Last output would be something like this only containing password for the next game
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
