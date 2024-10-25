---
title: VS Code
---

VS Code can be installed on any DataHub deployment. It is useful for when you want a full integrated development environment.

The application can be run from Jupyter Lab's launcher.

```{figure} ../assets/vscode-launcher.png
:align: center
:name: VS Code Jupyter Lab launcher

Click on the VS Code icon to launch it.
```

## Launch VS Code with nbgitpuller

At the [ngbitpuller link generator](https://jupyterhub.github.io/nbgitpuller/link), specify the hub that contains VS Code, and any other relevant information about the git repo.

Ignore the "File To Open" field, since VS Code will not open it directly. It would rather open the directory containing your files. Enter the *Custom URL* as `vscode/?folder=/home/jovyan/path/to/files` for the "Application to Open" field.

VS Code editor is currently configured only for EECS Hub and Data 8x Hub. If you want to enable this option as part of other hubs then please do raise a [github issue](https://github.com/berkeley-dsep-infra/datahub/issues/new?assignees=balajialg&labels=type%3A+enhancement&template=featurerequest.md)

```{figure} ../images/vscode_link_generator.PNG
:align: center
:name: nbgitpuller link to launch VS Code

Generate an nbgitpuller link to launch VS Code in EECS Hub
```

## Install Python and Jupyter Extensions

If you would like to use VS Code to be open and execute your `.ipynb` files, you will need to install extensions from VS Code's extension marketplace. Search for "python" and install the `ms-python` extension. Do the same for "Jupyter" (`ms-toolsai.jupyter`).


```{figure} ../images/python_extension.PNG
:align: center
:name: Install Python extension

Install python extension in the VS Code editor
```
