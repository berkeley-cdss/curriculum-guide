---
title: SyncThing
---

[SyncThing](https://syncthing.net) enables hub users to share data with any other person running the same app. This could be themselves running SyncThing on their own personal computer, or another user on the same hub.

## Device ID

Each instance of SyncThing running is called a "Device". To share data with a device, you will need to tell your instance about it.

Login to a hub with SyncThing available, and launch it.

```{figure} ../assets/launcher-syncthing.png
:align: center
:name: Launcher with SyncThing

Jupyter Lab launcher with SyncThing
```

SyncThing uses IDs to identify each application instance. To find the ID, access `Actions` > `Show ID`.

```{figure} ../images/syncstep1.2.PNG
:align: center
:name: Show Device ID

Find the ID within the application.
```

## Sharing Data

To share data with another Device, click `Add Remote Device` and enter
the ID. You can give the device an easy-to-remember name.

```{figure} ../images/syncstep1.1.PNG
:align: center
:name: Add Remote Device

Add a remote device.
```

Check whether the devices are synced by looking at the available
devices. Create a folder where you want to upload all your content and
share with your collaborators. Select the "Add Folder" option to create
a folder. Click the "Sharing" tab and from the listed devices and
select the device to which you want to share this folder.

```{figure} ../images/syncstep4.PNG
:align: center
:name: Share Folder

Share a folder with your collaborator(s).
```

If your collaborator wants to provide access to a folder, you need to share your device ID with them. Once they are able to add your device id to the shared folder, you will receive a notification like the one shown below. It may take a few minutes to receive these notifications.

```{figure} ../images/syncstep3.PNG
:align: center
:name: SyncThing Notification

Notification when a collaborator adds you to a shared folder.
```

## Step By Step

Below is a short animation that walks you through the step-by-step process:

```{figure} ../images/syncthingdemo.gif
:align: center
:name: SyncThing Demo

Demo of SyncThing.
```
