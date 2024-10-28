---
title: Performance Best Practices
---

Large courses or courses with complex software/compute requirements can consume a lot of memory/cpu which can result in poor user experience and increased cloud costs. Some of the commonly reported performance issues are due to one or many  of the following reasons.

## Large Output

Students may print large data frames to a notebook directly or try to show a
table that is too large in a notebook cell. The way to solve this issue is to
recommend students to not print large data directly to a cell in their
notebook. In addition, You can slice the datasets to a smaller samples that
students don't run into issues even if they print the entire dataset (not
ideal). Please always  review your datasets and remove parts of data that are
not core to achieving the required learning outcomes for students

Students are joining tables that are large. Once again, try to break down the dataset to subset that is of interest to achieve the course objectives.

## Infinite Loops

You can ask students to review their  code constantly to check if they are running an infinite loop. You can ask students to reach out to you/your team if they believe that they have issues related to infinite loop in their code. If no one reached out, You can also check with the infra team to identify the problematic user notebooks and do the necessary code review to solve this issue (Re: admin access).

## Multiple Open Notebooks

Students are having multiple notebooks open at the same time across one or many browsers. If students report errors such as 503, 401 error codes etc.. ask them to check if they have notebooks open in multiple tabs. As a best practice, please ask students to have a single active tab with a notebook and close other tabs.

## Software Updates

You might run into trouble if you upgrade to the latest version of a package
without testing it extensively. As a rule of thumb, upgrade packages in staging
environment and test the notebooks extensively. Only when you feel comfortable
with the updated environment, ask the infra team to upgrade to the latest
package version in the stable environment. If you are unsure of the URL for
staging environment for the hub you use for teaching purposes then  ask the
infra team.

## GPUs

We don't offer GPUs on the instructional hubs, and students working on
assignments with large language models can instead max out CPUs. This can
result in indefinite execution of celles with no output. 

## Consult with DataHub Team

Reach out to DataHub staff if you want to use:

 - databases like SQLite as part of your workflow.
 - GUI-based applications like pyqt5 and QGIS.
