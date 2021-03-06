swapview is a simple program to view processes' swap usage on Linux. This is intended to be a lilydjwg's version of Hello World program.

How to play
----

Install all the dependencies for your interested versions, then run `make -k`. It will build all that can be built.

To test and see the speed comparison, either use `bench.py` or `run_benchmark`. `bench.py` uses Python 3.4+ and depends on `python-toml`.

`run_benchmark` is a Rust version. Install latest Rust and Cargo, then change your working directory to `benchmark` and run `cargo build --release`. If the build fails, it's because your Rust is too old or too new....

Run `./run_benchmark <benchmark.toml` and wait for it to finish. Failed ones (e.g. because you don't have the dependencies installed) will be marked as failed so you don't need to edit `benchmark.toml` to disable the ones you can't run.

You can give `./run_benchmark` names to selectively run some versions, e.g.

    ./run_benchmark C C++14 'Rust*' <benchmark.toml

Implementions and their requirements
----

Of course you should have corresponding compilers / interpreters installed.
You can (edit and then) run `make` to build all that needs to be built.

* Bash
* Bash_parallel, Bash version using GNU parallel
* C
* C++98
* C++98_omp, openmp paralleled version
* C++14
* C++14_boost, C++ version using the boost library
* CSharp (mono)
* Chicken, format (will be installed by `make`)
* CommonLisp_opt, sbcl
* CommonLisp_old, sbcl, maynbe others also work
* CoffeeScript, requires promise (will be installed by `make`)
* CoffeeScript_parallel, a parallel version, requires promise (will be installed by `make`)
* D, `dmd` or `ldmd` (LLVM version)
* Elixir
* Erlang
* Go
* Guile, tested with 2.0.11
* Haskell, requires `strict` (install from `aur/haskell-strict` or `haskell-core/haskell-strict` or by `cabal install strict`)
* Haskell2, another better Haskell version using more dependencies
* Java, >= Java 8
* Lua, requires lua-filesystem, works with 5.1, 5.2 and LuaJIT
* NodeJS, requires sprintf (will be installed by `make`)
* NodeJS_async, another NodeJS version which use async I/O, requires sprintf and async (will be installed by `make`)
* OCaml
* FreePascal
* Perl
* Python, works with Python 2 & 3
* Python3_bytes
* R
* Racket
* Ruby
* Rust, use git version please
* Scala 2.11.6
* Vala, requires `glib2` (`libglib-2.0` and `libgio-2.0`)
* Tcl, >= 8.6

Contributions
----

Contributions are welcome! Improve current ones, or submit new one. But make
sure your implementations meet the following requirements:

1. Must be readable and maintainable
2. Output exact the same format as other versions (but sorting may be
   unstable)
3. Try to be efficient
4. Please include a `Makefile` if appropriate
5. Don't forget to tell the compiler to optimize
