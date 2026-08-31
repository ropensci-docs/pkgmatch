# Print method for 'pkgmatch' objects

The main `pkgmatch` function,
[pkgmatch_similar_pkgs](https://docs.ropensci.org/pkgmatch/reference/pkgmatch_similar_pkgs.md),
returns `data.frame` objects of class "pkgmatch". This class exists
primarily to enable this print method, which summarises by default the
top 5 matching packages or functions. Objects can be converted to
standard `data.frame`s with
[`as.data.frame()`](https://rdrr.io/r/base/as.data.frame.html).

## Usage

``` r
# S3 method for class 'pkgmatch'
print(x, ...)
```

## Arguments

- x:

  Object to be printed

- ...:

  Additional parameters passed to default 'print' method.

## Value

The result of printing `x`, in form of either a single character vector,
or a named list of character vectors.

## See also

Other utils:
[`generate_pkgmatch_example_data()`](https://docs.ropensci.org/pkgmatch/reference/generate_pkgmatch_example_data.md),
[`head.pkgmatch()`](https://docs.ropensci.org/pkgmatch/reference/head.pkgmatch.md),
[`pkgmatch_browse()`](https://docs.ropensci.org/pkgmatch/reference/pkgmatch_browse.md),
[`pkgmatch_load_data()`](https://docs.ropensci.org/pkgmatch/reference/pkgmatch_load_data.md),
[`pkgmatch_update_cache()`](https://docs.ropensci.org/pkgmatch/reference/pkgmatch_update_cache.md)

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
p # Default print method, lists 5 best matching packages
#> [1] "crul"      "ssh"       "httr"      "RCurl"     "mRpostman"
```
