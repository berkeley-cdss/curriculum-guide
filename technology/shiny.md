---
title: Shiny
---

[Shiny](https://shiny.posit.co) is a platform that makes it easy to build
interactive web apps. R shiny server in DataHub is used to build interactive
dashboards.

```{figure} ../images/shiny_combined.gif
:width: 500px
:align: center
:name: Shiny Demo

Short demo of Shiny application on DataHub
```

If you are interested to explore Shiny application further then you can play
with [examples from Posit](https://github.com/rstudio/shiny-examples) and some
[from a Stat instructor](https://github.com/gastonstat/shiny-introstats/).

## Using nbgitpuller

- Install the nbgitpuller plugin for [Google Chrome](https://chrome.google.com/webstore/detail/nbgitpuller-link-generato/hpdbdpklpmppnoibabdkkhnfhkkehgnc) or [Mozilla Firefox](https://addons.mozilla.org/en-US/firefox/addon/nbgitpuller-link-generator/).
- Upload the chosen Shiny application to a GitHub repository.
- Paste the URL for the datahub you are using (If you are using Shiny hub then paste https://shiny.datahub.berkeley.edu/) and open it using "Shiny" option in the nbgitpuller plugin.

```{figure} ../images/launchshinyapp.PNG
:width: 500px
:align: center
:name: Shiny via nbgitpuller link

Launch Shiny application via nbgitpuller plugin
```
- Paste the link in a browser to access the shiny application. Here is an example [link](https://datahub.berkeley.edu/hub/user-redirect/git-pull?repo=https%3A%2F%2Fgithub.com%2Frstudio%2Fshiny-examples&branch=main&urlpath=shiny%2Fshiny-examples%2F003-reactivity%2F).

## Manual Application Installation

- Clone the required [GitHub repository](https://github.com/rstudio/shiny-examples) having Shiny examples to your instance of Jupyterhub.
- Launch the Shiny server.

```{figure} ../images/launchshiny.PNG
:width: 500px
:align: center
:name: Shiny

Short Launch Shiny
```

- Point the Shiny server to an example from the cloned repository.
- Explore the rendered example using shiny dashboard.

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
