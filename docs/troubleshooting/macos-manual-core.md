# MacOS Manual Core Install

The below document details the steps to manually apply the Metrix core daemon to an Altitude installation. This is normally required on newer OSX installations due to heightened security measures by Apple with regards to running unverified executables.

!!! warning "Note"
    This process may be required on both existing installations and new Altitude installtions.

1. First download the latest core release from [Metrix Core for Windows, Linux & Mac](https://github.com/TheLindaProjectInc/Metrix/releases/latest) for MacOS you will only need the **metrix-darwin-x64.tar.gz**, once downloaded this will appear in your downloads directory.

![core_stopped.png](/assets/troubleshooting/macos-manual-core/step1.png)

2. Double click to extract this into the Downloads directory. Select and copy the **metrixd** file from the directory.

![core_stopped.png](/assets/troubleshooting/macos-manual-core/step2.png)

3. Access the hidden Library folder.
In the Finder, hold down the **Option** key when using the **Go** menu. **Library** will appear below the current user's home directory.

![core_stopped.png](/assets/troubleshooting/macos-manual-core/step3.png)

4. Open **Application Support**

![core_stopped.png](/assets/troubleshooting/macos-manual-core/step4.png)

5. Open **altitude-metrix-wallet**

![core_stopped.png](/assets/troubleshooting/macos-manual-core/step5.png)

6. Open **clients**

![core_stopped.png](/assets/troubleshooting/macos-manual-core/step6.png)

7. Paste the **metrixd** file copied earlier into this directory.

![core_stopped.png](/assets/troubleshooting/macos-manual-core/step7.png)

8. You can now exit Altitude and relaunch it. The wallet should successfully open and sync.
If you get the following error continue with the below steps (Most new OSX installs may get this).

![core_stopped.png](/assets/troubleshooting/macos-manual-core/step8.png)

9. Open **System Preferences** or **System Settings** on new installations.

![core_stopped.png](/assets/troubleshooting/macos-manual-core/step9.png)

10. Click **Security and Privacy**

![core_stopped.png](/assets/troubleshooting/macos-manual-core/step10.png)

11. Click the padlock to allow changes and then **Allow Anyway** the **metrixd** application to be launched. (*If metrixd does not appear here, try launching Altitude first, its should appear in here for up to 1 hour after unsuccessful launch*)

![core_stopped.png](/assets/troubleshooting/macos-manual-core/step11.png)

Altitude can now be launched and the wallet should run. You may get an additional prompt to open the metrixd, however once this has been opened once it should not prompt in future launches for this version.

!!! warning "Support"
    Should you require additional support during this process, or continue to have launch issues after completing this, please log a support ticket on the [Metrix Discord server](https://discord.gg/ZFqJu4c)
