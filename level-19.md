# Bandit Level 10

## Goal

The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

## Command Used

### To list out the line that contains the password
```bash
strings data.txt | grep -E "=+"
```

#### We have used the strings here so that file can be treated as text file otherwise grep command will just treat the file as binary file as this file contains code that is of binary

### Last output would be something like this only containing password for the next game
```bash
========== the
I\=Ow
V?L=
%3=VZ
========== password
={M\
========== is
=Dvq
=n/N
========== FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
zX]%=
]\{=
```
