# Update all locally-cached `pkgmatch` data to latest versions.

This function forces all locally-cached data to be updated with latest
version of remote data provided on the latest release of GitHub
repository at
<https://github.com/ropensci-review-tools/pkgmatch/releases>.

Caching strategies are described in the "*Data Caching and Updating*"
vignette, accessible either locally via
`vignette("data-caching-and-updating", package = "pkgmatch")`, or online
at
<https://docs.ropensci.org/pkgmatch/articles/B_data-caching-and-updating.html>.
In short, locally-cached data used by this package are updated by
default every 30 days (with the vignette describing how to modify this
default behaviour). This function forces all locally-cached data to be
updated, regardless of update frequencies.

## Usage

``` r
pkgmatch_update_cache()
```

## Value

(Invisibly) A list of full local paths to all files which were updated.

## See also

Other utils:
[`generate_pkgmatch_example_data()`](https://docs.ropensci.org/pkgmatch/reference/generate_pkgmatch_example_data.md),
[`head.pkgmatch()`](https://docs.ropensci.org/pkgmatch/reference/head.pkgmatch.md),
[`pkgmatch_browse()`](https://docs.ropensci.org/pkgmatch/reference/pkgmatch_browse.md),
[`pkgmatch_load_data()`](https://docs.ropensci.org/pkgmatch/reference/pkgmatch_load_data.md),
[`print.pkgmatch()`](https://docs.ropensci.org/pkgmatch/reference/print.pkgmatch.md)

## Examples

``` r
if (FALSE) { # \dontrun{
pkgmatch_update_cache ()
} # }
```
