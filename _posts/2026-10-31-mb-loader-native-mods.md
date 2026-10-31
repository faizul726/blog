---
title: Native Mods in MB Loader
date: 2026-10-30 07:40:00 +0600
categories: [Minecraft, Modding]
tags: [minecraft, bedrock, mb loader, shaders, renderdragon]     # TAG names should always be lowercase
#media_subpath: 

#image: thumbnail.png
excerpt: Explaining native mods in MB Loader app
---

> This article is not written yet. I will update this later in my free time
{: .prompt-info }

### Dynamic Shadows
Adds actual shadows to the game that change depending on sun/moon position. Doesn't rely on any shader loader or any RD (RenderDragon) shader.  
You can customize it from settings.

### Custom Buffers
Enhances RD shader capability by exposing certain features the game normally doesn't. A RD shader utilizing these can have better water reflection, colored shadows and many more. This is still new so majority of the shaders will not utilize this.

### Depth of Field Blur (DOFBlur)
Adds blur effect to your surrounding based on where you're looking. It's quite resource heavy so keep that in mind.  
You can customize it from settings.