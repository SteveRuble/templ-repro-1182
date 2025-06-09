This reproduces a bug in templ I reported at https://github.com/a-h/templ/issues/1182.
The bug is actuaLly a little worse than I thought,
it seems like a trailing comment before an `else` 
breaks parsing.

I've been running `templ` using

```shell
go run github.com/a-h/templ/cmd/templ generate
```

but the bug also reproduces with the `templ` binary installed in `PATH`.

The error is:
```shell
(✗) Error [ error=failed to generate code for "/Users/steve.ruble/src/github.com/SteveRuble/templ-repro-1182/repro.templ": /Users/steve.ruble/src/github.com/SteveRuble/templ-repro-1182/repro.templ parsing error: string expression: missing close brace: line 10, col 2 ]
```
