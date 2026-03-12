---
title: 'How to use RenderDragon shaders on Minecraft Bedrock [Android/iOS/Windows/Linux] [WIP]'
date: 2026-03-12 17:00:00 +0600
categories: [Minecraft, Modding]
tags: [minecraft, bedrock, shaders, renderdragon]     # TAG names should always be lowercase
#media_subpath: /assets/2026-02-13-how-to-use-4d-skins-in-mb-loader/

#image: thumbnail.png
excerpt: '[WIP] Guide on how to use RenderDragon shaders on some popular platforms'
---

# What are RenderDragon shaders?
RenderDragon shaders are unofficial third party shaders made by the Minecraft community. These are not supported in the original game without third party modding involved.  
This guide explains some ways that you can follow to use these shaders on Android, iOS, Windows and Linux.

> - These shaders being unofficial makes them very prone to breaking whenever Minecraft receives a medium/big update. So make sure the shader you're going to use supports your game version
> - As mentioned before, you need third party tools or these shaders will simply not work
> - Some shader creators intentionally cause confusion by not updating compatibility notes or giving out vague information. So you may run into issues :v  
{: .prompt-warning }

## Android
### Using MB Loader (recommended)
You need Minecraft installed for this. Preferably version that's not heavily modified (sailors will know what I mean)
{: .prompt-info }

1. Get MB Loader from Play Store
2. Open the app. Click Load with MBL2/Draco. Both are same except MBL2 is more robust.
3. Import the shader you want to use
4. Go to game settings -> Global resources, and activate the shader (Don't apply inside world settings. That's a very bad habit)

## iOS
I will ping her and some other people for guide on this :sob:

## Windows: 
### Using BetterRenderDragon
Well, since the current maintainer doesn't really want to give out any instructions (perhaps to move people to their Minecraft Launcher), I will show you an somewhat unofficial way of getting it working.
{: .prompt-info }

1. Get Fzul's BRD Manager Script
2. Double click the script
3. Click 1 on your keyboard to install
4. Now if everything went alright (and you're not using some heavily modded Windows or something), it should be installed. 
5. Now it should start automatically each time when you open the game, there will not be the blue small window by default but shaders will still work. Just import your shader and activate it in Game settings -> Global resources

### Using Matject
While Matject still works but it's default behavior is not suitable in current situation
{: .prompt-warning }

1. Download Matject
2. Extract and open matject.bat
3. Go through the exam (real) and setup process. When prompted to setup material-updater, reject it as it doesn't work anymore
4. Get the shader MCPACK file
5. Put it in the MCPACKs folder of Matject
6. In Matject select Auto by clicking 1 on keyboard
7. Confirm things and let it inject
8. Now it has put "core shader files" into Minecraft you still need to import the resource pack for it to fully work.
9. Import and activate the resource pack in game settings -> Global Resources

## Linux (my beloved):
This guide exclusively applies to mcpelauncher which is a way to play the Android version of game without any emulation (like emulators do)
{: .prompt-warning }

### Using mcpelauncher-shadersmod
This one is more preferable because it doesn't heavily rely on game mechanics and supports wider range of devices. One problem is it requires manual work everytime you want to use a different shader. You can use my helper script if you want to make it a bit easier

1. Get mcpelauncher shaders mod
2. Activate the mod following the "guide"
3. Extract .material.bin files from base (`./renderer/materials`) to `<mcpelauncher root>/shaders` folder
4. If the shader has subpacks you also need to copy .material.bin files from the respective subpack folder that you are intending to use
5. Open the game, import the resource pack, activate in game settings -> global resources (select correct subpack if it has any)

### Using mcpelauncher-materialbinloader
This one is probably outdated as of now and only supports `x86_64` arch

1. Get mcpelauncher-materialbinloader mod file
2. Activate the mod following the "guide"
3. Import the shader resource pack in game and activate in game settings -> Global resources
4. Now shader should work