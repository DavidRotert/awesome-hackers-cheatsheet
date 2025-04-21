#bash #terminal #tool #text-processing #helper
Merge lines of files. Write lines consisting of the sequentially corresponding lines from each FILE, separated by TABs, to standard output. With no FILE, or when FILE is -, read standard input.

# Quick examples
```
$ cat file1.txt
marie
daniel
henry

$ cat file2.txt
password123
SecurePazzW0rd
F0rdMu3t4ng

$ paste -d ':' file1.txt file2.txt 
marie:password123
daniel:SecurePazzW0rd

$ paste -s -d ':' file1.txt file2.txt
marie:daniel
password123:SecurePazzW0rd
henry:F0rdMu3t4ng

$ paste -s -d ':' file1.txt file2.txt
marie:daniel:henry
password123:SecurePazzW0rd:F0rdMu3t4ng

$ paste -s -d ':=' file1.txt file2.txt
marie:daniel=henry
password123:SecurePazzW0rd=F0rdMu3t4ng
```
# Common flags and arguments
| Flag                     | Description                                              |
| ------------------------ | -------------------------------------------------------- |
| `-d` `--delimiters`      | reuse characters from LIST instead of TABs as delimiters |
| `-s` `--serial`          | paste one file at a time instead of in parallel          |
| `-z` `--zero-terminated` | line delimiter is NUL, not newline                       |
