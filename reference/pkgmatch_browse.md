# Open web pages for `pkgmatch` results

Open web pages for `pkgmatch` results

## Usage

``` r
pkgmatch_browse(p, n = NULL)
```

## Arguments

- p:

  A `pkgmatch` object returned from
  [pkgmatch_similar_pkgs](https://docs.ropensci.org/pkgmatch/reference/pkgmatch_similar_pkgs.md).

- n:

  Number of top-matching entries which should be opened. Defaults to the
  value passed to the main functions.

## Value

(Invisibly) A named vector of integers, with 0 for all pages able to be
successfully opened, and 1 otherwise.

## See also

Other utils:
[`generate_pkgmatch_example_data()`](https://docs.ropensci.org/pkgmatch/reference/generate_pkgmatch_example_data.md),
[`head.pkgmatch()`](https://docs.ropensci.org/pkgmatch/reference/head.pkgmatch.md),
[`pkgmatch_load_data()`](https://docs.ropensci.org/pkgmatch/reference/pkgmatch_load_data.md),
[`pkgmatch_update_cache()`](https://docs.ropensci.org/pkgmatch/reference/pkgmatch_update_cache.md),
[`print.pkgmatch()`](https://docs.ropensci.org/pkgmatch/reference/print.pkgmatch.md)

## Examples

``` r
input <- "genomics and transcriptomics sequence data"
# \donttest{
p <- pkgmatch_similar_pkgs (input, corpus = "ropensci")
# }
if (FALSE) { # \dontrun{
pkgmatch_browse (p) # Open main package pages on rOpenSci
} # }
# \donttest{
p <- pkgmatch_similar_pkgs (input, corpus = "cran")
# }
if (FALSE) { # \dontrun{
pkgmatch_browse (p) # Open main package pages on CRAN
} # }
```
