# 📈 Minecraft-performance-guide
A guide on how to fully optimize Minecraft: Java Edition to squeeze out every, and last frame per second. I'm creating this for people with low end hardware, aka those who have troubles with running Minecraft at a playable, stable framerate. I've been a low end player for a while and I know the pain, and I wanna help by bringing you the biggest optimization guide!

**Q: Will these tweaks mentioned break my system, Bonzi?**

**A:** It shouldn't. I've done most of these on my old, low end laptop and it didn't do too much harm. But since this is more organised, there's a smaller chance to break anything

**WARNING: If you end up breaking anything, I cannot be held accountable. I am just trying to help people.**

## 🧽**1. Optimizing Windows 10**

**(Note: If you use MacOS or any sort of Linux Distro, skip this first step!)**
Windows 10 is, by default, very badly optimized. Things such as bloatware, background apps, services, search indexing, telemetry and much more will make your game and system lag. So let's get started!

## **BEFORE DOING ANY OF THESE TWEAKS, MAKE SURE YOU HAVE ALL THE LATEST UPDATES FROM MICROSOFT INSTALLED TO MINIMIZE ERRORS!**
## **Debloat**

* Debloating will remove all of the unnecesssary bloatware from Windows 10. Freeing up background processes, storage, and most importantly RAM. RAM (random access memory) is basically memory used to run the OS and programs. Windows 10 uses 1,5 - 2,5 gb whilst idle from my experience, which is very bad, especially for low end systems with 4gb of ram.

* For the purposes of this guide, we will be using [Sycnex's Windows 10 Debloater](https://github.com/Sycnex/Windows10Debloater). Download the debloater by clicking on the green "code" button and downloading it as a ZIP file. Once done, extract the contents to somewhere accessible, eg. desktop or documents. Find the file called ``Windows10DebloaterGUI.ps1`` and right click on it and click "run with powershell".

[This is the GUI you will see.](https://i.imgur.com/JXOxWzq.png) Click on `remove all bloatware`, `disable cortana`,`disable edge pdf`,`disable telemetry/tasks`,`remove bloatware regkeys` and `install .NET 3.5`. This removes all of the bloatware and telemetry. You can do the other tweaks in the GUI aswell, but think before doing it. eg. don't uninstall onedrive if you use it.

## **Changing settings**

* After debloating, you can now go through all of the windows settings. (setings, control panel, file explorer settings, nvidia control panel, intel hd graphics ontrol panel, amd settings, etc.) Go through __all__ of them and cherrypick what you want on and what you don't. If you're unsure on what a certain setting does, do some research beforehand and determine if it's worth changing or not. Make sure to disable Xbox Game Bar though, it's an unnecessary annoyance.

    **For NVIDIA gpus, I recommend you [follow this tutorial.](https://www.youtube.com/watch?v=KWEPjoit1_E&t=183s)**
    
    **For Intel HD graphics, I recommend you [follow this tutorial.](https://www.youtube.com/watch?v=3VV9okffK9M&t=256s)**

    **For AMD gpus and integrated graphics, I recommend you [follow this tutorial](https://www.youtube.com/watch?v=eZaJ2WHJsTs)**

* Make sure to use the `high performance` power plan! To change it, go into windows search and type "control panel" then select "view by: large icons" in the top right corner, then click on "power options". You should [see this](https://imgur.com/a/y89c51r), then change the plan to "high performance" and you're done! It uses more power, but it gives better performance. (notably enabling turbo boost) If you don't see it by chance, click on "show additional plans" and it should show up.

If you're on a laptop and use the high performance power plan, don't unplug it. Running anything on battery life is misery and it would drain quickly anyway.

## **Disbaling unnecessary services & startup programs**

* Here's a list of services you can safely disable with no worry:
    **The Print Spooler**

    **Windows Image Acquisition**

    **Fax Services**

    **Windows Search**

    **Windows Error Reporting**

    **Windows Insider Service**

    **Remote Desktop**

    **Remote Registry**

    **Touch Keyboard and Handwriting Panel Service**

This list is from [this article](https://helpdeskgeek.com/windows-10/windows-10-unnecessary-services-you-can-disable-safely/), you can read up on what each one of these services does. 
After disabling the services, go to task manager and go to the "startup" tab. Disable everything in it. This will prevent 10,000 programs opening up when you boot up your PC! Then go to the windows settings, privacy, then navigate over to the "background apps" section. turn everything off.

## **Custom ISOs**

* If you're lazy to do any optimizations on your own, I'd recommend using a custom Windows 10 ISO such as `ggOS`, `AtlasOS` or`GhostSpectre Superlite`. These are *extremelly* stripped down versions of Windows. They include some tweaks which I haven't included, since they'd take a lot of time to do by hand. Out of all the 3, ggOS will provide the best fps/low latency at the cost of compatability and features, which you can read in [their discord server.](https://discord.gg/ggOS) 

**PS:** If you want to install a custom ISO or any OS, you will need a USB stick and a program to burn the ISO to the USB. I recommend [ventoy](https://www.ventoy.net/en/index.html) as it's the easiest.

## ⛏**2. Optimizing Minecraft**

After optimizing Windows, let's move onto the most important part of the tutorial; optimising the game itself.

## **Before getting into game optimization, make sure to close __everything__ when launching into the game, try to keep background processes minimal.**
