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

```{figure} ../../images/jupyter_notebook_r_kernel.jpg
:width: 500px
:align: center
:name: Jupyter Notebook with R Kernel
```

## Google Colab

Step 1: Launch R Kernel in Google Colab by accessing this [link](https://colab.to/r)

Step 2: Check whether the tidyverse packages (or any other package you need) is already installed in Colab by using the following code,

```R
print(installed.packages())
```

Step 3: If not installed, Install tidyverse package using the following command

```R
devtools::install_github("tidyverse/tidyverse")
```

## Binder

[Binder](https://mybinder.org) enables users to launch Python and R notebooks in a free and open executable environment. Launch [Jupyter R notebook](https://notebooks.gesis.org/binder/jupyter/user/binder-examples-r-conda-ofu958y9/lab) or [R Studio](https://mybinder.org/v2/gh/binder-examples/r-conda/master?urlpath=rstudio) using the shared binder links.

## RStudio

If you are a RStudio fan, you can access [RStudio Cloud](https://rstudio.cloud/plans/instructor) where you can purchase a hosted environment for your coursework.

```{note}
Students need to create R Studio accounts.
```

If you don't want to purchase an RStudio cloud account, you can ask students to download and install a free [RStudio Desktop application](https://www.rstudio.com/products/rstudio/) on their desktop or use the [free tier account](https://rstudio.cloud/plans/free).

```{note}

Workflow while using free RStudio cloud account would look like below,

- Students need to download their homework from the github repository/canvas/google drive. 
- They should upload the homework to their RStudio server account. 
- Post completion, They should download the completed homework from RStudio server account.
```
