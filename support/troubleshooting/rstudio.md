---
title: RStudio
---

## Initialization Error

If you are seeing the error "Error occurred during transmission error", follow
this workaround until a fix can be identified and implemented. Workaround
involves renaming or removing ~/.rstudio via the terminal. To do so while
bypassing the typical rstudio session startup:

1. Go to https://{hub_url}/user-redirect/tree)
2. Click New > Terminal
3. In the terminal, run `mv .rstudio .rstudio.$(date +%s)`.
4. Try to launch rstudio as you normally would.

## Timeouts

Check if this is a browser or network issue.

If that doesn't solve the issue, raise a request using this [template](https://github.com/berkeley-dsep-infra/datahub/issues/new?assignees=&labels=bug&template=bug_report.yml)

As a general note, These issues are challenging to reproduce. It will be helpful if you can be as specific as you can with regards to the steps required to reproduce the issue. We generally observe that the back and forth communication required to reproduce the issue for a request **that is not specific** increases the time needed to fix the issue exponentially.
