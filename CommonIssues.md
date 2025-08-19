# Common Issues

- [Common Issues](#common-issues)
  - [Preface](#preface)
  - [Download Issues](#download-issues)
      - [Missing Files](#missing-files)
      - [Commonly Failing Downloads](#commonly-failing-downloads)
      - [Nexus Login Expired](#nexus-login-expired)
      - [Nexus Server Issue](#nexus-server-issue)
      - [Incorrect Game Files](#incorrect-game-files)
      - [File/Mod not Available](#filemod-not-available)
  - [Installation Issues](#installation-issues)
      - [Could Not Find Part Of The Path](#could-not-find-part-of-the-path)
      - [Sanity Check Error whilst installing Rayek's End](#sanity-check-error-whilst-installing-rayeks-end)
  - [Game Crashes](#game-crashes)
    - [Common Crashes](#common-crashes)
      - [1. Overlay Software](#1-overlay-software)

## Preface
Please help me to help yourself here. Search this page and please also use the Discord search function in the Merethic channels as your issue may already be solved. Do not just post a question in the support channel without doing your own research first.

## Download Issues

>[!CAUTION]
> If wabbajack throws an error, **DO NOT CLICK THE RETRY BUTTON**.  
Clicking the retry button will delete already downloaded mods and cause them to be downladed again, wasting your time.  
> 
> Instead, read carefully what kind of problem Wabbajack encountered, close Wabbajack, fix the error and then start the wabbajack installation again.

If you are not able to fix your Wabbajack error, or it is not listed in this list, please ask for support in our discord. Link is on the [ReadMe](README.md).

### Missing files
If you encounter an error looking like this:  
![Wabbajack missing files error](img/wj_MissingFiles.png)
  
Click the "Show Missing Archives" button.  
A browser windows will open, showing the **EXACT NAMES** of the file you need to download, and a link to each file. Make sure you downloaded the correct file and the filenames match. Put the downloaded files in the Wabbajack downloads folder and start Wabbajack again.

### Commonly Failing Downloads
It's one of the files on the commonly failing downloads list. Wabbajack even gives you report now, please read that to know exactly what files you missed. [All commonly failing downloads can be found on the Wiki page here.](https://github.com/iAmMe27/Merethic/wiki)

### Nexus Login Expired
Your Nexus login expired. In the Wabbajack settings, log out of Nexus and then re-login.

![Nexus Relog](img/NexusRelog.png)

### Nexus Server Issue
The Nexus server you are downloading from is having issues, try switching your preferred Nexus download server to something close to your location in the account settings. You can access this area by clicking on your account in the top right, and selecting site preferences.

### Incorrect Game Files
Your game files are wrong - this will give a clear error in the Wabbajack log, like so:

![Game file error](img/GameFileError.png)

To fix this, you need to ensure your game is set to English in Steam and then verify your game files with Steam.

### File/Mod not Available
You'll need to wait for a modlist update.

## Installation Issues

1. Hashes don't match for texture files (files that end in `.dds`) - Your Wabbajack version is outdated, make sure you are using v4.0.0.0 or later.

2. File is corrupt (usually `.bsa` files) - Wabbajack will tell you what file the error is with in its log as well as to delete it and retry the install. Follow the steps given to you by Wabbajack.

3. Your storage drives are full - both the installation drive and the drive you have Wabbajack on need a free space for the installation to be possible.

4. You didn't setup antivirus exclusions.

### Could not find part of the path
If you encounter an error looking like this:  
![Wabbajack could not find part of the path error](img/wj_PartOfPath.png)

Do the following:
1. Close wabbajack
2. Go to your install folder and locate the TEMP_BSA_FILES folder if it exists.
3. Empty that folder if it exists
4. Restart wabbajack
5. Restart Modlist installation.

#### Sanity Check Error whilst installing Rayek's End
This is actually caused by your PC having a different system locale installed, such as Japanese alphabets. [There is a simple fix here.](https://github.com/ForgottenGlory/Living-Skyrim-2/issues/69#issuecomment-643644342)

To summarise the fix here, you need to:
1. Open the Rayek's End zip file.
2. Manually extract `Meshes\Oaristys\Clutter\Mirror • nif` and place it in `Merethic\mods\Rayek's End - SSE Expanded Edition` (so you should have a file path of `Merethic\mods\Rayek's End - SSE Expanded Edition\Meshes\Oaristys\Mirror • nif`).
3. Rename the NIF file to `Mirror°.nif` (this is the degrees symbol).
4. Rerun Wabbajack, it should see this renamed file and continue on with the install.

## Game Crashes
Heavily modded Bethesda games are prone to crashing at times. Generally speaking, the following is true:

1 crash is a fluke, 2 crashes is weird but not impossible, 3 is a repeatable crash worth reporting and/or investigating.

Before you report a crash, consider these rules and also read below to see if your issue is already known about.

### Common Crashes

#### 1. Overlay Software
Software such as **Medal**, **EVGA Precision** and **MSI Afterburner** are the most common causes of this - anything that hooks the display to show or record stuff on screen. Close the software and test again.

#### 2. OBody Crashes
OBody crashes are not actually caused by OBody but actually by the RaceMenu DLL `skee64.dll` - in these types of crashes, you will see this DLL referenced. These crashes happen just as you're travelling through the world and are random.

Merethic has all the known fixes, tweaks and INI settings implemented but these still happen from time to time. The OBody devs blame RaceMenu and the RaceMenu dev blames OBody so we're likely not going to get a fix for this one any time soon.
