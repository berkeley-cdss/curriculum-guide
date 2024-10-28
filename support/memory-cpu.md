---
title: Memory and CPU Requirements
---

## Observing Memory Consumption

DataHub has a default per-user memory limit of 1 GB, which should meet the teaching needs of most of our users. Both Jupyter Lab and RStudio can reveal how much memory is being consumed.

Jupyter Lab displays the memory consumption at the bottom of the window.

```{figure} ../images/jupyterlab-memory.png
:align: center
:name: Available memory in Jupyter Lab

```

RStudio displays the memory consumption in the `Environment` tab.

```{figure} ../images/rstudio-memory.png
:align: center
:name: Available memory in RStudio

```

Additionally, if you click the value and choose `Memory Usage Report`, RStudio will display more information about the consumption.

```{figure} ../images/rstudio-memory-report.png
:align: center
:name: RStudio memory usage report

```

## Debugging Memory Consumption

If your consumed memory is greater than the available memory for your server, your kernel or application will crash. You will need to optimize your workflow to consume less RAM.

There are guides for [Python](https://docs.python.org/3/library/debug.html) and [R](https://support.rstudio.com/hc/en-us/articles/218221837-Profiling-R-code-with-the-RStudio-IDE) to help with memory profiling.

## Increase Limits

We recommend instructors to adapt the materials to the 1GB requirement of the DataHub as it is convenient for most usecases. However, If you have a compelling reason to request for more RAM/CPU, use this [template](https://github.com/berkeley-dsep-infra/datahub/issues/new?assignees=&labels=support&template=higher-resources.md&title=Request+more+RAM+for+class+X). Provide rationale for this upgrade as it has cost implications for the service.

There are three factors we consider as part of the requests related to increasing RAM:

- Number of students
- RAM requested
- Amount of time the resource increase is requested for.

You can request resources for all students in the class, or for a subset of students that have been placed into a [bCourses group](https://community.canvaslms.com/t5/Instructor-Guide/How-do-I-manually-create-groups-in-a-group-set/ta-p/700). The latter might be useful for when you need to temporarily increases resources for a particular assignment.

```{list-table}
:header-rows: 1

* - Duration
  - Auto-approval (student count * RAM) threshold
* - < 1 week
  - 600 GB
* - < 1 month
  - 400 GB
* - More than 1 month
  - 200 GB
```
 Any request for more resources than the highlighted ones in the above table requires further consideration at our end.

CPU grant requests are more complex as they they are more likely to affect performance of other users on the hub. As a result, every request would require further consideration at our end.


## Large Data Sets

Given than GitHub has a file upload limit of 100 MB, we recommend that you keep the dataset size below 100 MB. You could either create a subset of the dataset or find another dataset that fits the size limits for overcoming this constraint.

 ```{tip}
Most of the issues with the dataset arise due to the programming practices used while operating the dataset, such as a lot of machine time spent reading/writing to the disk or single-threaded executions that can max the allocated CPU.
```

If resizing the dataset is not feasible, Profile your system to understand the CPU/Memory consumption while operating on the dataset. Use this data to take modify your programming practices so that you are within the allocated CPU/RAM size.
