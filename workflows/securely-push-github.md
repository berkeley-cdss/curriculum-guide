---
title: Secure Git Workflows
---

DataHub users can securely push changes to specific GitHub repositories (include private repositories) without saving personal access tokens or SSH keys in their DataHub accounts. This is facilitated by the use of a GitHub App prepared by DataHub staff and installed by privileged users into their repositories with select privileges.

Note that everyone on the hub will have the same level of access to your repo that you designate.

## Berkeley DataHub Git Access

1. The [Berkeley DataHub Git Access](https://github.com/apps/berkeley-datahub-git-access) application must be installed into the desired repositories. Visit the app and click the green "install" button.
1. Select the organization or user containing the private repository. If you are not the owner or administrator of this organization, you might need extra permissions to do this action.
1. Select ‘Only select repositories’, and below that select the private repositories you want to distribute to this JupyterHub.
1. Click the ‘Install’ button. You can revoke this anytime by coming back to this page, and removing the repo from the list of allowed repos. You can also totally uninstall the GitHub app.

## Using the Tool

Run `gh-scoped-creds` and follow the instructions to authenticate and obtain a temporary token.

From the terminal:
```bash
gh-scoped-creds
```

From a Jupyter Notebook:
```python
import gh_scoped_creds
%ghscopedcreds
```
## Security Notes
- Authentication lasts for 8 hours or until a user server is stopped.
- Regularly update permissions to ensure security.

## Troubleshooting
- Check the GitHub App settings for correct permissions.

For more details, visit the [gh-scoped-creds repository](https://github.com/jupyterhub/gh-scoped-creds).
