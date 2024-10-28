---
title: Elevated Privileges
---

## What are elevated privileges?

Elevated privilege enable course staff to troubleshoot students notebook interface in the hub. If you have such privileges, you can:

1. Start and stop students' servers
1. Access students' servers to debug issues

```{warning}
Elevated privileges are hub-wide. If you have a GSI teaching your course using a particular hub but is acting as a student in another course which uses the same hub, then this can result in a conflict of interest. Please report such scenarios to the infrastructure team so that we can take the necessary corrective action.
```

```{figure} ../images/admin.png
:align: center
:name: DataHub Admin dashboard

Admin Dashboard
```

## Obtaining Elevated Privileges

Only course staff should have elevated privileges. If you need such access, you can [create a github issue](https://github.com/berkeley-dsep-infra/datahub/issues/new?assignees=&labels=support&template=admin_request.yml). By default, those who are assigned the `teacher` or `ta` role in bCourses will be given privileges.

```{note}
When making the request, do not submit a list of usernames for the staff who require elevated privileges. Instead, please provide the bcourses ID for the course.
```

To assign elevated privileges to a set of people other than all course staff, (for example a subset of them) please do the following:

1. In order to assign people to a group, they must have the role of "student". By default, course staff are either "teacher" or "ta", but they can be assigned more than one role. Visit the `People` section and click `+ People`. Specify the users' email addresses and make sure the Role is set to `Student`.
1. Create a [bcourses group](https://community.canvaslms.com/t5/Instructor-Guide/How-do-I-manually-create-groups-in-a-group-set/ta-p/700). The first step will be to create a groupset and then create a group inside it. For example, you can title the groupset "Staff Groups" and the group "Hub Admins".
1. [Add people to the created group](https://community.canvaslms.com/t5/Instructor-Guide/How-do-I-manually-assign-students-to-groups/ta-p/663).
1. Share the bcourses ID in the Github template. The admins will make changes to the DataHub configuration to enable this feature. If you are assigning privileges to a group of people other than course staff, specify this in the Github issue.
1. Once elevated privileges are assigned to jupyterhub groups based on the [DataHub documentation](https://docs.datahub.berkeley.edu/en/latest/admins/howto/course-config.html#assigning-scopes-to-roles), the people being granted those privileges will need to logout of the hub and then log in again for the config changes to persist. This is not the same thing as stopping and starting the server -- users need to click "Logout".
1. You will be able to access the admin interface in the UI by navigating to "<Hub URL>/hub/admin" and check for the admin status of varied users. You will also be able to use the "Manage groups" option in the admin interface to check the bcourses id of courses with admin privileges.
1. Sometimes, users in your course might not be listed as part of the admin interface. During those circumstances, it is recommended that those users log out of the hub and then log back in. It might take sometime for those users to be listed as part of your admin view.

```{note}
If you need any help during this process of creating bcourses groups, please reach out to bcourseshelp@berkeley.edu. Please keep in mind that the bcourses page for the course should be published so that users requiring elevated privileges actually have the required access. 
```

## Admin Dashboard

To access the admin dashboard, login to your hub and click the admin option from the top bar. If you have been recently granted elevated privileges, you will need to first log out and then back in.

```{figure} ../images/adminaccess.PNG
:align: center
:name: DataHub Admin options

```

```{note}
Once you click, you have access to instances of users and admins in that specific hub. The presence or absence of the `admin` term next to a username does not indicate whether or not someone has elevated privileges.
```

### User Servers

1. Click on the control panel.

   ```{figure} ../images/controlpanel.PNG
   :align: center
   :name: Control Panel

   ```
1. Click admin.

   ```{figure} ../images/adminaccess.PNG
   :align: center
   :name: DataHub Admin access

   ```
1. Search for the user.

   ```{figure} ../images/user.PNG
   :align: center
   :name: User List

   ```
1. Click `Start Server` if it is not running. Click `Access Server` or `Stop Server` if it is running.

```{figure} ../images/accessserver.PNG
:align: center
:name: Access Server

Access a student's server.
```

### RStudio

RStudio does not have buttons or links to JupyterHub features like the admin dashboard. To access them when using RStudio, replace `/user/your-calnet-id/rstudio` in the URL with `/hub/admin` to access the admin interface.
