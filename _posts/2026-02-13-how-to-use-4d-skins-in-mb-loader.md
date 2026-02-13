---
title: How to use 4D skins in MB Loader
date: 2026-02-13 11:53:00 +0600
categories: [Minecraft, Modding]
tags: [minecraft, bedrock, 4d, mb loader, skins]     # TAG names should always be lowercase
media_subpath: /assets/2026-02-13-how-to-use-4d-skins-in-mb-loader/

image: thumbnail.png
---

Before I start I want to say that, 
- The name '4D/5D skins' is so misleading. At best you can call it custom model/geometry skin.
- 🟥 I ASSUME you can modify files in `Android/data/io.bambosan.mbloader`. 
If you don't, you may be able to do that with Shizuku and a compatible file manager. But that's for you to figure out.
- I also assume you have enough braincells to read and understand
- Technically you can skip to step X if you have root/have access to internal data
- Theoretically, this guide should work for any case and is not limited to MB Loader (if you know what you're doing)


In this guide we are going to use [Alleis Skin Pack](https://mcpedl.com/alleis-skin-pack/) by [RaiseAlleiseReraise](https://mcpedl.com/user/raisealleisereraise)

1. Open MB Loader -> Settings and set 'Force game data location' to External
2. Start the game, login with your Microsoft Account
3. Get [Cute Kitty HD Skin Pack](https://www.minecraft.net/en-us/marketplace/pdp?id=f5e0eb10-ee1b-4982-a2a7-46fb1fa770e5) from Marketplace. It's free.  
Note that this step may vary depending on the 4D skin pack you're getting
4. When it is downloaded, close the game 
5. Open your file manager and go to `Android/data/io.bambosan.mbloader/premium_cache`
6. Find the folder that contains the skin pack you just downloaded.
7. Delete all content inside and replace with the files from Alleis Skin Pack or the one you're intending to use (hint: make sure directory structure is the same)
8. Open the game and new skins should be visible 