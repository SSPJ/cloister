# Note bene: Exercism recently changed the schema of their challenges - this code no longer works.

I hope I will have time to fix it soon-ish. :(

# Introduction

Exercism.io is a website that teaches programming in over 50 languages through a series of challenges. The challenges are MIT licensed and available on GitHub.

Cloister is a small tool for keeping track of one's progress.

I wrote this for people who do not or cannot use Exercism.io to track their progress. Longer discussion at bottom of this README.

## Project Goal

- versions of cloister written in **each programming language** available on Exercism
- each version of cloister **works with all** Exercism tracks

## Installation

Suppose you want to learn Ruby. At a bash prompt, type these commands:

```
git clone https://github.com/SSPJ/cloister.git           # download cloister
cd cloister/ruby           # change to the language of your choice
git clone --bare git@github.com:exercism/ruby.git .git   # download Exercism exercises
git config core.bare false # fix needing to use '--bare'
git checkout               # get the exercises out of .git
```

Not Ruby? Change the example to suit your desired language. Check the bottom of this README for a list.

**Note:** You can use cloister with any Exercism track! Say that you want to learn Rust, but there's no cloister for Rust. Make a rust directory and copy any cloister file into it. Here's an example:

```
git clone https://github.com/SSPJ/cloister.git
cd cloister
mkdir rust
cp python/cloister rust
cd rust
git clone --bare git@github.com:exercism/rust.git .git
git config core.bare false
git checkout
```

The only restriction is that you need to pick a cloister file from a language that your computer supports.

## Usage

In a bash shell, change to the directory of the language you installed above.

Type `./cloister`. You should see an output like this:

```
$ ./cloister
Next up are these:
difficulty 0, slug binary
difficulty 0, slug trinary
difficulty 0, slug hexadecimal
difficulty 0, slug octal
difficulty 0, slug point-mutations
difficulty 1, slug hello-world
difficulty 1, slug two-fer
difficulty 1, slug resistor-color-duo
difficulty 1, slug acronym
difficulty 1, slug hamming
difficulty 1, slug raindrops
difficulty 2, slug high-scores
difficulty 2, slug isogram
difficulty 2, slug scrabble-score
difficulty 2, slug luhn
difficulty 2, slug microwave
difficulty 3, slug series
difficulty 3, slug word-count
difficulty 3, slug clock
difficulty 3, slug tournament
difficulty 3, slug darts
difficulty 4, slug matrix
difficulty 4, slug twelve-days
Type cloister <slug> to select one.
```

Pick the one you want to work on and let cloister know:

```
$ ./cloister binary
Now working on binary
```

Start work on that exercise in your favorite editor. The exercise is located in `<language>/exercises/<slug>`. For example, `ruby/exercises/binary`. Write the code and get the tests to pass. Try not to peek at the example unless you really get stuck!

When you are ready to move on, type `./cloister` again to see the list:

```
$ ./cloister
You have completed 0 exercise(s)
You are currently working on binary
Next up are these:
difficulty 0, slug trinary
...
```

Then pick another and so on:

```
$ ./cloister trinary
Now working on trinary
binary marked as complete
```

## Contributing

Pull requests to add cloister in new languages or improve existing ones are very welcome.

Look at [CONTRIBUTING.md](CONTRIBUTING.md) to learn the technical requirements.

Participating is subject to the [Contributor Covenant](https://www.contributor-covenant.org/version/1/4/code-of-conduct/). Check [my website](https://seamusjohnston.com) for contact info if you need to flag something.

## Why This?

This little side project of mine is not meant to detract from the community of people using the official website. If the official site works for you, please use that!

I wrote this because some years ago (you may recall), the site was totally redesigned. It felt to many of us that our community space had been uprooted with little input. Where mentoring on the old site had been a pleasure for me, it was literally impossible on the new site due to [accessibility issues](https://github.com/exercism/exercism/issues/4237).

After giving the new site a good faith try for a short while, I gave up.

I still loved the concept behind the exercises, though. Real code. Real tests. Real dev tools. Most sites give you a "sandbox" but Exercism gave you the real experience of being a developer.

I want to see the exercises maintained and flourish, no matter what becomes of the website. Making this little project public is my (hopeful) contribution to that.

## List of Exercism tracks

- [05ab1e](https://github.com/exercism/05ab1e)
- [Ada](https://github.com/exercism/ada)
- [Arm64-assembly](https://github.com/exercism/arm64-assembly)
- [Ballerina](https://github.com/exercism/ballerina)
- [Bash](https://github.com/exercism/bash)
- [C](https://github.com/exercism/c)
- [C#](https://github.com/exercism/csharp)
- [C++](https://github.com/exercism/cpp)
- [Ceylon](https://github.com/exercism/ceylon)
- [CFML](https://github.com/exercism/cfml)
- [Clojure](https://github.com/exercism/clojure)
- [Clojurescript](https://github.com/exercism/clojurescript)
- [CoffeeScript](https://github.com/exercism/coffeescript)
- [Common Lisp](https://github.com/exercism/common-lisp)
- [Coq](https://github.com/exercism/coq)
- [Crystal](https://github.com/exercism/crystal)
- [D](https://github.com/exercism/d)
- [Dart](https://github.com/exercism/dart)
- [Delphi Pascal](https://github.com/exercism/delphi)
- [Elixir](https://github.com/exercism/elixir)
- [Elm](https://github.com/exercism/elm)
- [Emacs Lisp](https://github.com/exercism/emacs-lisp)
- [Erlang](https://github.com/exercism/erlang)
- [F#](https://github.com/exercism/fsharp)
- [Factor](https://github.com/exercism/factor)
- [Forth](https://github.com/exercism/forth)
- [Fortran](https://github.com/exercism/fortran)
- [Gleam](https://github.com/exercism/gleam)
- [GNU APL](https://github.com/exercism/gnu-apl)
- [Go](https://github.com/exercism/go)
- [Groovy](https://github.com/exercism/groovy)
- [Haskell](https://github.com/exercism/haskell)
- [Haxe](https://github.com/exercism/haxe)
- [Idris](https://github.com/exercism/idris)
- [Io](https://github.com/exercism/io)
- [J](https://github.com/exercism/j)
- [Java](https://github.com/exercism/java)
- [Javascript](https://github.com/exercism/javascript)
- [Julia](https://github.com/exercism/julia)
- [Kotlin](https://github.com/exercism/kotlin)
- [Lisp Flavoured Erlang (LFE)](https://github.com/exercism/lfe)
- [Lua](https://github.com/exercism/lua)
- [MIPS Assembly](https://github.com/exercism/mips)
- [Nim](https://github.com/exercism/nim)
- [Nix](https://github.com/exercism/nix)
- [Objective-C](https://github.com/exercism/objective-c)
- [OCaml](https://github.com/exercism/ocaml)
- [Perl 5](https://github.com/exercism/perl)
- [Perl 6](https://github.com/exercism/raku)
- [Pharo-smalltalk](https://github.com/exercism/pharo-smalltalk)
- [PHP](https://github.com/exercism/php)
- [PL/SQL](https://github.com/exercism/plsql)
- [Pony](https://github.com/exercism/pony)
- [Prolog](https://github.com/exercism/prolog)
- [PureScript](https://github.com/exercism/purescript)
- [Python](https://github.com/exercism/python)
- [R](https://github.com/exercism/r)
- [Racket](https://github.com/exercism/racket)
- [Reasonml](https://github.com/exercism/reasonml)
- [Research_experiment_](https://github.com/exercism/research_experiment_)
- [Ruby](https://github.com/exercism/ruby)
- [Rust](https://github.com/exercism/rust)
- [Scala](https://github.com/exercism/scala)
- [Scheme](https://github.com/exercism/scheme)
- [Shen](https://github.com/exercism/shen)
- [Standard ML](https://github.com/exercism/sml)
- [Swift](https://github.com/exercism/swift)
- [System-verilog](https://github.com/exercism/system-verilog)
- [Tcl](https://github.com/exercism/tcl)
- [TypeScript](https://github.com/exercism/typescript)
- [VB.NET](https://github.com/exercism/vbnet)
- [Vim script](https://github.com/exercism/vimscript)
- [Windows PowerShell](https://github.com/exercism/powershell)
- [X86-64-assembly](https://github.com/exercism/x86-64-assembly)

If you don't see your pick on this list, try searching the [Exercism repo](https://github.com/exercism). It may have been added since.
