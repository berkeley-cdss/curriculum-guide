---
title: External Computing
---

People who cannot access DataHub may still be able to do computing in other locations.

## Personal Computer with Miniforge

[Miniforge](https://conda-forge.org/miniforge) is a distribution of [Anaconda](https://docs.anaconda.com/anaconda/install/index.html) that has easy access to a wide range of open source scientific computing software. Download and run the appropriate `Miniforge3` installer from the link above.

Launch a terminal on your computer and install software.

```bash
# Install Jupyter with Python kernel
mamba install jupyterlab ipython

# Install R and its Jupyter kernel
mamba install r-essentials r-tidyverse r-irkernel
```

Launch Jupyter from a terminal:
```bash
jupyter lab
```

The following is a screenshot of Jupyter running the R kernel.

```{figure} ../images/jupyter_notebook_r_kernel.jpg
:align: center
:name: Jupyter Notebook with R Kernel
```

## Binder

[Binder](https://mybinder.org) enables users to launch Python and R notebooks in a free and open executable environment. Launch [Jupyter R notebook](https://notebooks.gesis.org/binder/jupyter/user/binder-examples-r-conda-ofu958y9/lab) or [R Studio](https://mybinder.org/v2/gh/binder-examples/r-conda/master?urlpath=rstudio) using the shared binder links.

## RStudio Cloud and Desktop

You can purchases a hosted [RStudio Cloud](https://rstudio.cloud/plans/instructor) environment for your coursework. Students would need to create RStudio accounts. They would also need to upload and download assignments to/from their RStudio cloud accounts. The is also a [free tier account](https://rstudio.cloud/plans/free).

If you don't want to use RStudio Cloud, you can ask students to download and install [RStudio Desktop](https://www.rstudio.com/products/rstudio/) onto their own device.

## Google Colab

You can launch Python or R based notebook environments on [Google Colab](https://colab.research.google.com).
