---
title: Jupyter Notebooks and JupyterHub
---

## Jupyter Notebooks

[Jupyter](https://jupyter.org) notebooks are a tool used for in-browser computing that allow code, text, and visualizations to be included on the same page. Students are able to [analyze, document, and visualize their code](https://cdss.berkeley.edu/news/course-future-and-technology-behind-it), all in a single computational document.

Notebooks can support most programming languages. DataHub primarily supports Python, R and, Julia. However, we also support other languages on a case-to-case basis. If you have a unique requirement for using a different programming language as part of your hub, [contact DataHub staff](/support/contact-us).

## JupyterHub

If you have worked with Jupyter notebooks before, you probably used a local installation. Jupyter notebooks can be created, run, and stored on your personal computer. In order to do all this, you have to install several different programs and the installation process can be very tedious and error-prone. Even after you have finished installing everything, you may still see errors in the future for various reasons. (versions of software become outdated, you install conflicting software, etc.)

To avoid the frustrations of setting up and maintaining the programming environment needed for Jupyter notebooks, we have deployed a JupyterHub -- up a multi-user web service that enables users to launch Jupyter notebooks in the cloud. We have named the service [DataHub](https://cdss.berkeley.edu/datahub). Instructors and students can work on and store assignments entirely through JupyterHub. No local installation of Python, Jupyter, etc. is needed. One only needs a browser to get started, which means data science students can start working in notebooks from day one.

### Why does JupyterHub exist?

Working on JupyterHub provides a number of benefits, especially in an introductory course:

* Students never have to do any setup or installation. JupyterHub removes the burden of setting up and maintaining a development environment.
* All students and instructors use the same computing environment.
* Work stored in the cloud and can be accessed from any computer. 
* All students have access to the same compute power, regardless of the machine they are using. For example, students without personal computers can use library computers without being at a disadvantage in the course. 

### Differences from local installation

| JupyterHub | Local Setup |
| :--- | :--- |
| Needs an internet connection | Does not need an internet connection |
| Limited resources (disk and RAM) | Unlimited resources (limited only by your computer) |
| System-wide installation done by admins | You can install anything you want |
| You can only access files in your account | You can maybe access all files (if you are an admin) |
| If things break, we fix them :) | If things break, you have to fix them |

## Getting Access

Anyone with Berkeley credentials has access to the JupyterHub at [datahub.berkeley.edu](https://datahub.berkeley.edu). If you are having difficulties with logging in, please make sure that you are using the correct JupyterHub URL and a berkeley.edu email to login.
