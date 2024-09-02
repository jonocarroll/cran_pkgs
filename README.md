
# cran_pkgs

<!-- badges: start -->
<!-- badges: end -->

## CRAN Packages for which I am the maintainer

GitHub Actions is used to check the CRAN checks status for all of my packages

- [{ggeasy}](https://cran.r-project.org/package=ggeasy)
- [{ggghost}](https://cran.r-project.org/package=ggghost)
- [{mathpix}](https://cran.r-project.org/package=mathpix)

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

- [{datapasta}](https://cran.r-project.org/package=datapasta)
- [{weatherOz}](https://cran.r-project.org/package=weatherOz)
- [{remedy}](https://cran.r-project.org/package=remedy)
- [{csvy}](https://cran.r-project.org/package=csvy)
- [{tidyRSS}](https://cran.r-project.org/package=tidyRSS)
- [{wakefield}](https://cran.r-project.org/package=wakefield)
- [{chessR}](https://cran.r-project.org/package=chessR) (archived)
- [{bomrang}](https://cran.r-project.org/package=bomrang) (archived)

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
