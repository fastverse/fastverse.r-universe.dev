# fastverse R-universe

[![:name status badge](https://fastverse.r-universe.dev/badges/:name)](https://fastverse.r-universe.dev/)
[![:packages status badge](https://fastverse.r-universe.dev/badges/:packages)](https://fastverse.r-universe.dev/)

This [R-universe](https://r-universe.dev) repository provides development versions of high-performance R packages for statistical computing and data manipulation, built daily from their GitHub sources for all major platforms (Windows, macOS, Linux).

🌐 **Browse packages:** <https://fastverse.r-universe.dev>

## Installation

Install any package from this universe by adding `https://fastverse.r-universe.dev` to your repos:

```r
install.packages("collapse", repos = c("https://fastverse.r-universe.dev", "https://cloud.r-project.org"))
```

To install multiple packages:

```r
install.packages(
  c("collapse", "data.table", "kit", "fastverse"),
  repos = c("https://fastverse.r-universe.dev", "https://cloud.r-project.org")
)
```

### Set as Default Repository

Add to your `~/.Rprofile` to always use this universe:

```r
options(repos = c(
  fastverse = "https://fastverse.r-universe.dev",
  CRAN = "https://cloud.r-project.org"
))
```

## Core Packages

The [*fastverse*](https://fastverse.github.io/fastverse/) installs with 4 core packages (5 dependencies in total) which provide broad C/C++ based statistical and data manipulation functionality and have carefully managed APIs:

- **[data.table](https://github.com/Rdatatable/data.table)**: Enhanced data frame class with concise data manipulation framework offering powerful aggregation, update, reshaping, (rolling) joins, rolling statistics, set operations on tables, fast csv read/write, and various utilities such as data transposition/stringsplit-transpose.

- **[collapse](https://github.com/SebKrantz/collapse)**: Fast grouped and weighted statistical computations, time series and panel data transformations, list-processing, data manipulation functions (incl. fast joins and pivots), summary statistics, and various utilities for efficient programming. Class-agnostic framework designed to work with vectors, matrices, data frames, lists and related classes including *xts*, *data.table*, *tibble*, and *sf*.

- **[kit](https://github.com/fastverse/kit)**: Parallel (row-wise) statistical functions, vectorized and nested switches, and some utilities such as efficient partial sorting.

- **[magrittr](https://github.com/tidyverse/magrittr)**: Efficient pipe operators and aliases for enhanced R programming and code un-nesting.

## Suggested Extensions

The packages below can extend the core *fastverse* and are also available from this repository.

### Time Series

| Package | Description |
|---------|-------------|
| [xts](https://github.com/joshuaulrich/xts) | Extensible time series class and methods |
| [roll](https://github.com/jasonjfoster/roll) | Rolling and expanding statistics using parallel algorithms |

### Dates and Times

| Package | Description |
|---------|-------------|
| [fasttime](https://github.com/s-u/fasttime) | Fast utility function for parsing date-time strings |
| [lubridate](https://github.com/tidyverse/lubridate) | Functions to work with date-times and time-spans |
| [clock](https://github.com/r-lib/clock) | Comprehensive library for date-time manipulations |
| [anytime](https://github.com/eddelbuettel/anytime) | Parse anything into date-time |
| [nanotime](https://github.com/eddelbuettel/nanotime) | Nanosecond-resolution time for R |
| [timechange](https://github.com/vspinu/timechange) | Efficient manipulation of date-times |

### Strings

| Package | Description |
|---------|-------------|
| [stringi](https://github.com/gagolews/stringi) | Fast and portable character string processing |
| [stringfish](https://github.com/traversc/stringfish) | Alt-rep string vectors for performant string storage |
| [stringdist](https://github.com/markvanderloo/stringdist) | Approximate string matching and string distance functions |
| [snakecase](https://github.com/Tazinho/snakecase) | Convert strings to any case |

### Statistics and Computing

| Package | Description |
|---------|-------------|
| [matrixStats](https://github.com/HenrikBengtsson/matrixStats) | Functions operating on rows and columns of matrices |
| [Rfast](https://github.com/RfastOfficial/Rfast) | Collection of efficient and fast R functions |
| [Rfast2](https://github.com/RfastOfficial/Rfast2) | Collection of efficient and fast R functions (2) |
| [fastmatrix](https://github.com/faosorios/fastmatrix) | Fast computation of matrix operations |
| [matrixTests](https://github.com/karoliskoncevicius/matrixTests) | Fast statistical hypothesis tests on matrix rows/columns |
| [parallelDist](https://github.com/alexeckert/parallelDist) | Parallel distance matrix computation |
| [coop](https://github.com/wrathematics/coop) | Fast covariance, correlation, and cosine similarity |
| [RcppAlgos](https://github.com/jwood000/RcppAlgos) | High-performance combinatorics and computational mathematics |
| [dqrng](https://github.com/daqana/dqrng) | Fast pseudo-random number generators |
| [cheapr](https://github.com/NicChr/cheapr) | Memory-efficient R functions |
| [SLmetrics](https://github.com/serkor1/SLmetrics) | Machine learning evaluation metrics |
| [vctrs](https://github.com/r-lib/vctrs) | Vector helpers |
| [broadcast](https://github.com/tony-aw/broadcast) | Broadcasting operations |
| [rrapply](https://github.com/JorisChau/rrapply) | Recursive apply for nested lists |
| [fastmatch](https://github.com/s-u/fastmatch) | Fast `match()` function |
| [fastmap](https://github.com/r-lib/fastmap) | Fast hash maps |
| [collections](https://github.com/randy3k/collections) | High-performance container data types |
| [stdvectors](https://github.com/digEmAll/stdvectors) | C++ vector types in R |
| [MatrixExtra](https://github.com/david-cortes/MatrixExtra) | Extra methods for sparse matrices |
| [hutilscpp](https://github.com/hughparsonage/hutilscpp) | Miscellaneous C++ utilities |
| [fst](https://github.com/fstpackage/fst) | Lightning fast serialization of data frames |
| [qs](https://github.com/traversc/qs) | Quick serialization of R objects |
| [vroom](https://github.com/tidyverse/vroom) | Fast reading of delimited files |
| [arrow](https://github.com/apache/arrow) | Integration with Apache Arrow |
| [polars](https://github.com/pola-rs/r-polars) | Lightning-fast DataFrame library |
| [duckplyr](https://github.com/tidyverse/duckplyr) | DuckDB-backed dplyr |
| [fixest](https://github.com/lrberge/fixest) | Fast fixed-effects estimations |
| [mirai](https://github.com/shikokuchuo/mirai) | Minimalist async evaluation framework |

### Spatial

| Package | Description |
|---------|-------------|
| [sf](https://github.com/r-spatial/sf) | Simple features for R |
| [geos](https://github.com/paleolimbot/geos) | Open source geometry engine |
| [terra](https://github.com/rspatial/terra) | Spatial data analysis |
| [stars](https://github.com/r-spatial/stars) | Spatiotemporal arrays |
| [s2](https://github.com/r-spatial/s2) | Spherical geometry operators |
| [dggridR](https://github.com/SebKrantz/dggridR) | Discrete global grids |
| [exactextractr](https://github.com/isciences/exactextractr) | Fast extraction from rasters |
| [geodist](https://github.com/hypertidy/geodist) | Fast geodesic distances |
| [cppRouting](https://github.com/vlarmet/cppRouting) | Fast algorithms for routing and shortest paths |
| [igraph](https://github.com/igraph/rigraph) | Network analysis and visualization |

### Visualization

| Package | Description |
|---------|-------------|
| [tinyplot](https://github.com/grantmcdermott/tinyplot) | Lightweight extension of base R graphics |
| [ggplot2](https://github.com/tidyverse/ggplot2) | Create elegant data visualizations |
| [lattice](https://github.com/deepayan/lattice) | Trellis graphics for R |
| [scales](https://github.com/r-lib/scales) | Scale functions for visualization |
| [scattermore](https://github.com/exaexa/scattermore) | Very fast scatterplots for millions of points |
| [ggrastr](https://github.com/VPetukhov/ggrastr) | Rasterize ggplot2 layers for large data |

### Speeding up R

| Package | Description |
|---------|-------------|
| [inline](https://github.com/eddelbuettel/inline) | Functions to inline C, C++, Fortran code in R |
| [ast2ast](https://github.com/Konrad1991/ast2ast) | Translate R to C++ |
| [r2c](https://github.com/brodieG/r2c) | Fast grouped-operations through compilation |
| [odin](https://github.com/mrc-ide/odin) | ODE generation and compilation |
| [quickr](https://github.com/t-kalinowski/quickr) | R to Fortran transpiler |

### R Bindings to Faster Languages

| Package | Description |
|---------|-------------|
| [Rcpp](https://github.com/RcppCore/Rcpp) | Seamless R and C++ integration |
| [cpp11](https://github.com/r-lib/cpp11) | A header-only C++11 interface for R |
| [tidyCpp](https://github.com/eddelbuettel/tidycpp) | Tidy C++ wrapping of the C API of R |
| [rextendr](https://github.com/extendr/rextendr) | Interface to Rust |
| [JuliaCall](https://github.com/Non-Contradiction/JuliaCall) | Seamless integration between R and Julia |
| [JuliaConnectoR](https://github.com/stefan-m-lenz/JuliaConnectoR) | Functionally oriented interface for Julia |
| [XRJulia](https://github.com/johnmchambers/XRJulia) | Structured interface to Julia |

### Tidyverse-like Data Manipulation built on data.table

| Package | Description |
|---------|-------------|
| [tidytable](https://github.com/markfairbanks/tidytable) | Tidy interface to data.table (*rlang* compatible) |
| [dtplyr](https://github.com/tidyverse/dtplyr) | data.table backend for dplyr |
| [tidyfst](https://github.com/hope-data-science/tidyfst) | Tidy verbs for fast data manipulation |
| [tidyft](https://github.com/hope-data-science/tidyft) | Tidy verbs for fast data operations by reference |
| [tidyfast](https://github.com/TysonStanley/tidyfast) | Fast tidying of data |
| [maditr](https://github.com/gdemin/maditr) | Pipe-friendly data.table wrapper |
| [table.express](https://github.com/asardaes/table.express) | Build data.table expressions with dplyr verbs |

### Tidyverse-like Data Manipulation built on collapse

| Package | Description |
|---------|-------------|
| [fastplyr](https://github.com/NicChr/fastplyr) | Fast dplyr-style verbs powered by collapse |
| [timeplyr](https://github.com/NicChr/timeplyr) | Fast time-based data manipulation and aggregation |

## Why Use R-universe?

- **Latest development versions** built daily from GitHub
- **Pre-compiled binaries** for Windows, macOS (Intel & ARM), and Linux
- **Faster installation** compared to installing from source
- **No compilation required** on your machine

## More Information

- [R-universe Documentation](https://r-universe.dev/docs)
- [fastverse Package](https://fastverse.github.io/fastverse/)
- [collapse Package](https://sebkrantz.github.io/collapse/)
