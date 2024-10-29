---
title: Otter Grader
---

## Downgrading

Otter Grader is periodically upgraded. If it was running smoothly previously, then it is possible the new version is incompatible with your test cases. You can revert to an older version temporarily with `pip`:

```python
!pip install otter-grader==x.y.z
```

Where `x.y.z` is the desired version.

In the long term, you should plan to rewrite your existing test cases to suit new formats and then run the latest version of otter grader in your notebooks. If you need further support with rewriting test cases then please [reach out to the otter team](https://github.com/ucbds-infra/otter-grader/issues/new?assignees=&labels=question&template=information-request.md&title=).

## Zip File Generation

If you got this error after running this command mentioned below, this is most likely an issue that the Otter team can debug. You can either access their [slack channel](https://join.slack.com/t/otter-grader/shared_invite/zt-bzfqbl82-C1s~YUBkbzvTcPCK60OOgg) or raise a [github issue](https://github.com/ucbds-infra/otter-grader) to seek their inputs directly.

```python
grader.export(pdf=False, force_save=True)
```
