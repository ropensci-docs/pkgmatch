# Head method for 'pkgmatch' objects

Head method for 'pkgmatch' objects

## Usage

``` r
# S3 method for class 'pkgmatch'
head(x, n = 5L, ...)
```

## Arguments

- x:

  Object for which head is to be printed

- n:

  Number of rows of full `pkgmatch` object to be displayed

- ...:

  Not used

## Value

A (usually) smaller version of `x`, with all columns displayed.

## See also

Other utils:
[`generate_pkgmatch_example_data()`](https://docs.ropensci.org/pkgmatch/reference/generate_pkgmatch_example_data.md),
[`pkgmatch_browse()`](https://docs.ropensci.org/pkgmatch/reference/pkgmatch_browse.md),
[`pkgmatch_load_data()`](https://docs.ropensci.org/pkgmatch/reference/pkgmatch_load_data.md),
[`pkgmatch_update_cache()`](https://docs.ropensci.org/pkgmatch/reference/pkgmatch_update_cache.md),
[`print.pkgmatch()`](https://docs.ropensci.org/pkgmatch/reference/print.pkgmatch.md)

## Examples

``` r
corpus <- "cran"
generate_pkgmatch_example_data (corpus = corpus)
input <- "Download open spatial data from NASA"
p <- pkgmatch_similar_pkgs (input, corpus = corpus)
head (p) # Shows first 5 rows of full `data.frame` object
#>     package version rank
#> 1      crul   1.5.0    1
#> 2       ssh   0.9.3    2
#> 3      httr   1.4.7    3
#> 4     RCurl    1.98    4
#> 5 mRpostman   1.1.4    5
```
