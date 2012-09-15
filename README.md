## Introduction
gack is a Go port of the ack code searching utility. It will eventually
support the same interface as the original ack.

## Background
I started working on `gack` when I saw a 
[port of ack to the C language](https://github.com/ggreer/the_silver_searcher). 
As I am currently working to learn Go, and the way for me to do that is to 
write as much Go as possible, I thought it would be an interesting project.

## Status
`gack` currently supports the following flags:

```
        -f          list files only
        -g query    list files that match the query
```

## Immediate TODO
* optimise to increase speed
* add support for selecting / excluding languages

## Bugs
* `gack` uses the `filepath.Walk` function, which doesn't handle large
directories well. consequently, 
* `gack` is currently slower than `ack`. I suspect a large part of this
is the maturity of Perl's regular expression support compared to Go's.
