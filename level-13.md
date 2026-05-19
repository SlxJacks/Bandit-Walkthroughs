# Bandit Level 13

## Goal

The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)

## Command Used

### To list out and confirm the file 
```bash
ls -l
```

### To make a random name tmp dir
```bash
mktemp -d
```

### To copy the data file into that tmp dir
```bash
cp data.txt /tmp/tmp.AgLC1nAuZh
```

### To move inside that tmp dir
```bash
cd /tmp/tmp.AgLC1nAuZh
```

### To rename the file into the normal binary file type then you can use below command to actually check the file type as its hexdump we will first use the xxd command to fix that
```bash
mv data.txt data

xxd -r data > binary

file binary
```

### Now that we know its one of the compressed file we wil use the gzip tar or bzip to uncompress the file in loop
```bash
mv binary binary.gz

gzip -d binary.gz

bandit12@bandit:/tmp/tmp.AgLC1nAuZh$ file binary 
binary: bzip2 compressed data, block size = 900k

mv binary binary.bz2

bunzip2 binary.bz2

bandit12@bandit:/tmp/tmp.AgLC1nAuZh$ file binary 
binary: POSIX tar archive (GNU)

tar -xvf binary.tar
```

### Last output would be something like this only containing password for the next game
```bash
bandit12@bandit:/tmp/tmp.AgLC1nAuZh$ cat data8 
The password is FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
```
