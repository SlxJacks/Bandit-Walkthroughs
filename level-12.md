# Bandit Level 12

## Goal

The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

## Command Used

### As all lowercase and uppercase letters have been rotated by 13 positions we have used the tr to translate them back into their original characters
```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

### Last output would be something like this only containing password for the next game
```bash
The password is 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
```
