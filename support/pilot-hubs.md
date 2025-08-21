# DataHub Feature Pilots - Fall 2025

This document outlines key feature pilots currently underway within various DataHubs during the Fall 2025 academic term. These pilots aim to give tools for a) Instructors to manage their conda environment, identify and fix accessibility issues and b) Admins to track the courses using a particular hub.

## 1. Shared-Conda-Environment Pilot
Description: This pilot focuses on implementing the use of Shared-Conda-Environments across multiple hubs. Shared conda environments let instructors and TAs install custom packages and register new Jupyter kernels for their courses, without needing GitHub pull requests or waiting for the new software to be deployed.

### Key Objectives:

- Gather instructor feedback on the ease of access and use of shared environments

- Assess the impact on resource utilization of instructors - memory and storage

- Identify potential challenges that instructors have while managing this environment

### Piloting Hubs:

- https://stat159.datahub.berkeley.edu/

- https://nature.datahub.berkeley.edu/

## 2. bCourses Based Authorization Pilot
Description: Restrict access to per course hubs hubs based on user's affiliation with bCourses. Students/TAs/Teachers who are in the bCourses roster for authorized courses can access certain hubs.

### Key Objectives:

- Evaluate whether this workflow of managing access to hubs via bCourses roster is manageable for instructors

- Identify process improvements for Spring 26

### Piloting Hubs:

- https://stat20.datahub.berkeley.edu/

- https://stat159.datahub.berkeley.edu/

- https://data8.datahub.berkeley.edu/

- https://data100.datahub.berkeley.edu/

- https://data101.datahub.berkeley.edu/

- https://data102.datahub.berkeley.edu/

- https://prob140.datahub.berkeley.edu/


## 3. JupyterLab-a11y-checker Extension Pilot
Description: JupyterLab-a11y-checker is a JupyterLab extension that performs accessibility checks on Jupyter Notebooks in DataHub, aiming to help authors align their notebooks with WCAG 2.0 AA guidelines. Notebook authors can identify accessibility issues in their notebooks and provide actionable suggestions to fix them.

### Key Objectives:

- Assess the effectiveness of the Jupyterlab-a11y-checker extension in identifying accessibility issues

- Gather user feedback on the usefulness of the suggestions to fix accessibility issues

- Inform future strategies for integrating the tool into the notebook author's workflow


### Piloting Hubs:

- https://a11y.datahub.berkeley.edu/
