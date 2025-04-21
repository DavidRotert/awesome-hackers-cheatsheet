#bash #terminal #text-processing #tool #helper #awk
Pattern scanning and processing language. Can be used for:
- Text processing
- Producing formatted text reports
- Performing arithmetic operations
- Performing string operations
# Quick Examples
```
```
# Common flags and arguments
| Flag                                 | Description                                                                                                                                                                                                                                                                                                               |
| ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `-f` `--file`                        | Load AWK program from file instead of string                                                                                                                                                                                                                                                                              |
| `-v` `--assign`                      | Assign the value val to the variable var, before execution of the program begins.  Such variable values are available to the BEGIN rule of an AWK program                                                                                                                                                                 |
| `-p prof-file` `--profile prof-file` | Start a profiling session, and send the profiling data to `prof-file`.  The default is awkprof.out in the current directory.  The profile contains execution counts of each statement in the program in the left margin and function call counts for each user-defined function. For debugging and profiling AWK programs |
# Workflow
The workflow is as follow:
1. Executes commands from a `BEGIN` block
2. Reads a line from input stream
3. Executes command on a line
4. If it is not end of file, repeats from 2., else jump to `END`
5. Execute commands from `END` block
## `BEGIN` and `END` blocks
`BEGIN {awk-commands}`
`END {awk-commands}`
## Body block
`/pattern/ {awk-commands}`
`/pattern/` restricts on which lines the commands are executed
## Example
```
$ cat marks.txt
1)  Amit    Physics  80
2)  Rahul   Maths    90
3)  Shyam   Biology  87
4)  Kedar   English  85
5)  Hari    History  89

$ awk 'BEGIN{printf "Sr No\tName\tSub\tMarks\n"} {print}' marks.txt
Sr No	Name	Sub	Marks
1)  Amit    Physics  80
2)  Rahul   Maths    90
3)  Shyam   Biology  87
4)  Kedar   English  85
5)  Hari    History  89
```

# AWK language
AWK basically supports basic programming language concepts like loops, variables, conditions, operations, ternary operators, arrays, etc.

## String concatenation
Just write one string after another:
`awk 'BEGIN { str1 = "Hello, "; str2 = "World"; str3 = str1 str2; print str3 }'`
## Regex match
`awk '$0 ~ 9' # matches everything where column 0 matches 9. If you want to negate the match, use !~`

