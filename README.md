# tidybayes: R Package for composing data for and extracting samples from Bayesian samplers in a tidy data format 

_Matthew Kay, University of Washington <mjskay@uw.edu>_

`tidybayes` aims to simplify two common (often tedious) operations in R when using Bayesian modelling languages like JAGS or Stan:

* __Composing data__ for use with the sampler. This often means translating data from a `data.frame` into a `list`, making sure `factors` are encoded as numerical data, adding variables to store the length of indices, etc. `tidybayes` helps automate these operations using the `compose_data` function, automatically handles data types like `numeric`, `logical`, `factor`, and `ordinal`, and allows easy extensions for converting other datatypes into a format the sampler understands by providing your own implementation of the generic `as.data_list`. 

* __Extracting samples__ from the sampler, which often means translating columns of samples indexed by names like `b[1,1]`, `b[1,2]`, etc. into a more usable format. We provide a straightforward way to convert samples of a variable with indices into long-format ("tidy") data, which automatic back-conversion of factors, using the `extract_samples` function. In most cases this kind of long-format data is much easier to use with other data-manipulation and plotting packages (e.g., `dplyr`, `tidyr`, `ggplot2`) than the format provided by default from the sampler.

## Installation

You can install the latest development version from GitHub with these R commands: 

```R
> install.packages("devtools")
> devtools::install_github("mjskay/tidybayes")
```

## Examples

TBD.

## Problems

Should you encounter any issues with this package, contact Matthew Kay (<mjskay@uw.edu>). If you have found a bug, please file it [here](https://github.com/mjskay/tidybayes/issues/new) with minimal code to reproduce the issue.