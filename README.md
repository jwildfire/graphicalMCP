
<!-- README.md is generated from README.Rmd. Please edit that file -->
<!-- badges: start -->

[![CRAN
status](https://www.r-pkg.org/badges/version/graphicalMCP)](https://cran.r-project.org/package=graphicalMCP)

<!-- badges: end -->

# graphicalMCP <a href="https://urban-sniffle-p11zlpj.pages.github.io/"><img src="man/figures/logo.png" align="right" height="139" /></a>

## Introduction

Graphical approaches for multiple comparison procedures (MCPs) are a
general framework to control the family-wise error rate strongly at a
pre-specified significance level $0<\alpha<1$. This approach includes
many commonly used MCPs as special cases and is transparent in
visualizing MCPs for better communications. `graphicalMCP` is designed
to design and analyze graphical MCPs in a flexible, informative and
efficient way.

## Installation

`graphicalMCP` is currently not on CRAN but can be installed from GitHub
using the following code:

``` r
# install.packages("pak")
pak::pak("Gilead-BioStats/graphicalMCP@dev")
```

## Documentation

- For basic usage instructions, see `vignette("graphicalMCP")`
- To become familiar with graphical MCP terminology, see
  `vignette("glossary")`
- To learn examples of how to use `graphicalMCP`,
  - see `vignette("shortcut-testing")` for sequentially rejective
    graphical multiple comparison procedures based on Bonferroni tests
  - see `vignette("closed-testing")` for graphical multiple comparison
    procedures based on the closure principle
  - see `vignette("graph-examples")` for common multiple comparison
    procedures illustrated using `graphicalMCP`
  - see `vignette("generate-closure")` for rationales to generate the
    closure and the weighting strategy of a graph
  - see `vignette("comparison")` for comparisons to other R packages

## Related work

- Graphical MCPs - [gMCP](https://cran.r-project.org/package=gMCP)
- Lighter version of `gMCP` which removes the rJava dependency -
  [gMCPLite](https://cran.r-project.org/package=gMCPLite)
- Graphical MCPs with Simes tests -
  [lrstat](https://cran.r-project.org/package=lrstat)

Built upon these packages, we hope to implement graphical MCPs in a more
general framework, with fewer dependencies and simpler S3 classes, and
without losing computational efficiency.

## Related work

- Graphical MCPs [gMCP](https://cran.r-project.org/package=gMCP)
- Lighter version of `gMCP` which removes the rJava dependency
  [gMCPLite](https://cran.r-project.org/package=gMCPLite)
- Graphical MCPs with Simes tests
  [lrstat](https://cran.r-project.org/package=lrstat)

Built upon these packages, we hope to implement graphical MCPs in a more
general framework, with fewer dependencies and simpler S3 classes, and
without losing computational efficiency.

## Citation

``` r
citation("graphicalMCP")
#> 
#> To cite graphicalMCP in publications use:
#> 
#>   Xi, D.; Brockmann, E. (2023). graphicalMCP: Graph-based multiple
#>   comparison procedures. version 0.1.0. Gilead Sciences, Inc. Foster
#>   City, California. https://github.com/Gilead-BioStats/graphicalMCP
#> 
#>   Frank Bretz, Martin Posch, Ekkehard Glimm, Florian Klinglmueller,
#>   Willi Maurer, Kornelius Rohmeyer (2011), Graphical approaches for
#>   multiple comparison procedures using weighted Bonferroni, Simes or
#>   parametric tests. Biometrical Journal 53 (6), pages 894--913, Wiley.
#> 
#> To see these entries in BibTeX format, use 'print(<citation>,
#> bibtex=TRUE)', 'toBibtex(.)', or set
#> 'options(citation.bibtex.max=999)'.
```

## Acknowledgments

Along with the authors and contributors, thanks to the following people
for their suggestions and inspirations on the package: Frank Bretz,
Willi Maurer, Ekkehard Glimm, Nan Chen, Jeremy Wildfire, Spencer
Childress, Colleen McLaughlin, Matt Roumaya, Chelsea Dickens, and Ron Yu

We owe a debt of gratitude to the authors of
[gMCP](https://cran.r-project.org/package=gMCP) for their pioneering
work, without which this package would not be nearly as extensive as it
is.
