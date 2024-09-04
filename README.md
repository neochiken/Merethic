![Merethic Banner](img/Splash.png)

First things first: **this list contains adult content and you must be of legal age in your country. This means 18+ in most countries, 21+ in others. It is up to you to be sure of the age requirement in your country.**

# What is Merethic?
Merethic is a NSFW Skyrim modlist that aims to improve and add upon the Skyrim experience. It's a power fantasy list with new lands and new areas added to Skyrim to encourage exploring.

# Need Support?
[![DiscordButton](img/DiscordButton.png)](https://discord.gg/WWx6bjmR)

# Contents
- [What is Merethic?](#what-is-merethic)
- [Need Support?](#need-support)
- [Contents](#contents)
- [Preface](#preface)
- [Quick Links (in case you didn't read the table of contents)](#quick-links-in-case-you-didnt-read-the-table-of-contents)
- [Before You Start](#before-you-start)
  - [Hardware Requirements](#hardware-requirements)
  - [Storage Space](#storage-space)
  - [Creation Club Content](#creation-club-content)
  - [Non-Nexus Mods](#non-nexus-mods)
  - [Accounts](#accounts)
- [Installation](#installation)
  - [Preparation](#preparation)
    - [Install Microsoft Visual C++ Redistributable Packages](#install-microsoft-visual-c-redistributable-packages)
    - [Setup your Page File](#setup-your-page-file)
    - [Disable Steam Overlay](#disable-steam-overlay)
    - [Set game language to English](#set-game-language-to-english)
    - [Change Steam's Updating Behavior](#change-steams-updating-behavior)
    - [Clean current Skyrim installation](#clean-current-skyrim-installation)
  - [Wabbajack](#wabbajack)
  - [Commonly Failing Downloads](#commonly-failing-downloads)
- [Post-Installation](#post-installation)
  - [Creating a desktop shortcut](#creating-a-desktop-shortcut)
- [Mod Setup](#mod-setup)
- [Updating Merethic](#updating-merethic)
- [Uninstalling Merethic](#uninstalling-merethic)

# Preface
Just to set some expectations and boundaries surrounding modlist development here, there's a couple things I'd like to say first.

1. As a modlist user, I expect some small efforts into fixing your own issues, mostly by searching the documentation provided here and by the Discord channels. It's very likely any issue you encounter has already been solved - if this is the case and it's well known, don't be surprised if you get ignored.
   
2. Support shouldn't be expected as instant - I have a full time job on top of this, as do my mod team, so I ask for a little bit of patience.
   
3. Do not expect a 100% polished, well-balanced and "perfect" experience. I am a 1-person dev team and expecting more from me than you would from AAA game studios is insanity.
   
4. We're modding a nearly 13 year old game here, please temper your expectations some.
   
5. I won't have a specific area for suggestions for mods to add. I have one for WoD and from what I've seen there and in other modlist situations is that people suggest mods that don't fit a lists theme or generally "bad" mods and then feel as if they're ignored or get annoyed when we say "won't add this".

# Quick Links (in case you didn't read the table of contents)
:arrow_down: [Commonly Failing Downloads](https://github.com/iAmMe27/Merethic/wiki)

:exclamation: [Common Issues](CommonIssues.md)

# Before You Start
<details open>
<summary>Before You Start</summary>

## Hardware Requirements

|             | CPU                             | RAM                 | GPU                                             |
|-------------|---------------------------------|---------------------|-------------------------------------------------|
| Minimum     | Intel 7th Gen,  AMD 3000 Series | 16GB DDR4 @ 3000MHz | RTX 3070 (at least 8GB of VRAM) |
| Recommended | Intel 9th Gen, AMD 5800X        | 32GB DDR4 @ 3600MHz | RTX 4070                        |

## Storage Space

|             | Total Space   | Storage Type        |
|-------------|---------------|---------------------|
| Minimum     | 450GB         | SATA SSD            |
| Recommended | 600GB         | NVMe SSD            |

## Creation Club Content

>[!WARNING]
> Merethic requires all Creation Club content - **you need the $20 AE upgrade from Steam to install!**
>
> Remember to download all of it from the Creations menu in the vanilla game before starting the Wabbajack install.

## Non-Nexus Mods
I recommend you download all of the non-Nexus hosted mods before starting the Wabbajack install. Links to all of these mods can be found on the [GitHub Wiki](https://github.com/iAmMe27/Merethic/wiki).

## Accounts
In terms of accounts you will need:
  * Nexus Premium Account
  * LoversLab Account

Whilst you don't *need* a Nexus premium account to install the modlist, you'll have a considerably better time of it if you do.

</details>

# Installation

<details open>
<summary>Installation</summary>

## Preparation

### Install Microsoft Visual C++ Redistributable Packages
MO2 and various SKSE mods need this - don't skip it.

[Download Visual C++ Redistributable Package.](https://docs.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170)

### Setup your Page File
Skyrim modlists need a large amount of memory purely because of the amount of *stuff* in them - especially modlists on the larger side or with a lot going on, like Merethic. For the best experience, you should setup a pagefile of at least **20GB** - yes, even if you have a million GB of RAM. To setup your pagfile;

1. Hold down the *LEFT* Windows key and press **R**
2. Type in `systempropertiesadvanced` in the run box and then press ENTER
3. Under the "Performance" option, click the "Settings..." button
4. Switch to the "Advanced" tab
5. Under "Virtual Memory", click the "Change..." button
6. Uncheck `Automatically manage...` if it's checked
7. Select your *fastest* SSD in the list of drives
8. Check "Custom Size"
9. Set `Initial Size` to 20480
10. Set `Maximum Size` to 20480 also
    1.  *Note: you can set this up to 40000 if you have the space, this will let the pagefile expand to as large as 40GB*
11. Press the "Set" button
12. Press OK
13. Press APPLY and then OK
14. Restart your PC to apply the pagefile setting

### Disable Steam Overlay
The Steam overlay is known to cause issues for both Skyrim and regular Skyrim SE/AE, especially when using ENBs. I recommend you turn it off to be sure that it doesn't interfere in any way and you can do so by heading into Steam, right clicking on Skyrim in your game library and clicking **Properties** > **General** > **Deselect "Enable Steam Overlay while in-game"**.

### Set game language to English
Wabbajack and some/most of the modding tools out there only support English language versions of Skyrim. Setting the language to English in Steam will stop issues like Wabbajack file verification failures when installing. As with disabling the overlay, right click on Skyrim in your game library and click **Properties** > **Language** > **Select English**.

### Change Steam's Updating Behavior
If for some reason Bethesda decide to release an update for Skyrim, everything will probably break. Well, not *everything* but something will definitely break until mods can be updated to suit. To stop this from happening, you need to tell Steam that you only want to update when you tell it to. You can do this by right clicking on Skyrim in your game library and clicking **Properties** > **Updates** > **Change Automatic Updates to "Only update this game when I launch it"**. Whilst you're in here, it's also recommended to disable Steam Cloud too.

### Clean current Skyrim installation
If you have not yet installed Skyrim, you can skip this part.

1. Right click on Skyrim in your game library and click **Properties** > **Local Files** > **Browse**.
2. Uninstall the game via Steam - right click on Skyrim in your game library and click **Manage** > **Uninstall**.
3. Check the explorer window for any left over files - if there are any, delete them.
4. Open Windows start menu/search and type in `%LOCALAPPDATA%`.
5. Delete the Skyrim folder.
6. Head to `Documents\My Games` and delete the Skyrim folder.

## Wabbajack
Installing the list is straight forward, Wabbajack will do most of the heavy lifting for you - you only have to tell it where to put stuff. Grab Merethic from the iAmDiscord #list-updates channel, once its downloaded the initial stuff it needs, Wabbajack will have 2 things for you to do - fill in the installation location and the download location.

Set the installation location to a folder on the root of a drive, something like `C:\Merethic`. Do not install it to one of the protected folders as mentioned earlier. The download location will have likely been filled in for you too - ensure it matches the directory you set for the installation location, or if you have multiple Skyrim modlists installed, use a common download folder - this will stop you from having to redownload common mods across multiple modlists.

**I recommend you keep your downloads outside of the Merethic installation folder!** It's best if you use a common folder for all of your Skyrim modlist downloads, to save repeatedly downloading the same mods over and over again.

## Commonly Failing Downloads
Downloads from file hosts such as Google Drive and Mega can sometimes be a pain and refuse to download automatically via Wabbajack for reasons unknown. Any files that might give you trouble [can be found here for manual download](https://github.com/iAmMe27/Merethic/wiki).

Download these files and place them *as they are* into the Resource Download folder.

</details>

# Post-Installation

<details open>
<summary>Post Installation</summary>

After Wabbajack has given you the installation successful screen, you're free to close it. Navigate to the Merethic installation folder and run MO2 by double-clicking `ModOrganizer.exe`.

***DO NOT UNDER ANY CIRCUMSTANCES RUN LOOT. The load order is exactly as intended out of the box and you do not need to change it.***

## Creating a desktop shortcut
Nobody wants to be launching their game via multiple clicks, they want to be able to do it from the desktop! This is simple to do - open MO2, ensure **Merethic** is selected in the dropdown and click the "Shortcut" button. From the small dropdown menu, click "Desktop". Of course, you can always run from inside of MO2 by clicking the "Run" button instead.

![Desktop Shortcut Creation](img/DesktopShortcut00.png)

Done! You should now have a shortcut on your desktop which you can now run the modlist from. Don't run Skyrim from within Steam.

</details>

# Mod Setup

<details open>
<summary>Mod Setup</summary>

When starting a new game, create your character and once done, *DO NOTHING ELSE* and allow the mods to initialise.

1. Once initialised, open the MCM Config menu, navigate to the MCM Recorder menu and run `Part 1`. Play the recording and allow it to finish.
2. Save your game and reload.
3. Navigate to the same menu and run `Part 2`.
4. Save your game and reload.

**IED currently needs manual setup:**

Without the game paused, press `BACKSPACE` to open the IED menu and in the top menu bar, click `View` and then `Gear Nodes` to open the Gear Positioning menu.

![](img/IED01.jpg)

In the Gear Nodes menu, ensure you are in the `Global` tab, with the `Player` option selected and then ensure `Sync` is ticked. Then from the `Preset` dropdown, select the `Merethic` preset.

![](img/IED02.png)

Once selected, hit the `Apply` button and then click `OK` on the confirmation dialog box.

![](img/IED03.jpg)

You should also check your inventory for the Merethic Pocket Guide book as that has some useful info you may need when playing.

</details>

# Updating Merethic
When an update is released, please always check the [changelog](changelog.md) first. You may not need to update your modlist but if there is anything that resolves game breaking issues, it'll be noted in the changelog. Backup your saves before you commit to any updates, Wabbajack doesn't usually touch save files, it does has the ability to delete them if it wanted to.

If you have added anything to this modlist at all, Wabbajack will also delete those. You should know how to stop it from doing this if you're going to add stuff to modlists but if you don't, you have to prepend your mod name with `[NoDelete]` - this will make Wabbajack ignore these files. You will need to reinstall these mods and re-sort their load order after an update though, so I hope you kept backup information on where they went in the load order!

# Uninstalling Merethic
Just delete the Merethic folder and it'll be gone.