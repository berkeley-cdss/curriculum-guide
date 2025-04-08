---
title: Otter Grader
---

Otter Grader is an open-source, lightweight autograding tool designed to streamline the grading process for programming assignments, labs, and exams. It integrates seamlessly with Jupyter Notebooks and other coding environments, enabling instructors to efficiently test student submissions against predefined criteria. Otter Grader supports various grading workflows, including automated grading with containerized environments (Docker), manual grading interfaces, and generating detailed reports for students.


# Key Features
- Supports grading in Python and R programming languages.
- Grades assignments both locally and in containerized environments.
- Compatible with bcourses and gradescope.
- Instructors provide compute; Otter takes care of generating assignments and tests, managing grading environments and grading submissions.

# Tips for troubleshooting otter

## Downgrading

Otter Grader is periodically upgraded. If it was running smoothly previously, then it is possible the new version is incompatible with your test cases. You can revert to an older version temporarily with `pip`:

```python
!pip install otter-grader==x.y.z
```

Where `x.y.z` is the desired version.

In the long term, you should plan to rewrite your existing test cases to suit new formats and then run the latest version of otter grader in your notebooks. If you need further support with rewriting test cases then please reach out to the otter team.

## Zip File Generation

If you got this error after running this command mentioned below, this is most likely an issue that the Otter team can debug. You can either access their [slack channel](https://join.slack.com/t/otter-grader/shared_invite/zt-bzfqbl82-C1s~YUBkbzvTcPCK60OOgg) or raise a [github issue](https://github.com/ucbds-infra/otter-grader) to seek their inputs directly.

```python
grader.export(pdf=False, force_save=True)
```

## Help Resources

*Documentation:* Visit Otter Grader [Documentation](https://otter-grader.readthedocs.io/en/latest/) for detailed setup guides, API references, and examples.
*Issue Reporting:* For bugs or feature requests, submit a ticket on the [GitHub Issues Page](https://github.com/ucbds-infra/otter-grader/issues).
*Community Support:* Join discussions and get help on the [Community Forum](https://github.com/ucbds-infra/otter-grader/discussions).
