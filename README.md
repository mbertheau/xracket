# xRacket

Exercism problems in Racket.

## Working on the Exercises

We welcome both improvements to the existing exercises and the addition of new exercises. A pool of exercise ideas can be found in the [x-common repo](https://github.com/exercism/x-common).

Each exercise should have an example solution and a test suite, as well as a stub file for the solution declaring the module and exports.

### Naming Conventions 

The example solution should be named `example.rkt`. The test should be named `<exercise-name>-test.rkt`, and the stub should be named `<exercise-name>.rkt`.

For example, if you were to work on the `binary` exercise, you would have the following three files:

```bash
$ tree
.
├── binary.rkt
├── binary-test.rkt
└── example.rkt
```

### Code Style
The Racket code in this repo is meant to conform with the conventions set forth in [How to Program Racket](http://docs.racket-lang.org/style/index.html).

### Dependencies
Try to avoid external dependencies.

### Pull Requests
Prior to submitting a pull request, ensure that your test requires the stub file, and not the example file - like so:

```Racket
#lang racket/base

(require "perfect-numbers.rkt")

(module+ test
  (require rackunit rackunit/text-ui)

  (define suite
    (test-suite
     "perfect numbers tests"

     (test-equal? "no perfect numbers in 1 - 5"
                  (perfect-numbers 5)
                  '())))

  (run-tests suite))
```
The exercise should also be added as a value for the `problems` key in [config.json](https://github.com/exercism/xracket/blob/master/config.json); otherwise, the pull request will not pass the Travis CI build.

You can perform additional checks by running the following in your terminal:

```bash
bin/check_exercises.sh
```

and:

```bash
bin/configlet .
```
Your pull request won't pass the Travis CI build if either of those fail.

If you're new to Git, take a look at [this short guide](http://help.exercism.io/git-workflow.html).

## READMEs
Please do not add a README or README.md file to the problem directory. The READMEs are constructed using shared metadata, which lives in the [exercism/x-common](https://github.com/exercism/x-common) repository.

## Contributing Guide

Please see the [contributing guide](https://github.com/exercism/x-api/blob/master/CONTRIBUTING.md#the-exercise-data)

## License

The MIT License (MIT)

Copyright (c) 2015 Katrina Owen, _@kytrinyx.com

