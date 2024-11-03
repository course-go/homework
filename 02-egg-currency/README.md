# EGG Currency

_"Paying with eggs was never easier."_ - Author unknown

## Assignment

Throughout this homework assignment you will expand your existing solution
of the [egg](https://github.com/course-go/egg) project with
concurrent processing.

### Specification

The goal of this task is to make files processing concurrent. That is, whenever
the client provides a list of files for the _egg_ to match, your solution should
match the files concurrently.

Whenever an error occurs while processing the files, the program should not terminate
right away. Instead, it should finish processing the rest of the files that did
not encounter any problem and print their matched output in the order in which they
were provided on the command line.

If processing one or more files failed, the program must terminate with non-zero
code.

If you are unsure about some behaviour take the tests as the source of truth.

## Requirements

The CLI application has to support all the functionality previously
described. Stress is also given on writing idiomatic code and properly
handling resources and errors.

The concurrent solution must be correct and deterministic with no unnecessary
synchronizations, no inefficiencies and without unidiomatic usage of
synchronization primitives.

## Motivation

The main goal of this homework is to practice the usage of synchronization
primitives and Go concurrency concepts such as channels or goroutines.

## Packages

Some of the Go packages worth looking into include:

- [sync](https://pkg.go.dev/sync) for synchronization primitives
- [context](https://pkg.go.dev/context) for context and signaling
