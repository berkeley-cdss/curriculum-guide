---
title: Download Files in Bulk
---

You can easily download all your assignments and projects as an archive file, eliminating the need to download each file individually. The [Jupyter Archive](https://github.com/jupyterlab-contrib/jupyter-archive) package enables users to bundle their files and folders as single archive file which can be downloaded.

You have two options to download all your files in DataHub as an archive:

- Download Current Folder as an Archive
- Download as an Archive

## Download Current Folder as an Archive

You can navigate to the folder you want to download and then select this option to download all the folders/files located within this folder. This option downloads all the contents of the current folder as a single zip file. If you are in the home directory then it downloads all your content as a single archive file.

## Download as an Archive

If you prefer to download specific folders individually, use the "Download as an Archive" option. This allows you to select individual folders, which will then be downloaded as separate ZIP files.

## Instructions for JupyterLab Interface

- Open the File Browser section located on the left side of the JupyterLab interface.
- To use the "Download as an Archive" option, select the folders you wish to download or,
- To use the "Download Current Folder as an Archive" option, navigate to the folder you want to download.
- Right-click and select your preferred download option from the context menu.

```{figure} ../images/download-folder.gif
:align: center
:name: Download archive from lab interface
```

## Instructions for Jupyter Notebook Interface

If you are using the Jupyter Notebook interface, you can easily download all your files using one of the options mentioned above by navigating to the tree view. To access your hub's tree interface, use the following URL format:

```{code}
<HUB_URL>/user/<YOUR_USERNAME>/tree
```
For example, if your username is bawar, you can access the tree interface in Data 100 hub via:

https://data100.datahub.berkeley.edu/user/bawar/tree

Once you're in the tree view, you can select the desired option to download your files efficiently.

```{figure} ../images/download-archive.gif
:align: center
:name: Download archive from tree interface
```