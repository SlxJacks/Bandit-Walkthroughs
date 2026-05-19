# Bandit Level 9

## Goal

The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

## Command Used

### To list out the line that contains the password
```bash
sort data.txt | uniq -u
```

#### We have sorted the file firs because if the following reason
The uniq command has a strict limitation: it only checks adjacent (neighboring) lines. It reads a file from top to bottom, and if a line matches the one immediately before it, it considers it a duplicate. It completely misses duplicates that are separated by other lines.

### Last output would be something like this only containing password for the next game
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
