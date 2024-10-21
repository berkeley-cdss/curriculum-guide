---
title: RStudio
---

[RStudio](https://posit.co/products/open-source/rstudio) is an integrated development environment that is popular among R users.

```{figure} ../images/rstudio.png
:width: 500px
:align: center
:name: RStudio

Example of running RStudio on DataHub
```

RStudio is available on many of our R-based hubs, and is the default application on [R hub](https://r.datahub.berkeley.edu).


## RStudio Applications

RStudio has integration with applications such as [Quarto](quarto) and [Shiny](shiny). These applications should work as they do on desktop machines. Windows and tabs will be launched as expected.

## Using nbgitpuller

One can use nbgitpuller to pull in code and data, however unlike JupyterLab, RStudio cannot be configured to open a specific document at server launch. One must manually navigate to the pulled file.
