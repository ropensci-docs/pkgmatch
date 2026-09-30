# Generate example data to use with pkgmatch

This function generates a selection of test data for the "cran" corpus,
to allow functions to be run offline, without having to download the
large datasets otherwise required for the package to function.

Note that these data are randomly generated, and results will be
generally meaningless. They are generated solely to demonstrate how the
package functions, and are not intended to derive meaningful outputs.

## Usage

``` r
generate_pkgmatch_example_data(corpus = "cran")
```

## Arguments

- corpus:

  One of "ropensci" or "cran", where "ropensci" generates additional
  data on function call frequencies.

## Value

(Invisibly) The path to the temporary directory containing the package
data.

## See also

Other utils:
[`head.pkgmatch()`](https://docs.ropensci.org/pkgmatch/reference/head.pkgmatch.md),
[`pkgmatch_browse()`](https://docs.ropensci.org/pkgmatch/reference/pkgmatch_browse.md),
[`pkgmatch_load_data()`](https://docs.ropensci.org/pkgmatch/reference/pkgmatch_load_data.md),
[`pkgmatch_update_cache()`](https://docs.ropensci.org/pkgmatch/reference/pkgmatch_update_cache.md),
[`print.pkgmatch()`](https://docs.ropensci.org/pkgmatch/reference/print.pkgmatch.md)

## Examples

``` r
generate_pkgmatch_example_data ()
input <- "curl" # Name of a single installed package
pkgmatch_similar_pkgs (input, corpus = "cran")
#> [1] "httr"       "AmpGram"    "CancerGram" "crul"       "curl"      
```
