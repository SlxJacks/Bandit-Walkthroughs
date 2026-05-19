# Bandit Level 7

## Goal

The password for next level is stored somewhere on the server and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size

## Command Used

### By using the below command we can find the exact file which has the password the options are given based on their hints from question
```bash
find /* -group bandit6 -user bandit7 -size 33c -type f
```

### We can always use 2>/dev/null in command above to hide the errors
```bash
find /* -group bandit6 -user bandit7 -size 33c -type f 2>/dev/null
```

### Based on above result data we can just read the file to know the password for the next level 
```bash
cat /var/lib/dpkg/info/bandit7.passwor
```

### Last output would be something like this only containing password for the next game
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
