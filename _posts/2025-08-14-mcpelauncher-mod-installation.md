---
title: How to install mods on mcpelauncher? (Linux/Mac)
date: 2025-08-14 12:30:00 +0600
categories: [Minecraft, Modding]
tags: [minecraft, bedrock, mcpelauncher]
media_subpath: /assets/2025-08-14-mcpelauncher-mod-installation/

redirect_from:
  - /mcpelauncher-mod/

image:
  path: '_thumbnail.png'
---


### Introduction
mcpelauncher is a launcher for Android version of Minecraft. It supports both Linux and macOS. It also supports modding of the game (not minecraft addons). The modding community is very small so there are not many mods, but some of them are very useful.

### How to use mods?
> I am not going to demonstrate the in-app mod download UI because it's still not fully ready.  
> I will add it to this guide once it becomes good enough.
{: .prompt-info }

1. First, you have to know which architectures your launcher supports.
   You can check by going launcher Settings -> (scroll down) -> Run troubleshooter
   It will show you something like this...  
   ![](run_troubleshooter.png)

2. As you can see the first entry to support is `x86_64`, this means by default the launcher installs x86_64 compatible APKs.
   So, I will have to get mods that are for `x86_64` architecture.

3. Let's get a mod now, for this tutorial I am going to use mcpelauncher-shadersmod, which makes it easier to add shaders manually.

   - Go to mcpelauncher-shadersmod [release page](https://github.com/GameParrot/mcpelauncher-shadersmod/releases/latest).
   - Download the file with architecture that matches the first entry from step 1. (if no file matching it is available then the mod is unsupported on your system)
   - Extract it if it's a zip

4. Now you should have a `.so` file which is the actual mod.  
![](mod_file.png)

5. Go to launcher settings -> Storage tab -> (scroll down) and click the folder icon next to "Game Data" entry.
   It will take you to a folder named "mcpelauncher"  
![](opening_gameroot.png)

6. There create a folder named `mods` if it doesn't exist already  
![](folder_creation.png)

7. Copy the mod `.so` file from earlier to the `mods` folder.  
![](mod_copy.png)

Congratulations! You have successfully installed a mod. Now the mod should take effect when you launch Minecraft.

> **Warning**  
> - This guide only explains how to install mods, some mods require extra work to actually work.
>   For example, shadersmod requires user to create another folder named `shaders` and putting `.material.bin` files inside it.
> - Since these mods are made by reverse engineering the game, there's always a chance that a mod will stop working when the game is updated.
>   In that case, you have to wait for the mod to be updated.
> - Installing mod which is not supported on your system may crash the game.
{: .prompt-warning }


### Some mods you can try
[**mcpelauncher-fullbright** by CrackedMatter](https://github.com/CrackedMatter/mcpelauncher-fullbright/)  
A mod that will set brightness to max, allowing you to see in dark.

[**mcpelauncher-zoom** by CrackedMatter](https://github.com/CrackedMatter/mcpelauncher-zoom)  
A mod that will allow you to zoom in like OptiFine, you can control zoom level using scroll wheel.

[**mcpelauncher-nohurtcam** by GameParrot](https://github.com/GameParrot/mcpelauncher-nohurtcam)  
A mod that disables hurt animation.

[**mcpelauncher-strafe-sprint-fix** by CrackedMatter](https://github.com/CrackedMatter/mcpelauncher-strafe-sprint-fix/)  
A mod that will fix diagonal sprinting bug that happens with Android x86 builds of Minecraft on Intel CPUs.  

[**mcpelauncher-materialbinloader** by CrackedMatter](https://github.com/CrackedMatter/mcpelauncher-materialbinloader)
A mod that allows user to load RenderDragon shaders from resource packs just like how old shaders worked in 1.18.12 and older versions.  
Note that, it only supports RenderDragon shaders. Also the shader must support the game version, since it doesn't support auto updating shader.