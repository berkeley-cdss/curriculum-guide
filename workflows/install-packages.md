---
title: Install Software Packages
---

## Pre-installed Packages

Package installation procedures vary across different programming languages. Basic python packages such as numPy, pandas, scikit-learn, matplotlib, etc., are installed across the main DataHub. R hubs supports packages such as shiny, dplyr, tidyR, RSQLlite, etc.

You can query the list of installed python packages in a jupyter notebook:

```python
!pip list
```
You can query R for the list of installed packages as well:

```R
installed.packages()
```
You can check the packages installed in Julia by accessing the [Julia Hub](http://julia.datahub.berkeley.edu/).

## Install Packages

There are two methods for installing packages. If you will be using a package regularly in your course, we recommend using the long-term installation method.

### Temporary Installation

You can run language-specific commands for installing packages on the hubs. This will install the software within the running environment, however the changes will not be permanent. The environment will get reset when users restart their servers.

```{code} python
:caption: Example of Python package installation
!pip install numpy
import numpy
```

```{code} R
:caption: Example of R package installation
install.packages("ggplot2")
library("ggplot2")
```

### Long-term Installation

:::{attention}
This is the recommended method for frequently used packages.
:::

You can [request](https://github.com/berkeley-dsep-infra/datahub/issues/new?assignees=&labels=support&template=datahub-package-addition---change-request.md&title=Request+python+package+X+for+class+Y) that additional packages be installed in any of the environments in the user docker images. When the software is installed this way, it will persist across server restarts. The packages will remain in the user images for at least the length of the academic term. We periodically review the list of installed packages in between semesters.

#### On Reproducibility

Make sure to specify a version for any library you request. If you do not, the deployment process may break at some point during the semester. Omitting a version will not enable the user environment to always have the latest version -- it will only have the latest version that existed on the date that CI process runs. 

If you want to use an unreleased version of a library, specify the corresponding git SHA of that library's repository.
