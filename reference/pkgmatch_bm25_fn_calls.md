# The "Best Matching 25" (BM25) ranking function for function calls

See
[`?pkgmatch_bm25`](https://docs.ropensci.org/pkgmatch/reference/pkgmatch_bm25.md)
for details of BM25 ranks. This function calculates "BM25" ranks from
function-call frequencies between a local R package and all packages in
specified corpus. Values are thus higher for packages with similar
patterns of function calls, weighted by inverse frequencies, so
functions called infrequently across the entire corpus contribute more
than common functions.

Note that the results of this function are entirely different from
[pkgmatch_bm25](https://docs.ropensci.org/pkgmatch/reference/pkgmatch_bm25.md)
with `corpus = "ropensci-fns"` or `corpus = "bioc-fns"`. The latter
return BM25 values from text descriptions of all functions in all
rOpenSci or BioConductor packages, whereas this function returns BM25
values based on frequencies of function calls within packages.

## Usage

``` r
pkgmatch_bm25_fn_calls(path, corpus = NULL)
```

## Arguments

- path:

  Local path to source code of an R package.

- corpus:

  One of "ropensci" or "cran"

## Value

A `data.frame` of two columns:

- "package" Naming the package from the specified corpus;

- bm25 The "BM25" index value for the nominated packages, where high
  values indicate greater overlap in term frequencies.

## See also

Other bm25:
[`pkgmatch_bm25()`](https://docs.ropensci.org/pkgmatch/reference/pkgmatch_bm25.md)

## Examples

``` r
corpus <- "ropensci"
flist <- generate_pkgmatch_example_data (corpus = corpus)
# \donttest{
pkgmatch_bm25_fn_calls (path = "cli", corpus = corpus)
#>      package      bm25
#> 1        cli 745.56676
#> 2       httr  80.28750
#> 3         fs  76.71897
#> 4       curl  70.05386
#> 5    memoise  39.04868
#> 6 tokenizers  14.02283
# }
```
