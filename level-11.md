# Bandit Level 11

## Goal

The password for the next level is stored in the file data.txt, which contains base64 encoded data

## Command Used

### As the file contains the base64 encoded data we have used the option -d here to decode the file data
```bash
base64 -d data.txt
```

### Last output would be something like this only containing password for the next game
```bash
The password is dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
```
