# DataHub Feature Pilots

This document outlines feature pilots within various DataHubs. These pilots aim to provide tools for instructors to manage their conda environment, identify and fix accessibility issues and for admins to track the courses using a particular hub.

## Current Pilots - Spring 2026

### 1. JupyterLab-a11y-checker Extension Pilot

**Status:** Ongoing

**Description:** JupyterLab-a11y-checker is a JupyterLab extension that performs accessibility checks on Jupyter Notebooks in DataHub, aiming to help authors align their notebooks with WCAG 2.0 AA guidelines. Notebook authors can identify accessibility issues in their notebooks and receive actionable suggestions to fix them.

#### Key Objectives:

- Assess the effectiveness of the JupyterLab-a11y-checker extension in identifying accessibility issues

- Gather user feedback on the usefulness of the suggestions to fix accessibility issues

- Inform future strategies for integrating the tool into the notebook author's workflow

#### Piloting Hubs:

- https://a11y.datahub.berkeley.edu/

---

## Completed Pilots - Fall 2025

### 1. Shared-Conda-Environment

**Status:** Completed

**Description:** This pilot focused on implementing `Shared-Conda-Environments` across multiple hubs. Shared conda environments let instructors and TAs install custom packages and register new Jupyter kernels for their courses, without needing GitHub pull requests or waiting for the admins to deploy the new software.

#### Key Outcomes:

- Gathered instructor feedback on the ease of access and use of shared environments

#### Piloted Hubs:

 https://astro.datahub.berkeley.edu/

- https://stat159.datahub.berkeley.edu/

- https://nature.datahub.berkeley.edu/

#### Documentation:

For more information on using shared conda environments, see the [Shared Conda Environment workflow guide](/workflows/shared-conda-environment).

---

### 2. bCourses Based Authorization

**Status:** Completed

**Description:** This pilot restricted access to per-course hubs based on user's affiliation with bCourses. Students/TAs/Teachers who are in the bCourses roster for authorized courses can access certain hubs.

#### Key Outcomes:

- Evaluated whether this workflow of managing access to hubs via bCourses roster is manageable for instructors

- Making this workflow to be a standard practice for the piloted hubs from Spring 2026

#### Piloted Hubs:

- https://stat20.datahub.berkeley.edu/

- https://stat159.datahub.berkeley.edu/

- https://data8.datahub.berkeley.edu/

- https://data100.datahub.berkeley.edu/

- https://data101.datahub.berkeley.edu/

- https://data102.datahub.berkeley.edu/

- https://prob140.datahub.berkeley.edu/
