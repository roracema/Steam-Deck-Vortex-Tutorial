
# Steam Deck Vortex Installation guide

This is a simple and straight forward solution to mod games using vortex, for this example I will be using Fallout new vegas (my most recent modded game)

# Pre-Requisites

1. Have unlocked your deck from read mode
2. Set a password
3. Have lutris installed

# Installation
1. Open lutris
2. Add a new program by clicking on the "+" on the top left corner next to the lutris icon
3. Click on "Install a Windows game from an executable"
4. Give a "Game Name" as you want, I will name it as "Vortex Mod Manager"
5. Click Install
6. Click Install again on the setup file
7. Check the "create application menu shortcut" and click continue.
(you could also add it to steam shorcut but I did not tested or tried)
8. "Select the setup file" search for the .exe file that you download from vortex page: https://www.nexusmods.com/about/vortex

9.  Click Install
10. Install vortex on the default folders as they suggest
11. Uncheck the "Run Vortex" once its installed and click finish
12. Close the current screen, dont Launch the application yet
13. On the applications list, select the "Vortex Mod Manager" and Click on the Wine glass button next to the "Play" button then click on "Winetricks"
14. Once the Winetricks open, select the "Select the default wineprefix"
15. select "Install a Windows DLL or component" then hit ok
16. select "dotnetdesktop6" (MS .NET Desktop Runtime 6.0 LTS) then hit ok
17. Open the Litrus and run the application once to check if everything is correct and you dont face any errors
18. Click on the game that you want and then click manage -> Select the folder that contains the game executable .exe
Example:
/home/deck/.steam/steam/steamapps/common/Fallout New Vegas/
19. A lot of errors should pop up, try to fix then as the mod manager suggest
20. Do the next steps to avoid any errors once the vortex files are created even though you are facing errors the next steps should fix it all

IMPORTANT: in order for the deployments to work you need to do the following:
Create a "mods" folder on the following:
/home/deck/.steam/steam/steamapps/compatdata/<APP_ID>/pfx/drive_c/users/steamuser/Application Data/

would be like this:
/home/deck/.steam/steam/steamapps/compatdata/<APP_ID>/pfx/drive_c/users/steamuser/Application Data/mods

Then you need to create a sys link from the new folder that you create to the following path:
/home/deck/Games/vortex-mod-manager/drive_c/users/steamuser/AppData/Local/falloutnv/

would be like this:
/home/deck/Games/vortex-mod-manager/drive_c/users/steamuser/AppData/Local/falloutnv/mods

21. As last step you should change the Mod Staging folder under -> Settings -> Mods (tab) -> set the path to the mods staging as the:
/home/deck/Games/vortex-mod-manager/drive_c/users/steamuser/AppData/Local/{GAME}/mods


NOTE: Considering that you are using falloutnv (Fallout New Vegas) update the references for each game you want


If you want to use the links from the vortex page to work with the new vortex installation dont forget to update the:
/home/deck/.config/mimeapps.list 

[Added Associations]
x-scheme-handler/nxm=net.lutris.vortex-mod-manager-1.desktop
x-scheme-handler/nxm-protocol=net.lutris.vortex-mod-manager-1.desktop

[Default Applications]
x-scheme-handler/nxm=net.lutris.vortex-mod-manager-1.desktop
x-scheme-handler/nxm-protocol=net.lutris.vortex-mod-manager-1.desktop
