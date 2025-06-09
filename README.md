This reproduces a bug in templ I reported at https://github.com/a-h/templ/issues/1182.
The bug is actuaLly a little worse than I thought,
it seems like a trailing comment before an `else` 
breaks parsing.
