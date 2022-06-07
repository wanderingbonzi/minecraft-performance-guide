# 📈 Minecraft-performance-guide
A guide on how to fully optimize Minecraft: Java Edition to squeeze out every, and last frame per second! I'm creating this for people with low end hardware, aka those who have troubles with running Minecraft at a playable, stable framerate. I've been a low end player for a while and I know the pain, and I wanna help by bringing you the biggest optimization guide!

🤔 **Will these tweaks mentioned break my system, Bonzi?**

They shouldn't. I've done most of these on my old, low end laptop and it didn't do too much harm. But since this is more organised, there's a smaller chance to break anything

## **WARNING: If you end up breaking anything, I cannot be held accountable. I am just trying to help people.**

## 🧽 **1. Optimizing Windows 10**

Windows 10 is, by default, very badly optimized. Things such as bloatware, background apps, services, search indexing, telemetry and much more will make your game and system lag. So let's get started!

## **BEFORE DOING ANY OF THESE TWEAKS, MAKE SURE YOU HAVE ALL THE LATEST WINDOWS UPDATES FROM MICROSOFT INSTALLED!**
## **Debloat**

* Debloating will remove all of the unnecesssary programs from Windows 10. Freeing up background processes, storage, and most importantly RAM. RAM (random access memory) is basically memory used to run the OS and programs. Windows 10 uses 1,5 - 2,5 gb whilst idle from my experience, which is very bad, especially for low end systems with 4gb of ram.

* For the purposes of this guide, we will be using [Sycnex's Windows 10 Debloater](https://github.com/Sycnex/Windows10Debloater). Download the debloater by clicking on the green "code" button and downloading it as a ZIP file. Once done, extract the contents to somewhere accessible, eg. desktop or documents. Find the file called ``Windows10DebloaterGUI.ps1`` and right click on it and click "run with powershell".

[This is the GUI you will see.](https://i.imgur.com/JXOxWzq.png) Click on `remove all bloatware`,`disable edge pdf`,`disable telemetry/tasks`,`remove bloatware regkeys` and `install .NET 3.5`. If it freezes, try to run it again and maybe try to restart windows. This removes all of the bloatware and telemetry. You can do the other tweaks in the GUI aswell, but think before doing it. eg. don't uninstall onedrive if you use it, don't disable cortana if you use her.

## **Side-Effects**

* If you experience any side-effects due to the debloater, I'll put possible solutions here. **If you experience a side-effect and have a fix for it, notify me or add it yourself!**

    [If your NVIDIA control panel broke as a side effect of the debloater, follow this tutorial.](https://www.drivereasy.com/knowledge/nvidia-control-panel-missing-solved/)

    [If a Microsoft App you used disappeared, follow this tutorial.](https://gearupwindows.com/how-to-reinstall-microsoft-store-and-other-preinstalled-apps-in-windows-10/)

## **Changing settings**

* After debloating, now go through all of the windows settings, (setings, control panel, file explorer settings, nvidia control panel,etc.) and cherrypick what you want on and what you don't. If you're unsure on what a certain setting does, do some research beforehand and determine if it's worth changing or not. Make sure to disable Xbox Game Bar though, it's an unnecessary annoyance.

    **For NVIDIA gpus, I recommend you [follow this tutorial.](https://www.youtube.com/watch?v=KWEPjoit1_E&t=183s)**
    
    **For Intel HD graphics, I recommend you [follow this tutorial.](https://www.youtube.com/watch?v=3VV9okffK9M&t=256s)**

    **For AMD gpus and integrated graphics, I recommend you [follow this tutorial](https://www.youtube.com/watch?v=eZaJ2WHJsTs)**

* Make sure to use the `high performance` power plan! To change it, go into windows search and type "control panel" then select `view by: large icons` in the top right corner, then click on `power options`. You should [see this](https://imgur.com/a/y89c51r), then change the plan to `high performance` and you're done! It uses more power, but it gives better performance. (notably enabling turbo boost) If you don't see it by chance, click on `show additional plans` and it should show up.

**If you're on a laptop and use the high performance power plan, don't unplug it. Running anything on battery life is misery and it would drain quickly anyway.**

* Registry tweaks can help out a bit, the following tweaks will regard network throttling and gpu priority. Press `windows + r` and type `regedit` in the run windows. Navigate over to `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile` and double click on `NetworkThrottlngIndex` and type FFFFFFFF and save the changes. (this tweak will heavily help if you have high ping) Then double click on `SystemRepsonsivness` and change the value to 0, this will make your system and game feel much smoother. After that, go to `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks\Games` and double click on `GPU Priority` and change the value to 8. Then double click on `priority` and change the value to 6. Make sure that `schedulingcategory` is set to high.

## **Change how Windows looks like**

* Windows 10 by default has a lot of heavy effects and animations, which can make the system feel slow. Firstly, go to the `settings` and then `personalization`, go to `colours` and switch `transparency effect` to off. After you do that, go to windows search and type `advanced system settings`. After clicking on it, go to `advanced settings` and click on `performance`. Copy [these settings.](https://imgur.com/a/AEe3tH0)

## **Disbaling unnecessary services & startup programs**

* To disable any of the services, go to windows search and type `services` and click on the top result. Here's a list of services you can safely disable with no worry:

    **The Print Spooler**

    **Windows Image Acquisition**

    **Fax Services**

    **Windows Search**

    **Windows Error Reporting**

    **Windows Insider Service**

    **Remote Desktop**

    **Remote Registry**

    **Touch Keyboard and Handwriting Panel Service**

This list is from [this article](https://helpdeskgeek.com/windows-10/windows-10-unnecessary-services-you-can-disable-safely/), you can read up on what each one of these services does. If you wanna disable even more services, search up what service(s) you wanna disable and decide if it's worth it or not.
After disabling the services, go to task manager and go to the `startup" tab`. Disable everything in it. This will prevent 10,000 programs opening up when you boot up your PC! Then go to the windows settings, privacy, then navigate over to the `background apps` section. turn everything off.

## **Programs**

* This isn't a required step, just some recommendations. If you have a low end pc, here are some programs and tweaks for said programs that I recommend:

    [Browser: Mozilla Firefox](https://www.mozilla.org/en-US/firefox/new/) & [Better-Fox](https://github.com/yokoffing/Better-Fox) to replace Chrome.

    [Discord: Openasar](https://openasar.dev/) to improve responsivness and smoothness.

    [Photo Editor: Paint.NET](https://www.dotpdn.com/downloads/pdn.html) as a simple photo editing solution.

    [Cleanmngr+](https://www.builtbybel.com/ms-apps/cleanmgrplus) to clean up unnecessary files.

    [Emsisoft - Emergency Kit Free](https://www.emsisoft.com/en/home/emergencykit/) as an antivirus that's portable.

    [Ventoy](https://www.ventoy.net/en/index.html) to boot from multiple ISOs.

    [Nvidia Profile Inspector](https://github.com/Orbmu2k/nvidiaProfileInspector/releases) manage and see hidden NVIDIA settings.

    [MSI Mode Utility](https://www.techpowerup.com/forums/attachments/msi_util_v3-exe.169994/) to manage device MSI modes and interrupt priorities.

    [MultiMC](https://multimc.org/) to manage multiple instances of Minecraft.

    [SKLauncher](https://skmedix.pl/sklauncher) as a cracked Minecraft launcher. (because tlauncher bad}

## **Custom ISOs**

* If you're lazy to do any optimizations on your own, or want even more performance, I'd recommend using a custom Windows 10 ISO. Custom ISOs such as `ggOS`, `AtlasOS` or`GhostSpectre Superlite`are *extremelly* stripped down versions of Windows. They remove A LOT more features for the grand prize of better fps and lower input latency. Out of all the 3, ggOS will provide the best fps/low latency at the cost of compatability and features, which you can read in [their discord server.](https://discord.gg/ggOS) 

* If you want to install a custom ISO or any OS, you will need a USB stick and a program to burn the ISO to the USB. I recommend [ventoy](https://www.ventoy.net/en/index.html) as it's the easiest. But [rufus](https://rufus.ie/en/) is also an option.

## ⛏ **2. Optimizing Minecraft**

After optimizing Windows, let's move onto the most important part of the tutorial; optimising the game itself.

## **Before getting into game optimization, make sure to close __everything__ when launching into the game, try to keep background programs minimal.**

## **JVM arguments & memory allocation**
* Before even launching the game, we must optimize the JVM arguments and allocate enough RAM to the game. I recommend you allocate `2gb`, `4gb` at most. This is because Java Garbage Collection doesn't do a great job of dealing with a lot of RAM. (so don't allocate 16gb or half your memory to mc) JVM arguments will give a small boost in fps, which doesn't hurt to add.

I would recommend using this JVM argument on a low end system:
* `-Xms2G -Xmx2G -XX:+UnlockExperimentalVMOptions -XX:+UseLargePages -XX:+DisableExplicitGC -XX:G1MixedGCCountTarget=1`
If you wanna learn more about JVM arguments, [look here.](https://www.reddit.com/r/feedthebeast/comments/cjciv9/java_argumentsjvm_explaining_them_and_commonly/)

* **After launching the game, open task manager and right click on `OpenJDK Platform Library` and click on `go to details`, right click on javaaw.exe and `set the priority to high`.** Also while playing the game, make sure that `hardware acceleration` is disabled in any open program you have. Hardware acceleration is supposed to make your apps smoother by utilizing the GPU for it. While Minecraft is CPU-bound (to 1 core and 1 thread), the GPU is also useful since it can take on some of the more demadning parts of the game, making the CPU use its full potencial!

## **Performance Mods**
* Now it's time for the meat of the guide; the performance enhancing mods!
**All of the following mods will be using the [Fabric modloader](https://fabricmc.net/) due to it's supariorites over forge.**

* ✨ **Performance mods (1.18.2 & above)**

    **[Fabric API](https://modrinth.com/mod/fabric-api) (REQUIRED)**

    * Required for most Fabric Mods.

    **[Sodium](https://modrinth.com/mod/sodium) (Extremely Recommended)**

    * Replaces the original vanilla engine with a more modern one, providing big improvements.
    
    **[Lithium](https://modrinth.com/mod/lithium) (Extremely Recommended)**

    * Optimises game physics, mob AI, block ticking, etc. while preserving vanilla behaviour.

    **[Starlight](https://modrinth.com/mod/starlight) (Extremely Recommended)**
    
    * Rewrites the lighting engine, making it faster and better especially with chunk loading.

    **[LazyDFU](https://modrinth.com/mod/lazydfu) (Extremely Recommended)**

    * Makes the game boot faster by skipping unnecessary work initializations.

    **[Ferritecore](https://modrinth.com/mod/ferrite-core) (Highly Recommended)**

     * Reduces memory usage, very useful in heavily moded scenarios or intense areas.

    **[C2ME](https://modrinth.com/mod/c2me-fabric) (Highly Recommended)**

    * Makes chunk loading faster, though it is very experimental.
    
    **[EntityCulling](https://modrinth.com/mod/entityculling) (Moderately Recommended)**

    * Doesn't render entities behind a wall or entities which can't be seen, very good for areas full of entities.

    **[Dashloader](https://modrinth.com/mod/dashloader) (Moderately Recommended)**

    * Makes the game load up much faster.

    **[Dynamic FPS](https://modrinth.com/mod/dynamic-fps) (Moderately Recommended)**

    * Makes Minecraft take up less resources while tabbed out of it.

    **[Enhancted Block Entities](https://modrinth.com/mod/ebe) (Moderately Recommended)**

    * Makes entities such as chests or beds use the baked block models, providing a considerable boost in areas with tons of chests or beds.

    **[Krypton](https://modrinth.com/mod/krypton) (Moderately Recommended)**

    * Attempts to optimize the Minecraft networking stack.

    **[Ksyxis](https://www.curseforge.com/minecraft/mc-mods/ksyxis) (Moderately Recommended**

    * Speeds up world loading times by skipping unnecessary procedures.

    **[Cull Leaves](https://modrinth.com/mod/cull-leaves) (Lowly Recommended)**

    * Adds culling to leaves, similar to Optifines "smart leaves" option.

    **[BiomeThreadLocalFix](https://github.com/RedLime/BiomeThreadLocalFix/releases) (Lowly Recommended)**

    * Fixes the BiomeThreadLocalFix memory leak.

    **[Better Sodium Video Settings](https://www.curseforge.com/minecraft/mc-mods/better-sodium-video-settings-button) (Bonus)**

    * Restores the default vanilla settings menu while leaving a button for accessing sodium video settings, **this is required for changing the resolution.**

* And those are all the perfomance mods for 1.18.2! I've only provided basic info about them, but you can look into them further if you want to! If you wish to install any of them, firstly download [the Fabric Modloader](https://fabricmc.net/) and [Fabric API](https://modrinth.com/mod/fabric-api). Place the Fabric API mod in your mod folder (the mods folder is usually in the `C:\Users\<insertnamehere>\AppData\Roaming\.minecraft\mods` file path.), then download the mods you want to try out and place them in the mod folder aswell!

## **Why are you not recommending Optifine?!?**

* I've been a Optifine user myself, but I ended up switching over and making a small Fabric modpack which has all of the features I need. **Optifine stopped being an actual optimization mod.** The developer refuses to rewrite the decade old code, and even worse; It's closed source. Which means that no one can view the source code. Now with open source projects, anyone can view and edit the code, and some people might even end up __improving__ it. Not to mention that it also breaks mods, wonder why Optifine isn't in large modpacks? Exactly.

* Features such as shaders, zoom and custom entity models have fabric equivalents, aka [Iris](https://modrinth.com/mod/iris), [Logical Zoom](https://modrinth.com/mod/logical-zoom) and [CIT Resewn](https://modrinth.com/mod/cit-resewn).

## **Optifine *may* work better on some hardware due to Sodium's usage of newer OpenGL versions. If Optifine works better for you, then by all means use it.**

## **Game Settings**

* Now when you're in-game, let's get into what video settings to use. [These](https://imgur.com/a/0CrOTdp) settings are what I recommend for low end systems. Make sure to lower your resolution aswell! Setting it to 900p or 720p will give a considerable boost since it is displaying less pixels. (use [Better Sodium Settings](https://www.curseforge.com/minecraft/mc-mods/better-sodium-video-settings-button) or [Sodium Extras](https://www.curseforge.com/minecraft/mc-mods/sodium-extra))

* If you don't want to use these settings, turn everything to the lowest and then start testing out what settings work best for you. Ex, If your pc can handle more chunks, increase the render distance, if it can handle higher video settings, try turning them up. Rinse and repeat.
