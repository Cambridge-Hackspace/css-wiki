# 3D Printer Remote Printing (OctoPrint / SimplyPrint)

## Overview
This page covers adding CHS members to remote printing on the Prusa via the OctoPrint server, and connecting PrusaSlicer and SimplyPrint to it. See the main [3D Printers](TOOLS/3D-PRINTING/3d-printer.md) guide for general printer use and rules.

Printing through OctoPrint and PrusaSlicer works only while you are in the Hackspace and connected to the local network. It is best for short print sessions where the member stays in the space until the print completes.

## Step 1: Create a member account on OctoPrint
1. Open a web browser to the OctoPrint server (the Hackspace Prusa) — its address is shown on the Prusa's control panel; ask a trainer if unsure.
2. Log in with the OctoPrint admin account (credentials from a trainer or the shared credentials store).
3. Go to **Settings → Access Control → Users**, then click **+ Add user…**

![OctoPrint Settings with the Access Control panel open, showing the Users list and the Add user button](assets/tools/3d-printer/octoprint-img01.png)

4. Fill out the new member's username and password.
5. Assign the correct permission: under **Groups**, check **Operator**.

![OctoPrint Add user dialog on the Groups tab with the Operator group checked](assets/tools/3d-printer/octoprint-img02.png)

6. Verify the new user can log in to OctoPrint.
7. Review the basics of the OctoPrint interface and show the member how to "connect" to the printer and monitor its status.

## Step 2: Set up PrusaSlicer to use OctoPrint
This lets the member print directly from PrusaSlicer to the Prusa through OctoPrint (only while in the Hackspace and connected to the local network).

1. In PrusaSlicer, in the right-hand control panel under **Printer**, select **Add Physical Printer**.
2. In the printer setup, fill out three fields:
   - **Hostname, IP or URL:** whatever is displayed on the Prusa's control panel (ask a trainer if unsure).
   - **Descriptive name:** give it a name so you know prints are going to OctoPrint.
   - **API Key / Password:** paste the API key from OctoPrint (see next step).

![PrusaSlicer Add Physical Printer dialog showing the descriptive name, Host Type set to OctoPrint, the IP field, and the API Key field](assets/tools/3d-printer/octoprint-img03.png)

3. Get the API key from OctoPrint:
   1. In OctoPrint (logged in as the user), go to **Settings → Application Keys**.
   2. Click **Generate** to create an app key.
   3. Copy the key and paste it into the PrusaSlicer printer setup's API Key field.
   4. Click **OK** to save.
4. Test that it can print:
   1. Open a model in PrusaSlicer and slice it with the OctoPrint-connected printer selected.
   2. A new icon appears next to the Export G-code button — click it to push the print to the Prusa through OctoPrint.
   3. Open OctoPrint to monitor the print.

## Step 3: Connect SimplyPrint
1. Verify you're at the Hackspace and connected to the local network.
2. Log in to OctoPrint in a web browser.
3. In a new browser tab, go to the SimplyPrint website and make a new account.
4. Once logged into SimplyPrint, in the left toolbar select **Add printer** (the "+" icon at the bottom of the panel). With OctoPrint logged in on another tab, it should find the Prusa through OctoPrint. Give it a descriptive name. Since you'll be pushing G-code to the printer, adding filament is not necessary.

![SimplyPrint web panel Printers view with the Add printer button highlighted](assets/tools/3d-printer/octoprint-img04.png)

5. Back in PrusaSlicer, export the G-code file from the model you sliced earlier.
6. In SimplyPrint, select **Start Print** and upload the file you just exported (or upload the G-code to the "Your files" section).

![SimplyPrint control panel for the Prusa i3 MK3S showing movement controls, filament, and the printer camera](assets/tools/3d-printer/octoprint-img05.png)

## Resources
- [3D Printers (main guide)](TOOLS/3D-PRINTING/3d-printer.md)
- [Tool Training](TOOLS/tool-training.md)
