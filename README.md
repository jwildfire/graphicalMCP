
<!-- README.md is generated from README.Rmd. Please edit that file -->
<!-- badges: start -->

[![CRAN
status](https://www.r-pkg.org/badges/version/graphicalMCP)](https://cran.r-project.org/package=graphicalMCP)
[![R-CMD-check](https://github.com/Gilead-BioStats/graphicalMCP/workflows/R-CMD-check-main/badge.svg)](https://github.com/Gilead-BioStats/graphicalMCP/actions)
[![Codecov test
coverage](https://codecov.io/gh/Gilead-BioStats/graphicalMCP/branch/s3-graph_mcp/graph/badge.svg)](https://app.codecov.io/gh/Gilead-BioStats/graphicalMCP?branch=s3-graph_mcp)
<!-- badges: end -->

## Introduction

A multiple comparison procedure (MCP) is a statistical analysis method
that allows for assessing the efficacy of multiple endpoints, some of
which are dependent on each other, in a single clinical trial. Endpoints
can be different doses, treatment of different conditions, or combined
superiority & non-inferiority testing.

In [Bretz et al
(2011)](https://onlinelibrary.wiley.com/doi/10.1002/bimj.201000239), a
graphical method to MCPs was described, which separates the weighting of
the dependency graph from the particular statistical test used to assess
each endpoint. This package is a low-dependency implementation of those
methods.

## Installation

graphicalMCP is not on CRAN, so install it from GitHub with

``` r
# install.packages("pak")
pak::pak("Gilead-BioStats/graphicalMCP")
```

## Basic usage

The base object in graphicalMCP is an `mcp_graph`, which is a weighted,
directed graph represented by a matrix of transition (edge) weights, and
a vector of hypothesis (vertex) weights.

``` r
library(graphicalMCP)

transitions <- rbind(
  c(0, .5, .5),
  c(.5, 0, .5),
  c(.5, .5, 0)
)
hypotheses <- rep(.333333, 3)

g_dose <- graph(hypotheses, transitions, paste("dose", letters[1:3]))

g_dose
#> An mcp_graph
#> 
#> --- Hypothesis names ---
#> H1: dose a
#> H2: dose b
#> H3: dose c
#> 
#> --- Hypothesis weights ---
#> dose a: (0.3333)
#> dose b: (0.3333)
#> dose c: (0.3333)
#> 
#> --- Transition weights ---
#>        dose a dose b dose c
#> dose a   --   0.5000 0.5000
#> dose b 0.5000   --   0.5000
#> dose c 0.5000 0.5000   --
```

## Related work

These methods were originally implemented in R after the 2011 paper in
the gMCP package, which is still available on CRAN today:

- `install.packages("gMCP")`
- <https://github.com/kornl/gMCP>

However, because development has ceased on this original package, we
hope to re-implement the methods with a clearer distinction between
weighting procedures and test procedures; with fewer dependencies, in
particular shedding the Java dependency; with the simpler, more
transparent S3 class framework; and with improvements to the accuracy of
the parametric tests method.
