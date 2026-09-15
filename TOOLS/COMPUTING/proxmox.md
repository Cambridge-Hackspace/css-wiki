# Proxmox VM Creation

## Overview

How to create a virtual machine (VM) on the Hackspace Proxmox server. This is an
abridged guide focused on the specifics of our setup — there are many general
Proxmox tutorials online for the parts not covered here.

## Step 1 — Log in to the Proxmox server

From a browser on the Hackspace wifi, go to the Proxmox web GUI (the server
address and your login are shared on Discord / ask an admin). Your browser may
warn that the site's certificate isn't recognized — you can safely bypass that
warning to reach the Proxmox web GUI.

You'll see a login prompt in the center of the screen:

![Proxmox login prompt](assets/tools/computing/proxmox/img01.png)

By default the **Realm** is `Linux PAM standard authentication`. Change it to
**`Proxmox VE Authentication server`** as shown below, then enter the username
and password you were given on Discord. After clicking **Login** you'll see the
full Proxmox GUI.

![Realm dropdown set to Proxmox VE Authentication server](assets/tools/computing/proxmox/img02.png)

## Step 2 — Change your password

The password you were given on Discord is a starter password known by the
admins — change it first.

In the upper-right corner you'll see `your_name@pve` with a dropdown caret. Click
it and select **Password**.

![Account dropdown with the Password option](assets/tools/computing/proxmox/img03.png)

You'll get a standard password-reset form:

![Password reset form](assets/tools/computing/proxmox/img04.png)

## Step 3 — Download an install ISO

You need an `.iso` file to install your operating system from. Find your OS's
download page and copy the direct download URL (the actual file link, not an
intermediary page).

In the left-hand menu, select **`local (bass)`** under the `bass` node, then
**ISO Images → Download from URL**.

![local (bass) → ISO Images → Download from URL](assets/tools/computing/proxmox/img05.png)

Paste the URL into the top field of the popup:

![Download from URL popup](assets/tools/computing/proxmox/img06.png)

Click **Query URL**. If it works, a file name populates and the **Download**
button becomes clickable. Click it and wait for the ISO to download — it will
then be selectable when you create the VM.

## Step 4 — Create the VM

In the upper-right corner, click **Create VM** (next to Create CT).

![Create VM / Create CT buttons](assets/tools/computing/proxmox/img07.png)

You'll see the VM creation wizard:

![VM creation wizard](assets/tools/computing/proxmox/img08.png)

First you **must** select the **Resource Pool** — this grants the right
permissions and organizes who runs which VMs. Every member has their own pool, so
you should only see your own name; select it.

![Resource Pool selection](assets/tools/computing/proxmox/img09.png)

Under **OS**, choose from the list of ISO files — pick the one you downloaded:

![OS / ISO selection](assets/tools/computing/proxmox/img10.png)

The remaining steps are standard and covered in online tutorials, **except the
Disks section**: for **Storage** select **`member-vms2`**, and set a **Disk Size**
of up to **64 GB**. (If you genuinely need more, message an admin about
allocating more space.)

![Disks section: member-vms2 storage](assets/tools/computing/proxmox/img11.png)

It takes a few seconds to initialize — watch its status in the tasks bar at the
bottom of the screen.

![Task status bar](assets/tools/computing/proxmox/img12.png)

Navigate to **Console** to set up your image.

![VM Console](assets/tools/computing/proxmox/img13.png)

## Notes

- There are no other hardware restrictions for now, but limits may be added later if resources become strained.
- You can also install **containers** ("CT" in Proxmox). Containers use fewer system resources, so prefer them where feasible. The process is well covered in online tutorials.

## Resources

- Community-developed helper scripts (not officially supported or vetted — use your best judgment): <https://community-scripts.github.io/ProxmoxVE/scripts>
- The official Proxmox docs are good for troubleshooting: <https://pve.proxmox.com/pve-docs/>
