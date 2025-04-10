# Options to Launch Jupyter R Kernel (or run R notebooks)

## Option #1: Launch Jupyter R Kernel locally

Step 1: Install Anaconda locally. Check this [link](https://docs.anaconda.com/anaconda/install/index.html) for installation.

Step 2: Open Anaconda prompt shell. Run the following code to install R Kernel in Jupyter Lab

```{code}
conda install -c r r-essentials
```

```{note}
Press "y" when commandline prompts to install all the packages
```


Step 3: Run the following command to install tidyverse.

```{code}
conda install -c r r-tidyverse
```

```{note}
Press "y" when commandline prompts to install all the packages
```


Step 4: Run the following command to launch Jupyter Lab

```{code}
jupyter lab
```

Step 5: Now, from the launcher tab, choose R kernel to start a new notebook.

```{figure} ../images/launcher_tab_r_kernel.jpg
:align: center
:name: Jupyter Notebook Launcher Tab with R Kernel
```

The following is a screenshot of Jupyter notebook having R kernel.

```{figure} ../images/jupyter_notebook_r_kernel.jpg
:align: center
:name: Jupyter Notebook with R Kernel
```

## Option #2: Use Google Colab to launch R Kernel

Step 1: Launch R Kernel in Google Colab by accessing this link - https://colab.to/r

Step 2: Check whether the tidyverse packages (or any other package you need) are already installed in Colab by using the following code,

```{code}
print(installed.packages())
```

Step 3: If not installed, Install tidyverse package using the following command

```{code}
devtools::install_github("tidyverse/tidyverse")
```
