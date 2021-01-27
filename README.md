# ht-wrangle
This repository is about useful bash commands

# Assigned play:

- Just choose any two speakers from this url: http://shakespeare.mit.edu/hamlet/full.html
- I have chosen below 2 speakers
    - Speaker 1: Hamlet
    - Speaker 2: Horatio

# Getting data from url into a file

- Run below command in bash
```
curl "http://shakespeare.mit.edu/hamlet/full.html" | sed 's/<\/*[^>]*>//g' > input.txt
```
- Above command gets data from url and it remove unnecessary tags and dumps data into input.txt file

# Speaker 1: Hamlet

- Run below command in bash
```
grep '^HAMLET$' input.txt -c > hamletCount.txt
```
- output in hamletCount.txt: 359

- grep command used to find match regular expression with input
- -c refers count of matched data with input file

# Speaker 2: Hamlet
- Run below command in bash
```
grep '^HORATIO$' input.txt -c. > horatioCount.txt
```
- output in horatioCount.txt: 112

# My question:
- How many times does speaker speaks in tragedy
# Files:
- [input.txt](./input.tx)
- [hamletCount.txt](./hamletCount.txt)
- [horatioCount.txt](./horatioCount.txt)
