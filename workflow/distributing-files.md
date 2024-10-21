---
title: Distributing Files
---

We recommend using [nbgitpuller](https://nbgitpuller.readthedocs.io) to
distribute files to students.

If you do not wish to use this mechanism, you can distribute assignments
through bCourses. In this case, after you have uploaded the files to bCourses,
students will need to download them and then upload them to their own
DataHub accounts.

## Workflow

Here are the basic steps you will need to go through to distribute notebooks
and other files. Please read through the rest of this page to learn more about
the details of the process.

1. Create a folder on your own device containing all files for the assignment, e.g. notebook, datasets, etc.
1. [Upload the folder](pushing-to-github.md) to a public GitHub repository
1. Generate an nbgitpuller link for the folder using the nbgitpuller link generator. (more on this below)
1. Distribute the link to students through email, bcourses, etc.

## nbgitpuller Links

nbgitpuller links simplify the assignment distribution process. Rather than
downloading files from an external source and then uploading to their personal
DataHub accounts, users can obtain all files for a given assignment with
just one click. When a user clicks on an nbgitpuller link for a particular
assignment, all files for the assignment will show up in the user's personal
DataHub account.

These links can be used with any content stored on GitHub in a public
repository. nbgitpuller links can be generated for an entire repository, or a
particular file or folder. When a link is clicked, a series of git commands are
run from the user's DataHub account, which is why nbgitpuller links must be
used with content on GitHub. They cannot be used to pull arbitrary files from
sources other than GitHub.

Using these links enables users to immediately nbgitpuller with publicly
available content on GitHub. This is valuable for easy assignment distribution,
but also in the broader context of using the open-source content that is
available on GitHub. Learning Git is no longer a barrier to interacting with
this content.

### How do nbgitpuller links work?

Here is an nbgitpuller link with the various components highlighted in different colors. The grey portions of the link are needed for formatting and will remain the same for each links. The colored portions will be different for each link. If you are new to GitHub you may want to familiarize yourself with the basics (repositories, branches, etc.) to better understand each component.

![link components](link-components.png)

The above link does the following:

* Clones the repo `ds-modules/SW-282` into the user's account on `https://datahub.berkeley.edu`
* Checks out to the `master` branch (this is the default, but specifiable on nbgitpuller)
* Opens the file `lab04/lab04.ipynb` on `datahub.berkeley.edu`. The full path of this file on the user's DataHub account would be `~/SW-282/lab04/lab04.ipynb`.

## Restrictions

To use an nbgitpuller link, files must be stored in a public GitHub repo.
nbgitpuller links will not work with private repositories.

## Link Generator

nbgitpuller links can be manually created in the format shown above, or can be automatically generated using the [link generator](https://jupyterhub.github.io/nbgitpuller/link?hub=https://datahub.berkeley.edu&repo=https://github.com/ds-modules/). The generator tool allows users to specify a JupyterHub URL and GitHub URL as inputs. The tool will generate an nbgitpuller link for the specified GitHub content and JupyterHub.

![nbgitpuller](nbgitpuller.png)

For example, to pull [this repo](https://github.com/ds-modules/SW-282/tree/master/lab04/lab04.ipynb) into DataHub, we would fill out the nbgitpuller link generator with:

1. Fill in the JupyterHub URL field with `https://datahub.berkeley.edu`
2. Paste the GitHub URL **to the repo** in the Git Repository URL field: `https://github.com/ds-modules/SW-282`
3. Leave the Branch field blank, because it defaults to `master`
4. Fill in the File to Open field with the path to the file: `lab04/lab04.ipynb`

After finishing these steps, the link in the grey text box will be your nbgitpuller link. Note that the link to the link generator above will pre-fill the JupyterHub URL and GitHub URL fields, **but it will not paste in the repo**, so you will need to add the name of the repo to the GitHub URL field, as well as fill in the (optional) branch and file path fields.

## Best Practices

nbgitpuller pulls _all files_ from a repository into the user's DataHub account.

:::{danger}
You should not store unfinished materials and answer keys in the same repo as
published assignments. Any nbgitpuller link for a published assignment would
also distribute the unfinished materials and answer keys to the students.
:::


We recommend that you use a public repo for published assignments and a private repo for unfinished materials and answer keys.

## Browser Extensions

We have created web browser extensions to streamline the process of creating shareable links. It is tailored specifically for UC Berkeley instructors, as seen in the Berkeley-specific version of the [nbgitpuller link generator](https://github.com/berkeley-dsep-infra/nbgitpuller-link-generator-webextension).

### Installation

Google Chrome
: Visit the DataHub link generator [Chrome extension's
webpage](https://chromewebstore.google.com/detail/datahub-link-generator/ijbgangngghdanhcnaliiobbiffocahf?hl=en).
Click the "Add to Chrome" button to install the extension.

Mozilla Firefox
: Download and install [the
extension](https://addons.mozilla.org/en-US/firefox/addon/nbgitpuller-link-generator)
from within Mozilla Firefox.


### Access

After installation, look for the extension in your browser toolbar. In Chrome, there is puzzle piece icon in the upper-right corner of your Chrome tab.

```{figure} ../images/link-generator.png
:width: 500px
:align: center
:name: puzzle piece

Click puzzle piece icon
``` 

Click on the pin button to make sure the extension stays pinned at the top of the screen.

```{figure} ../images/pin-extension.png
:width: 500px
:align: center
:name: pin extension

Pin extension
``` 

- The extension appears on the browser like the snapshot below,

```{figure} ../images/installed-extension.png
:width: 500px
:align: center
:name: show installed extension

Show installed extension
``` 

### Creating the Link

1. Access a Github repository containing notebooks in Python/R

1. Open your assignment from a respective Github repo

   ```{figure} ../images/github-notebook.png
   :width: 500px
   :align: center
   :name: github repo
   
   Open a notebook from github repo
   ``` 

1. Select the link generator extensions icon in the top right part of the browser (closer to URL section)

1. Enter parameters for your link.

   JupyterHub URL
   : Paste your DataHub URL, e.g. https://datahub.berkeley.edu, https://r.datahub.berkeley.edu

   Open in
   : Choose the appropriate option, e.g. JupyterLab, Classic Notebook, RStudio, etc.


   ```{figure} ../images/extension.png
   :width: 500px
   :align: center
   :name: extension icon
   
   Icon showing the DataHub-link-generator extension
   ```

1. As a last step, Select "Copy nbgitpuller link" button which generates a shareable link that opens your assignment in the choosen interface or "Open in tab" button which opens the notebook in a new tab. 
