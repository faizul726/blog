---
title: How to use Wyvern Shader Loader for Minecraft on Windows
date: 2026-07-06 08:10:00 +0600
categories: [Minecraft, Modding]
tags: [minecraft, bedrock, renderdragon, shaders, windows]     # TAG names should always be lowercase
media_subpath: /assets/2026-07-06-how-to-use-wyvern-windows/

image: wyvern_hero.webp
excerpt: Guide on how to setup and use Wyvern on Windows
---

> - This shader loader is new and is not guaranteed to work.  
> - As of writing this article, the mod is confirmed working on MC v26.32
> - This guide only applies to GDK version of Minecraft which is v1.21.120+ 
> - Due to the nature of memory manipulation programs, this may get falsely flagged as virus/malware by your antivirus. You may need to whitelist it in your antivirus for it to work.
{: .prompt-warning }

Let's get straight to the topic. 

## Installation
1. Download `WyvernSetup.exe` from [wyvern_releases repo](https://github.com/mcbegamerxx954/wyvern_releases/releases/latest)

2. Setup Wyvern (you don't have to worry about any options it gives)

3. In Start menu, you will see new app named 'Wyvern'. Open it.

**Now there are two ways you can start it:**

- You can open Minecraft and then click on the 'Inject' button
- Or, you can enable "Load on startup". Which will leave a background process that will start with Windows and inject into Minecraft everytime you start the game.  
  You can close it anytime by right-clicking Wyvern icon in taskbar and clicking 'Exit'

## Usage
1. Import your shader resource pack
2. Go to Minecraft settings -> Global Resources and activate the shader (preferably put it on top)
3. Now shader should work. If it doesn't, try re-activating the resource pack or restart game. 

> - Shaders **must** be put in Global resources not inside world settings. Or it will not work
> - Wyvern Shader Loader only serves the purpose of loading shader. It has **absolutely nothing** to do with how shader looks in-game. It's your job to find shaders that work for your game version.  
> - You need to use shaders that work on Windows. Using Android/iOS only shader will result in crash. 
{: .prompt-warning }


## Uninstallation
- Go to Settings -> Apps & features 
- Find Wyvern and uninstall

Have a good day!