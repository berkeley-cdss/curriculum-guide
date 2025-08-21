# Pulling from Private GitHub Repositories

This guide explains how to use nbgitpuller to pull notebooks and files from private GitHub repositories on DataHub. This feature is useful when you need to distribute private course materials and proprietary datasets to students.

## Overview

DataHub supports pulling rom private GitHub repositories through GitHub Apps with specific configurations. This allows instructors to:

- Distribute course materials from private repositories securely
- Share proprietary datasets with enrolled students
- Create nbgitpuller links for private repositories

## Available GitHub Apps

DataHub has several GitHub Apps configured for private repository access. These apps have titles containing "private repos" and can be found in the [berkeley-dsep-infra organization settings](https://github.com/organizations/berkeley-dsep-infra/settings/apps).

Each DataHub instance may have its own dedicated GitHub App for private repository access:

## Prerequisites

Before you can pull notebooks from a private repository, ensure that:

1. **Hub Support**: Your DataHub instance supports private repository pulling (contact DataHub administrators to confirm)
2. **GitHub App Permission**: A DataHub administrator has granted the appropriate GitHub App access to your repository

## Getting Permission for Private Repository Access

:::{important}
A DataHub administrator must grant permission for the GitHub App to access your private repository before you can create nbgitpuller links.
:::

To request access:

1. **Contact DataHub Support**: Reach out to the Berkeley DataHub team through your usual [support channels](https://github.com/berkeley-dsep-infra/datahub/issues)
2. **Provide Repository Details**: Include the following information:
   - Full repository URL (e.g., `https://github.com/your-org/private-repo`)
   - DataHub instance you'll be using (main DataHub, dev, or specific course hub)
   - Course information and justification for private access
3. **Wait for Configuration**: The administrator will configure the GitHub App to access your repository

### Administrator Process

For DataHub administrators, the process involves:

1. Identifying the correct GitHub App for the target DataHub instance
2. Installing the app in the organization containing the private repository
3. Granting the app access specifically to the requested repository
4. Verifying the configuration works with a test pull

## Troubleshooting

### Common Issues

**Link doesn't work / Access denied**
- Verify the GitHub App has been granted access to your repository
- Check that you're using the correct DataHub URL for your instance
- Ensure the repository URL is correct and accessible

**Repository not found**
- Confirm the repository is private and exists
- Verify you have the correct repository URL
- Check that the GitHub App is installed in the correct organization

## Security Considerations

When working with private repositories:

### Access Control
- **Limited Scope**: GitHub Apps only have access to repositories explicitly granted
- **Read-Only**: Apps typically have read-only access to repository contents
- **User Authentication**: Students must be logged into DataHub to access private content

### Best Practices
- **Minimize Exposure**: Only grant access to repositories that absolutely need it
- **Regular Audits**: Periodically review which repositories have been granted access
- **Remove Access**: Request removal of access when courses end or materials are no longer needed
- **Sensitive Data**: Avoid storing highly sensitive data even in private repositories

## Example Workflow

Here's a typical workflow for using private repositories:

1. **Prepare Repository**: Create or organize your private GitHub repository with course materials
2. **Request Access**: Contact DataHub administrators to grant GitHub App access
3. **Wait for Confirmation**: Administrator confirms the configuration is complete
4. **Create Links**: Generate nbgitpuller links using your preferred method
5. **Test Access**: Verify the links work by testing them yourself
6. **Distribute**: Share the links with students through your LMS or course website
7. **Monitor Usage**: Check for any access issues reported by students

## Related Documentation

- [Creating nbgitpuller Links](nbgitpuller-link.md) - General nbgitpuller usage
- [Distributing Files](distributing-files.md) - Alternative methods for file distribution