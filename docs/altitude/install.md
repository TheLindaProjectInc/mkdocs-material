# Installation

Most modern day PC's can run the Altitude GUI if running a supported operating system.

Altitude is available for a variety of operating systems, the following have pre-made installation binaries available (Please consult with the [Altitude Github](https://github.com/TheLindaProjectInc/Altitude) if you wish to compile for other operating systems).

- Windows (x86 & x64)
- Linux x64 (AppImage supported OS)
- Mac OS x64

## Minimum Requirements

These are considered the minimum requirements to ensure your system is able to perform blockchain syncronisation and operations effectively. The application may still run on lower specification machines, but good performance cannot be guaranteed.

- 1GB memory
- 10GB free HDD space


## Installation

The installation files for all methods below can be obtained from the [Altitude Github](https://github.com/TheLindaProjectInc/Altitude/releases/latest).

### :fontawesome-brands-windows: Windows

1. Download the version of Altitude required for your OS architecture.
2. Click **Run** on the Windows signature verification prompt.
3. Select the installation option for who you wish to install for, this selection decides where the instalaltion files are placed.
    - Anyone who uses this computer (this will install into the program files directory, and be available for all users of the machine)
    - Only for me (a per user installation, this is the default)
4. Confirm the destination folder path.
5. Click **Install**.
6. Click **Finish**, leave the checkbox selected to start Altitude.
7. When the wallet starts it will obtain connections to the network and begin syncing the blockchain. (A full sync may take a few hours)

### :fontawesome-brands-linux: Linux

1. Download the Linux version of Altitude.
2. Make the AppImage executable by right clicking the file and select **Properties**.
3. Then select the **Permissions** tab and tick the box that says "Allow executing file as program".
4. Then close the window and double click the AppImage file to install Altitude.
> Alternatively, if you prefer the command line, you can simply use `chmod u+x Altitude-linux-x64.AppImage` to make it executable
{.is-info}
5. When the wallet starts it will obtain connections to the network and begin syncing the blockchain. (A full sync may take a few hours)

### :material-apple: Mac OS

1. Download the OSX version of Altitude.
2. Run the downloaded dmg and drag the Altitude icon to your Applications folder when prompted.
3. The first time you run Altitude you will need to right click on the appliaction icon and select **Open** from the menu.
4. Then select **Open** from the displayed window.
5. When the wallet starts it will obtain connections to the network and begin syncing the blockchain. (A full sync may take a few hours)

## Data Directories

These are the default installation directories of Altitude and Metrix Core.

### :fontawesome-brands-windows: Windows

Use the start menu, run bar or Windows explorer address bar to navigate.

**Altitude** : %AppData%\altitude-metrix-wallet 

**Metrix Core** : %AppData%\MetrixCoin
 
### :fontawesome-brands-linux: Linux

These are the default installation directories when installed from the AppImage.

**Altitude** : ~/.config/altitude-metrix-wallet

**Metrix Core** : ~/.metrixcoin


### :material-apple: MAC OS

These are the default installation directories when installed from the DMG.

**Altitude** : ~Library/Application Support/altitude-metrix-wallet

**Metrix Core** : ~Library/Application Support/metrixcoin
