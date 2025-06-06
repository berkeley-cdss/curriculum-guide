---
title: Shiny
---

[Shiny](https://shiny.posit.co) is a platform that makes it easy to build
interactive web apps. R shiny server in DataHub is used to build interactive
dashboards.

```{figure} ../images/shiny_combined.gif
:align: center
:name: Shiny demo on DataHub

Short demo of Shiny application on DataHub
```

If you are interested to explore Shiny application further then you can play
with [examples from Posit](https://github.com/rstudio/shiny-examples) and some
[from a Stat instructor](https://github.com/gastonstat/shiny-introstats/).


## Distributing and Running Shiny Apps

You can use [nbgitpuller](nbgitpuller.md) to distribute a Shiny application. You need to specify the full path to the shiny app which includes the targetpath parameter. This parameter sets the destination directory for your Shiny app.

The targetpath parameter is important for Shiny applications because jupyter-shiny-proxy (a Jupyter extension that allows users to run R Shiny applications directly from their Jupyter environment) looks for Shiny apps in specific locations in user's environment, such as ~/ShinyApps/. 

```note
Setting the appropriate target path ensures that your Shiny app will be discoverable and properly launched by the proxy service. Without specifying this parameter, your Shiny applications may not be accessible to users after cloning.
```

For example if the application exists in `course-repo/app1`, the `nbgitpuller` custom URL would be `shiny/course-repo/app1`.

```bash
https://datahub.berkeley.edu/hub/user-redirect/git-pull?repo=<repository-url>&branch=<branch-name>&targetpath=<target-directory>
```

Here is an example link that launches Shiny application in R-staging hub,

```bash
https://r.datahub.berkeley.edu/hub/user-redirect/git-pull?repo=https%3A%2F%2Fgithub.com%2Fds-modules%2Fpolisci-3&branch=main&urlpath=shiny%2Fpolisci-3%2FModule_8_Regression%2F&targetPath=ShinyApps/polisci-3
```

Users can also run Shiny from the JupyterLab launcher. This will display a shiny file browser.

```{figure} ../images/shiny-launcher.png
:align: center
:name: Shiny launcher

Shiny launcher button.
```

## Manual Application Installation

- Clone the required [GitHub repository](https://github.com/rstudio/shiny-examples) having Shiny examples to your instance of Jupyterhub.
- Launch the Shiny server.

## Example

```{figure} ../images/shinyDashboard.PNG
:align: center
:name: Shiny Dashboard

Explore Shiny Dashboard
```

You can also view the code that generated the dashboard in the rendered output. 

```{figure} ../images/shinycode.PNG
:align: center
:name: Code for Shiny

Code that generates Shiny dashboard
```
