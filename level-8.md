# Bandit Level 8

## Goal

The password for the next level is stored in the file data.txt next to the word millionth

## Command Used

### By using the below command we can find the exact thing which we need from file the option is given based on their hints from question
```bash
grep -r "millionth" data.txt
```

### The above command will get us the line of the passowrd which we need so output of it would be like below
```bash
bandit7@bandit:~$ grep -r "millionth" data.txt 
millionth       dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
```
