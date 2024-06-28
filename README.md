# Windows 11 Pro productkey activation
Activation Windows 11 Pro product key with CMD
# Get Started
Open Comman Promote as adminstrator in your Windows 11 by using this command

Windows-logo-key + R      

Now Type "cmd.exe" in the box

![image](https://github.com/elfordanson/windows_11_pro_productkey_activation/assets/116512676/0483880c-43c7-4144-81d6-bc781906aca0) 

Press ctrl+shift+enter

Then Click "YES"

Now will you have something like this:

![image](https://github.com/elfordanson/windows_11_pro_productkey_activation/assets/116512676/e322f8ce-f447-4179-9a6d-afc2d301ae94)

# Commands

Now, type the following command: slmgr.vbs /upk Now it will give an message, click on OK

And now this command: slmgr.vbs /cpky It will give an message once again, and click on OK again

And now type this command: slmgr.vbs /ckms Once again click on OK when you get an message

# Edition upgradable check command

Now we are gonna check of your edition is supported to upgrade to Pro, run the following command to check this: DISM /online /Get-TargetEditions If you see "Professional" in the list, then you can upgrade your Windows edition to Pro for free!

# Run Pro installer

Now, copy and paste this complete command:

sc config LicenseManager start= auto & net start LicenseManager

sc config wuauserv start= auto & net start wuauserv

changepk.exe /productkey VK7JG-NPHTM-C97JM-9MPGT-3V66T

exit

It will run an installer and you will see an message:"% complete"

Now wait until it's 100% and it's not weird that you will get an error

When you get the error, just click Exit and then reboot your pc.

You will now see an message that he is running updates and is installing features, just wait until its done and check "info" in settings, You will see that Windows 11 Pro is installed!

But we are not done, You will see that it isn't activated and that you can't change some settings, now we are gonna fix that!

# Activating Windows Pro

Now we are gonna run some other commands to activate Windows 11 Pro

Press these keyboard keys once again:

Windows-logo key+R

It looks like this again:

![image](https://github.com/elfordanson/windows_11_pro_productkey_activation/assets/116512676/0483880c-43c7-4144-81d6-bc781906aca0) 

Run Dialog With cmd.exe Text In It

Press ctrl+shift+enter

You will get an message, just click on Yes

Now you will get an Command Prompt.

Type the following commands one for one to activate:

slmgr /ipk W269N-WFGWX-YVC9B-4J6C9-T83GX

slmgr /skms kms8.msguides.com

slmgr /ato

Now you have Windows 11 Pro and it activated! You can check settings to see it.
