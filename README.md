
# cran_pkgs

<!-- badges: start -->
<!-- badges: end -->

## CRAN Packages for which I am the maintainer

[GitHub Actions](https://github.com/jonocarroll/cran_pkgs/actions) is used to check the CRAN checks status for all of my packages

| CRAN Package | version / status | checks status | checks link | downloads |
| :----------: | :--------------: | :-----------: | :---------: | :-------: |
| [{ggeasy}](https://cran.r-project.org/package=ggeasy)   | ![](https://www.r-pkg.org/badges/version/ggeasy)  | ![](https://github.com/jonocarroll/cran_pkgs/actions/workflows/check_ggeasy.yaml/badge.svg) | [{ggeasy}](https://cran.r-project.org/web/checks/check_results_ggeasy.html) | ![](https://cranlogs.r-pkg.org/badges/grand-total/ggeasy) |
| [{mathpix}](https://cran.r-project.org/package=mathpix) | ![](https://www.r-pkg.org/badges/version/mathpix) | ![](https://github.com/jonocarroll/cran_pkgs/actions/workflows/check_mathpix.yaml/badge.svg) | [{mathpix}](https://cran.r-project.org/web/checks/check_results_mathpix.html) | ![](https://cranlogs.r-pkg.org/badges/grand-total/mathpix) |
| [{ggghost}](https://cran.r-project.org/package=ggghost) | ![](https://www.r-pkg.org/badges/version/ggghost) | ![](https://github.com/jonocarroll/cran_pkgs/actions/workflows/check_ggghost.yaml/badge.svg) | [{ggghost}](https://cran.r-project.org/web/checks/check_results_ggghost.html) | ![](https://cranlogs.r-pkg.org/badges/grand-total/ggghost) |
| [{ntfy}](https://cran.r-project.org/package=ntfy) | ![](https://www.r-pkg.org/badges/version/ntfy) | ![](https://github.com/jonocarroll/cran_pkgs/actions/workflows/check_ntfy.yaml/badge.svg) | [{ntfy}](https://cran.r-project.org/web/checks/check_results_ntfy.html) | ![](https://cranlogs.r-pkg.org/badges/grand-total/ntfy) |
| [{charcuterie}](https://cran.r-project.org/package=charcuterie) | ![](https://www.r-pkg.org/badges/version/charcuterie) | ![](https://github.com/jonocarroll/cran_pkgs/actions/workflows/check_charcuterie.yaml/badge.svg) | [{charcuterie}](https://cran.r-project.org/web/checks/check_results_charcuterie.html) | ![](https://cranlogs.r-pkg.org/badges/grand-total/charcuterie) |

<details>
  <summary>Find all maintained packages</summary>
  
```
library(cranly)
cran_db <- clean_CRAN_db()
package_network <- build_network(cran_db)

package_network$nodes |> 
   dplyr::filter(grepl("rpkg@jcarroll.com.au", email)) |> 
   dplyr::select(package, version, doi)
```
</details>

## CRAN Packages for which I am a contributor, not the maintainer

I have contributed to these, but I am not the maintainer

| CRAN Package | version / status | 
| :----------: | :--------------: | 
| [{datapasta}](https://cran.r-project.org/package=datapasta) | ![](https://www.r-pkg.org/badges/version/datapasta) |
| [{weatherOz}](https://cran.r-project.org/package=weatherOz) | ![](https://www.r-pkg.org/badges/version/weatherOz) |
| [{remedy}](https://cran.r-project.org/package=remedy) | ![](https://www.r-pkg.org/badges/version/remedy) |
| [{csvy}](https://cran.r-project.org/package=csvy) | ![](https://www.r-pkg.org/badges/version/csvy) |
| [{tidyRSS}](https://cran.r-project.org/package=tidyRSS) | ![](https://www.r-pkg.org/badges/version/tidyRSS) |
| [{wakefield}](https://cran.r-project.org/package=wakefield) | ![](https://www.r-pkg.org/badges/version/wakefield) |
| [{chessR}](https://cran.r-project.org/package=chessR) (archived) | ![](https://www.r-pkg.org/badges/version/chessR) |
| [{bomrang}](https://cran.r-project.org/package=bomrang) (archived) | ![](https://www.r-pkg.org/badges/version/bomrang) |

<details>
  <summary>Find all contributions</summary>
  
```
library(cranly)
cran_db <- clean_CRAN_db()
package_network <- build_network(cran_db)

# requires manual inspection for false positives
package_network$nodes |> 
    dplyr::filter(grepl("carroll", `authors@r`, ignore.case = TRUE)) |> 
    dplyr::select(package, `authors@r`)
```
</details>
