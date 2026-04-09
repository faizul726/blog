---
title: How to use 4D skins in MB Loader
date: 2026-02-13 11:53:00 +0600
categories: [Minecraft, Modding]
tags: [minecraft, bedrock, 4d, mb loader, skins]     # TAG names should always be lowercase
media_subpath: /assets/2026-02-13-how-to-use-4d-skins-in-mb-loader/

excerpt: Guide on how to use 4D skins in Minecraft with MB Loader

image: thumbnail.png
---

Before I start I want to say that, 
- The name '4D/5D skins' is so misleading. At best you can call it custom model/geometry skin.
- I also assume you have enough braincells to read and understand
- Theoretically, this guide should work for any case and is not limited to MB Loader (if you know what you're doing)

> - Setting data location to media may be risky since it's publicly accessible by any app which may lead to your Microsoft account getting hacked  
> - ONLY follow this guide IF YOU ARE SURE that you don't have any app on your phone that may do something like that.
{: .prompt-warning }  

In this guide we are going to use [Alleis Skin Pack](https://mcpedl.com/alleis-skin-pack/) by [RaiseAlleiseReraise](https://mcpedl.com/user/raisealleisereraise)

1. Open MB Loader -> About, and click the flower icon until it says something like "enabled hidden settings"
2. Go to app settings -> (scroll down) -> Force game data location and set it to `Android/media`
3. Start the game, login with your Microsoft Account
4. Get [Cute Kitty HD Skin Pack](https://www.minecraft.net/en-us/marketplace/pdp?id=f5e0eb10-ee1b-4982-a2a7-46fb1fa770e5) from Marketplace. It's free.  
   Note that this step may vary depending on the 4D skin pack you're getting
5. When it is downloaded, close the game 
6. Open your file manager and go to `Android/media/io.github.bambosan.mbloader/premium_cache`
7. Find the folder that contains the skin pack you just downloaded. (tip: sort it by date to find it more easily)
8. Delete all content inside and replace with the files from Alleis Skin Pack or the one you're intending to use (hint: make sure directory structure is the same)
9. Open the game and new skins should be visible 