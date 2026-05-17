# Windows 11 Pro Product Key Activation

Activate Windows 11 Pro using CMD — no third-party tools required.

# Getting Started

Open **Command Prompt as Administrator** by following these steps:

1. Press **Windows key + R** to open the Run dialog.
2. Type `cmd.exe` in the box.
3. Press **Ctrl + Shift + Enter** to run it as Administrator.
4. Click **Yes** when prompted by User Account Control.

You should now see an elevated Command Prompt window.

<img width="1365" height="767" alt="Screenshot 2026-05-15 213242" src="https://github.com/user-attachments/assets/9b079e01-caef-4ed0-8d14-0087e9658fba" />


# Step 1 — Clear Existing License Data

Run the following commands one at a time, clicking **OK** after each prompt:

```
slmgr.vbs /upk
slmgr.vbs /cpky
slmgr.vbs /ckms
```

These commands uninstall the current product key, clear it from the registry, and remove any configured KMS server.

# Step 2 — Check Edition Upgrade Eligibility

Before proceeding, verify that your current Windows edition supports upgrading to Pro:

```
DISM /online /Get-TargetEditions
```

If **Professional** appears in the list, your device is eligible for a free edition upgrade.

# Step 3 — Run the Pro Installer

Copy and paste the following commands into the Command Prompt:

```
sc config LicenseManager start= auto & net start LicenseManager
sc config wuauserv start= auto & net start wuauserv
changepk.exe /productkey VK7JG-NPHTM-C97JM-9MPGT-3V66T
exit
```

Windows will begin the upgrade process and display a progress percentage. This may take a few minutes. 

If an error appears once it reaches 100%, simply click **Exit** — this is expected behavior.

Restart your PC. Windows will install the necessary updates and features during reboot. 

Once complete, go to **Settings → System → About** to confirm that **Windows 11 Pro** is now installed.

> [!IMPORTANT]
> You may notice that Windows is not yet activated and that some settings are restricted. The next step addresses that.

# Step 4 — Activate Windows 11 Pro

Open an elevated Command Prompt again (repeat the steps from the Getting Started section), then run the following commands one at a time:

```
slmgr /ipk W269N-WFGWX-YVC9B-4J6C9-T83GX
slmgr /skms kms8.msguides.com
slmgr /ato
```

Once all three commands complete successfully, Windows 11 Pro will be fully activated. 

You can verify this under **Settings → System → About**.

# Notes

- This guide uses a KMS activation method via `kms8.msguides.com`.
- An active internet connection is required for Step 4.
- If you reinstall Windows, you may need to repeat Step 4.

*If this guide helped you, consider leaving a star on the repository. Thanks for 500+ stars!*
