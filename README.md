# Garrys-Mod-C_Hand-Scripts
All the scripts I made for converting various game rigs to Valve's ValveBiped rig, used in Source games, specifically for Garry's Mod

Instructions on how to use these:
- [Download the scripts I created from my releases page here](https://github.com/KoukoCocoa/Garrys-Mod-C_Hand-Scripts/releases)
- [Install Crowbar from the Steam Group page here](https://steamcommunity.com/groups/CrowbarTool)
- [Install Blender here](https://www.blender.org/download/)
- [Install Blender Source Tools here](http://steamreview.org/BlenderSourceTools/)
- Download Crowbar and extract it's contents to a location you can access
- Download a Source Game (I.e.: Garry's Mod, Counter Strike: Global Offensive, etc.) and find a model you want to convert by going to the games local files

**For Garry's Mod ONLY (You can extract the model you want to convert by extracting the .GMA file for the addon you want and looking in the /models/ folder, by programs like [my tool seen here](https://github.com/KoukoCocoa/Garrys-Mod-Workshop-Utility/releases)**

- Once you have the .mdl you want to decompile, open up Crowbar and go to the "Decompile" tab
- Locate the .mdl you want to decompile then click "Decompile" (I also recommend turning on "Group into QCI Files" and setting Output to "Subfolder of MDL input" as it's easier to edit/view what you need)
- Locate the decompiled contents and look at the (name_)bone.qci file that is in there, make sure that the bone structure (naming, etc.) is **EXACTLY** the same as the script that is required for it (I did try my best to name them as accurately as possible) and put it inside the decompiled contents folder
- Load up Blender and install the Blender Source Tools plugin, then import the .SMD file that contains both the gun **AND** the arm mesh 
- Remove the arm mesh by deleting the vertices using Blender's Edit Mode (While keeping the gun and the rig intact)
- Re-export the .SMD to the same area where you decompiled the .MDL
- Edit the (name).qc file that is in the decompiled folder, move the $include "(name_)bone.qci" above the $modelname, and rename it to the new script name
- If you renamed the model .SMD file, rename that part in the $model or "studio" area (if using Bodygroups)
- Go to Crowbar's "Compile" tab and find the .qc file you just edited

**Make sure you have installed the SDK for the game you want to use, Counter Strike's SDK Tools is in the Steam Tools area, I recommend using Counter Strike over Garry's Mod for compiling**

- Compile the new model and test it in game, enjoy!
