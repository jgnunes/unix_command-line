# Introduction
Unix commands that I found useful

# xargs
## Parallelize gzip for multiple files
Find files greater than 1G and send one by one to xargs, using 4 threads (i.e. total of 4 files being processed in parallel)
```bash
find . -size +1G | xargs -n 1 -P 4 gzip
```

# find 
## Find files that follow one pattern OR another one
Find files that end with either `.fa` or `.fna`
find . \( -name "*.fa" -o -name "*.fna" \)
