---
title: Troubleshooting
---

Try some of the troubleshooting steps documented below. If the issue persists, contact your course TA. If they can’t resolve it, they will reach out to DataHub staff.

## CalNet ID

Ensure your CalNet ID is active.

If you change your CalNet ID mid-semester, your DataHub files will need to be moved. Contact your TA. Let them know your old and new CalNet IDs, and ask that they notify DataHub staff.

## Restart Kernel/Server

Try restarting your kernel to see if the error goes away. If the problem persists, restart your server.
 
## Kill Process

Having too many things open on DataHub can cause issues. There are two different approaches to view running processes and kill them.

### Jupyter Lab

. In Jupyter Lab, click the icon at the far left depicting a square within a circle. It displays open tabs, running kernels and language servers, and open terminals. Hover your mouse over any entry and a close icon (X) will appear. Click on the close icon to shut down that entry.

### Terminal

1. Open the terminal in your DataHub session.
1. Run `ps aux` to list all running processes.
1. Find the process ID (PID) of the processes you want to stop.
1. Use the command `kill <PID>` to terminate those processes.
1. Repeat these steps as necessary.
