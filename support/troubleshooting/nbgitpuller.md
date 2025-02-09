---
title: nbgitpuller
---

You may run into different types of errors when you are using the JupyterHub or Jupyter notebooks. The majority of errors come from a few common causes and can be solved using the following methods.

## Link Errors

nbgitpuller link errors are usually due to one of three issues.

### Incompatible Browser

Unfortunately, the nbgitpuller software does not support the Microsoft Edge browser. If you click an nbgitpuller link in Edge, you will likely be taken to your datahub.berkeley.edu dashboard, but you won't see your desired files there. 

Open nbgitpuller links in Chrome, Firefox, or Safari.

### Link Generated Incorrectly

If the nbgitpuller link was not generated correctly, you'll see a red loading bar with an error message that says "Error: Command '['git', 'fetch']' returned non-zero exit status 128." An example screenshot is below:

```{image} ../../assets/broken-nbgitpuller-link.png
:alt: Example error output from nbgitpuller

```

Solution: re-generate the nbgitpuller link. Make sure that you've filled in the correct Jupyter hub URL, Github URL, branch, and file. Some tips:
* URLS should NOT end with forward slashes. "https://github.com/ds-modules" is okay; "https://github.com/ds-modules/" will break
* The Git repository url should go to the base repo that contains the materials you want. For example, if you want to link to the "lab01.ipynb" in the fall19 repository of the data-8 organization, the Git URL should be "https://github.com/data-8/fall19", not "https://github.com/data-8/fall19/blob/master/lab01"
* The File to Open needs to include the full path of the file from the base repository. For example, if the "lab01" file is in a folder called "labs", the File to Open needs to be "labs/lab01"

### Modified Content

If you make changes to an assignment on GitHub after students have started working on it, students that click the nbgitpuller link again may see a red loading bar and a message about a *merge conflict*. This occurs if the instructor and the student both change the same parts of the notebook: nbgitpuller doesn't know how to integrate the instructor's changes without overwriting student work, so it refuses to proceed. You can read [more about nbgitpuller's automatic merging behavior](https://jupyterhub.github.io/nbgitpuller/topic/automatic-merging.html).

### Solutions

#### Rename Files

The easiest and most conservative solution is to rename the file or folder that contains the incompatible changes, then click the nbgitpuller link again. If the file or folder is renamed to anything else (e.g. "SOC-5-old"), nbgitpuller will clone a fresh copy of the problematic files to the student's Jupyterhub. They can then copy over any work from the old version of the file.

When you face an error like below, do the following steps
```{figure} ../../images/mergeconflict.png
:align: center
:name: DataHub Admin

Here is how the admin dashboard looks like!
```

- Rename the existing folder where the merge conflict error arose
```{figure} ../../images/tshoot.PNG
:align: center
:name: Folder Rename!

Here is the steps required to rename the folder!
```
- Click on the nbgitpuller link again
- Use the newly cloned repository created after nbgitpuller link was clicked

#### git stash

If you have command line experience then you can use "git stash" command in terminal to temporarily remove the incompatible changes.
 
- If you are using https://datahub.berkeley.edu then navigate to your file manager which acts as your home page. If you are using other hubs then you can access your file manager by navigating to "Hub URL/user/`Your-Username`/tree" which will take you to the home directory. For eg: If my user name is Julia and I want to access my home directory in R hub then the URL to access my home directory will be https://r.datahub.berkeley.edu/user/julia/tree.
- On the upper right of the page, click the dropdown menu that says “New” and select “Terminal”.

```{figure} ../../assets/terminal.png
:align: center
:name: Launch Terminal

Launch a terminal
```

- Navigate to the folder where a) your files are stored and b) you have merge conflict issues
- Run `git stash` command in the terminal and you will see the following output

```{figure} ../../assets/gitstash_output.png
:align: center
:name: git stash output

Output from git stash command
```
- Access the nbgitpuller link again. You will be able to load the notebooks directly.

The best advice, however, is to avoid making changes to assignments once they've been released to students if at all possible.
