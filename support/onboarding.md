---
title: Onboard Yourself
---

If you are an instructor planning to teach using DataHub, review this paterial prior to the start of the semester.


## Be Proactive

Please submit support requests for software changes and resource allocations before instruction begins. This helps us to ensure that your requests can be accommodated and will not disrupt other course environments. Ideal time frames to make requests are either **before the start or during the first two weeks of the semester**. We recommend this timeline to ensure that we make minimal changes to the hub infrastructure when the courses are ongoing.

### Assignment Deadlines

Please try to schedule assignments during regular working hours so that infrastructure staff can troubleshoot hubs if something goes wrong.

### Test Assignments in Advance

Please try to test assignments and notebooks on the hub before giving them to students. This will allow time for the infra team to fix any issues you discover.

## Export to PDF Using WebPDF

We recommend using the “Save and Export Notebook as -> WebPDF” option to convert Jupyter notebooks to PDF. We have resolved the image rendering issues previously encountered with this method and are hoping for a smoother conversion process. For more details on PDF conversion, please refer to the [documentation](download_notebook_as_pdf).

## Using Language Models in Assignments

If you plan to incorporate language models into your assignments then please schedule a consultation with the infra team before releasing the assignments to students. For more details, please refer to the [documentation](using-ai-llm).

## Backup Students' Data

We recommend that you inform students to back up their data (notebooks and datasets) on their local devices before the end of the semester. We have prepared [download instructions](download-archive) on how students can retrieve all of their archived files.  We receive a lot of student requests to retrieve their files after the completion of the semester. Any upfront communication from your end about backing up their files will hopefully ease the workload for us.

## FAQ

### How can I learn more about DataHub to onboard myself?

- If you are interested in learning more about the configuration of various Berkeley hubs, you can checkout [UC Berkeley's JupyterHubs documentation](https://docs.datahub.berkeley.edu).

- If you want to set up a hub infrastructure at your end and are interested in learning more about the technical details, use this [Zero to JupyterHub with Kubernetes documentation](https://zero-to-jupyterhub.readthedocs.io/en/latest/).

We have [over a dozen hubs](https://docs.datahub.berkeley.edu/hubs.html) which cater to the diverse needs of the campus audience. We have the [main hub](https://datahub.berkeley.edu/), which serves multiple departments/courses across the campus. We also have separate hubs for courses such as Data 8, Data 100, Public health, etc., serving the instructional needs.

### Default memory and CPU requirements

[DataHub](https://datahub.berkeley.edu/) has a per-user memory limit of 1 GB, which should meet the teaching needs of most of our users. If you are interested to know more about the memory consumption in your instance, please follow the steps below:

- Look at the top right corner of your Python/R notebook for the term memory. It will highlight the amount of memory you had consumed against the total memory available for your server.
- If your consumed memory is greater than the available memory for your instance then your server will crash resulting in you either optimizing your workflow to be less compute intensive or requesting additional RAM,

```{figure} ../images/memory.png
:align: center
:name: Available Memory

```

Please contact us if your course/research has more complex computation requiring increased capacity.

### As an instructor what do I need to do to set up the hub for my course?

Honestly, nothing! You are free to use the DataHub starting today.

### How do my students download their submissions as a PDF?
We recommend that you use the following options,
 
- **For Jupyter Notebooks:** Select File -> Download as -> WebPDF to download the PDF version of your notebook.
```{figure} ../images/downloadhtml.PNG
:align: center
:name: Downloading notebook as a PDF 
Here is where you can find the option to download the Python notebook as a PDF!
```
- **For R files:** Select File -> Knit Document -> Select the target folder -> Select the Output Format as PDF to save the PDF version of the file
 ```{figure} ../images/knitting.PNG
:align: center
:name: Downloading R notebook as a PDF
Here is where you can find the option to download the R file!
```
```{figure} ../images/knittingpdf.PNG
:align: center
:name: Knitting a PDF
Here is where you can find the option to specify the download format as PDF!
```
