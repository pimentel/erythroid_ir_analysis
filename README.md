# Erythroid Intron Retention Analysis

This repository contains the post-processing results necessary to reproduce the
figures and analysis that was performed in the paper

- "An Erythroid Intron Retention Program Regulates Gene Expression During
  Terminal Erythropoiesis" by Harold Pimentel, Marilyn Parra, Sherry Gee, Narla
  Mohandas, Lior Pachter, John Conboy.

## Organization

Most people will likely be interested in the `knitr` result file, which is
essentially a report. This file can be found at `R/analysis.html`

- The main code can be found in `R/`
    - It depends on several packages, all of which can be found on CRAN, with
      the exception of [kma](http://github.com/pachterlab/kma)
- To run the code, you also need the expression estimates to be stored in
  a `data` directory
    - The `data` directory can be download from
      [here](http://math.mcb.berkeley.edu/~pimentel/erythroid_ir_analysis/data.tar.gz)
      - The directory should exist under `data` so that the R code knows how to
        find it

### Example

Here is an example of how you might run this analysis.

First, clone the reposistory:

```{bash}
git clone git@github.com:pimentel/erythroid_ir_analysis.git
cd erythroid_ir_analysis
```

Now download the `data` directory and extract it into the same folder

```{bash}
wget http://math.mcb.berkeley.edu/~pimentel/erythroid_ir_analysis/data.tar.gz
tar -xf data.tar.gz
```

Fire up `R` and open `R/analysis.Rmd` with your favorite editor
