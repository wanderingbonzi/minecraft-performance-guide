# Minecraft-performance-guide
A guide on how to fully optimize Minecraft: Java Edition to squeeze out every, and last frame per second.

**Q: Who is this meant for?**

**A:** I'm creating this for people with low end hardware, aka those who have troubles with running Minecraft at a playable, stable framerate.

**Q: Will these tweaks mentioned break my system?**

**A:** It depends. I've done most of these on my old, low end laptop and it didn't do too much harm. But since this is more organised, there's a smaller chance to break anything

**WARNING: If you end up breaking anything, I cannot be held accountable. I am just trying to help people.**

## 🧽**1. Optimizing Windows 10**

Windows 10 is, by default, very badly optimized. Things such as bloatware, background apps, services, search indexing, telemetry and much more will make your game and system lag. So let's get started!

## **BEFORE DOING ANY OF THESE TWEAKS, MAKE SURE YOU HAVE ALL THE LATEST UPDATES FROM MICROSOFT INSTALLED TO MINIMIZE ERRORS!**
## **Debloat**

* Debloating will remove all of the unnecesssary bloatware from Windows 10. Freeing up background processes, storage, and most importantly RAM. RAM (random access memory) is basically memory used to run the OS and programs. Windows 10 uses 1,5 - 2,5 gb whilst idle from my experience, which is very bad, especially for low end systems with 4gb of ram.

* For the purposes of this guide, we will be using [Sycnex's Windows 10 Debloater](https://github.com/Sycnex/Windows10Debloater). Download the debloater by clicking on the green "code" button and downloading it as a ZIP file. Once done, extract the contents to somewhere accessible, eg. desktop or documents. Find the file called Windows10DebloaterGUI.ps1 and right click on it and click "run with powershell".

[This is the GUI you will see.](https://i.imgur.com/JXOxWzq.png) Click on `remove all bloatware`, `disable cortana`,`disable edge pdf`,`disable telemetry/tasks`,`remove bloatware regkeys` and `install .NET 3.5`. This removes all of the bloatware and telemetry. You can do the other tweaks in the GUI aswell, but think before doing it. eg. don't uninstall onedrive if you use it.

## **Changing settings**

* After debloating, you can now go through all of the windows settings. (setings, control panel, file explorer settings, nvidia control panel, intel hd graphics ontrol panel, amd settings, etc.) Go through __all__ of them and cherrypick what you want on and what you don't. If you're unsure on what a certain setting does, do some research beforehand and determine if it's worth changing or not. Make sure to disable Xbox Game Bar though, it's an unnecessary annoyance.

**For NVIDIA gpus, I recommend you [follow this tutorial.](https://www.youtube.com/watch?v=KWEPjoit1_E&t=183s)**

**For Intel HD graphics, I recommend you [follow this tutorial.](https://www.youtube.com/watch?v=3VV9okffK9M&t=256s)**

**For AMD gpus and integrated graphics, I recommend you [follow this tutorial](https://www.youtube.com/watch?v=eZaJ2WHJsTs)**
