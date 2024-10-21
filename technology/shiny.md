---
title: Shiny
---

[Shiny](https://shiny.posit.co) is a platform that makes it easy to build
interactive web apps. R shiny server in DataHub is used to build interactive
dashboards.

```{figure} ../images/shiny_combined.gif
:width: 500px
:align: center
:name: Shiny demo on DataHub

Short demo of Shiny application on DataHub
```

If you are interested to explore Shiny application further then you can play
with [examples from Posit](https://github.com/rstudio/shiny-examples) and some
[from a Stat instructor](https://github.com/gastonstat/shiny-introstats/).


## Distributing and Running Shiny Apps

You can use [nbgitpuller](nbgitpuller.md) to distribute a shiny application. Specify a URL of `/shiny`. You can also specify the full path to the shiny app. For example if the application exists in `course-repo/app1`, the `nbgitpuller` custom URL would be `shiny/course-repo/app1`.

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
:width: 500px
:align: center
:name: Shiny Dashboard

Explore Shiny Dashboard
```

You can also view the code that generated the dashboard in the rendered output. 

```{figure} ../images/shinycode.PNG
:width: 500px
:align: center
:name: Code for Shiny

Code that generates Shiny dashboard
```
