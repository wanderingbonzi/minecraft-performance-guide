# 📈 Minecraft-performance-guide
A guide on how to fully optimize Minecraft: Java Edition to squeeze out every, and last frame per second! I'm creating this for people with low end hardware, aka those who have troubles with running Minecraft at a playable, stable framerate. I've been a low end player for a while and I know the pain, and I wanna help by bringing you the biggest optimization guide!

**Will these tweaks mentioned break my system, Bonzi?**

They shouldn't. I've done most of these on my old, low end laptop and it didn't do too much harm. But since this is more organised, there's a smaller chance to break anything

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

* Make sure to use the `high performance` power plan! To change it, go into windows search and type "control panel" then select `view by: large icons` in the top right corner, then click on `power options`. You should [see this](https://imgur.com/a/y89c51r), then change the plan to `high performance` and you're done! It uses more power, but it gives better performance. (notably enabling turbo boost) If you don't see it by chance, click on `show additional plans` and it should show up.

**If you're on a laptop and use the high performance power plan, don't unplug it. Running anything on battery life is misery and it would drain quickly anyway.**

* After changing the power plan, it's time to do some registry tweaks to further improve the performance. Press `windows + r` and type `regedit` in the run windows. Navigate over to `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile` and double click on `NetworkThrottlngIndex` and type FFFFFFFF and save the changes. (this tweak will heavily help if you have high ping) Then double click on `SystemRepsonsivness` and change the value to 0, this will make your system and game feel much smoother. After that, go to `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks\Games` and double click on `GPU Priority` and change the value to 8. Then double click on `priority` and change the value to 6. Make sure that `schedulingcategory` is set to high.

## **Change how Windows looks like**

* Windows 10 by default has a lot of heavy effects and animations, which can make the system feel slow. Firstly, go to the `settings` and then `personalization`, go to `colours` and switch `transparency effect` to off. After you do that, go to windows search and type `advanced system settings`. After clicking on it, go to `advanced settings` and click on `performance`. Copy [these settings.](https://imgur.com/a/AEe3tH0)

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
After disabling the services, go to task manager and go to the `startup" tab`. Disable everything in it. This will prevent 10,000 programs opening up when you boot up your PC! Then go to the windows settings, privacy, then navigate over to the `background apps` section. turn everything off.

## **Custom ISOs**

* If you're lazy to do any optimizations on your own, I'd recommend using a custom Windows 10 ISO such as `ggOS`, `AtlasOS` or`GhostSpectre Superlite`. These are *extremelly* stripped down versions of Windows. They include some tweaks which I haven't included, since they'd take a lot of time to do by hand. Out of all the 3, ggOS will provide the best fps/low latency at the cost of compatability and features, which you can read in [their discord server.](https://discord.gg/ggOS) 

**PS:** If you want to install a custom ISO or any OS, you will need a USB stick and a program to burn the ISO to the USB. I recommend [ventoy](https://www.ventoy.net/en/index.html) as it's the easiest.

## ⛏**2. Optimizing Minecraft**

After optimizing Windows, let's move onto the most important part of the tutorial; optimising the game itself.

## **Before getting into game optimization, make sure to close __everything__ when launching into the game, try to keep background processes minimal.**

## **JVM arguments & memory allocation.**
* Before even launching the game, we must optimize the JVM arguments and allocate enough RAM to the game. I recommend you allocate `2gb`, `4gb` at most. This is because Java Garbage Collection doesn't do a great job of dealing with a lot of RAM. (so don't allocate 16gb or half your memory to mc) JVM arguments will give a small boost in fps, which doesn't hurt to add.

I would recommend using this JVM argument on a low end system:
* `-Xms2G -Xmx2G -XX:+UnlockExperimentalVMOptions -XX:+UseLargePages -XX:+DisableExplicitGC -XX:G1MixedGCCountTarget=1`
If you wanna learn more about JVM arguments, [look here.](https://www.reddit.com/r/feedthebeast/comments/cjciv9/java_argumentsjvm_explaining_them_and_commonly/)

## **Performance Mods**
* Now it's time for the meat of the guide; the performance enhancing mods!
**All of the following mods will be using the [Fabric modloader](https://fabricmc.net/) due to it's supariorites over forge.**

* ✨**Performance mods (1.18.2)**

    [Fabric API](https://modrinth.com/mod/fabric-api) (Required)

    * Required for most Fabric Mods

    [Sodium](https://modrinth.com/mod/sodium) (Extremelly Recommended)

    * The most impactful mod; it replaces the vanilla engine with a modern opengl 4 engine, providing *very* big performance improvements
    
    [Lithium](https://modrinth.com/mod/lithium) (Extremelly Recommended)

    * Optimises game physics, mob AI, block ticking, etc. while preserving vanilla behaviour

    [Starlight](https://modrinth.com/mod/starlight) (Extremelly Recommended)
    
    * Rewrites the lighting engine, making it faster and better

    [LazyDFU](https://modrinth.com/mod/lazydfu) (Extremelly Recommended)

    * Makes the game boot faster and use less resources while booting

    [Ferritecore](https://modrinth.com/mod/ferrite-core) (Highly Recommended)

    * Reduces memory usage, very useful in heavily moded scenarios or intense areas
    
    [Dashloader](https://modrinth.com/mod/dashloader) (Moderately Recommended)

    * Makes the game load up much faster

    [Dynamic FPS](https://modrinth.com/mod/dynamic-fps) (Moderately Recommended)

    * Makes Minecraft take up less resources while tabbed out of it

    [Enhancted Block Entities](https://modrinth.com/mod/ebe) (Moderately Recommended)

    * Makes some of the blocks such as beds or chests render differently, providing a considerable boost in areas with tons of chests or beds
