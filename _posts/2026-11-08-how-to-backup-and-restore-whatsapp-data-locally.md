---
title: How to backup and restore WhatsApp/Business data locally in 2026
date: 2026-11-08 07:00:00 +0600
categories: []
tags: []     # TAG names should always be lowercase
#media_subpath: 

#image: thumbnail.png
---

### What happened and why I am writing this
I feel ashamed that even as a experienced user who haven't lost WhatsApp data in past 4 years, I made a huge mistake and ended up losing all chat. Luckily, I had a local backup from February 2025 but still I have lost 20 months of chat! 
I wouldn't say that this is entirely my fault. WhatsApp themselves are also responsible which I will go over now.

Yesterday, I was backing up all of my data as a part of my goal to fully get rid of Google Play Services and use microG. That's when I saw that besides Google Drive, it's possible to use WhatsApp cloud or whatever it's called. I wanted to take advantage of it as I didn't want to login my main Gmail with microG. So, I tried a lot of ways and I was unable to trigger a backup to that cloud. In the process I had deleted my Google Drive backup (which I had made as a precaution). 

Then I realized I can make a local backup (supported by WhatsApp), I looked up and there's nothing of that on official WhatsApp help site. So, I added `site:reddit.com` to my query and looked up on Reddit threads. After reading, I took a backup of `Android/data/media/com.whatsapp/WhatsApp/Databases` folder and uninstalled WhatsApp thinking that's all the data. 

And guess what? That `Databases` folder is not all, there were 2 more folders named `Backups` and `Media`. I realized that when I decided to check size of Databases folder. 

This is the dumbest thing possible, I should have still made a backup to Google Driver before uninstalling, I could even have made a full app backup using SwiftBackup but I did none of that. And also that Databases folder alone didn't work in the app. So essentially, I am left with the only what possibly could be text messages which I will now have to use a third party tool to see. This wouldn't have happened if WhatsApp had written on how to backup locally. But tech giants really love abstraction and they don't really want people to do the advanced stuff. 

Okay, that's a lot of speech. I will write the main part now.


### How to backup
> You must not be connected to internet in the process. Mainly because if someone sends you a message after you have made the backup, that new message will not be included.
{: .prompt-caution }

> WhatsApp UI/behavior may change over time so this guide may become partially or fully outdated
{: .prompt-caution }

1. Make sure you're logged in on a single device. If you're logged in on other devices, either log out or disconnect internet from other devices. As we need a single source of truth.
2. Disconnect from internet on the main device
3. Go to `You (your profile icon) -> Chats -> Chat backup` and click "Backup"
4. Doing so will first create a local backup and if you're connected to Google Drive then it will attempt to backup but fail. You don't have to worry about that unless you want to keep a backup on Drive as well.
5. Uninstall WhatsApp and do not login to WhatsApp or let it access internet in anyway (on other devices)
6. Create an empty folder where you want to store.
7. Create a blank/text file named `.nomedia` (optional, this will make sure your gallery doesn't get spammed with WhatsApp images)
8. Copy `Android/media/com.whatsapp` folder (for WhatsApp Business, `Android/media/com.whatsapp.w4b`) to your folder that you created in step 6. Do note that those folders should contain folders like `Backups`, `Databases`, `Media` inside another folder. Take a note of size just to be sure.

Now backup is done, let's go to restore part

### How to restore
1. Copy your backed up folder `com.whatsapp` or `com.whatsapp.w4b` to `Android/media`. Make sure directory structure is same like this:
```
// Generated with https://utilitycove.com/tools/folder-structure-generator

└── Android/
    └── media/
        └── com.whatsapp.w4b/
            └── WhatsApp Business/
                ├── Backups/
                │   └── ...
                ├── Databases/
                │   └── ...
                └── Media/
                    └── ...
```
For normal WhatsApp it would be `com.whatsapp/WhatsApp`.

2. Install WhatsApp
3. Be careful of each step you go through in the app so you don't miss the restore prompt. Else you will end up in a state where messages after inetnet cut will has arrived and all messages before that are missing. You wouldn't be able to easily merge two message history
4. Login your account in WhatsApp and go through each screen very carefully
5. When prompted to restore data from Google Drive or transfer from other device, skip
6. Then you will be shown a screen telling you that it found a backup and ask you to restore, alongside size of the backup
7. Let it restore and don't interrupt or let device go to sleep

Now if everything went correctly, your backup will be restored and any messages that were sent to you after internet cut off will come up as unread.