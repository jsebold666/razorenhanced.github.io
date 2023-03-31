# CUO and RE with Wine-staging #

## Credits

- tau#7508    
- Zaos Xyrdan#1074
- Ecte#6799

## Instructions

1. Install wine staging branch, guide here -> [Wine Wiki](https://wiki.winehq.org/Download)

2. Follow this guide
[(Discord Link)](https://discord.com/channels/292282788311203841/866766902839869480/958734508381855786)
for creating a wineprefix

3. OK now we have a clean wineprefix folder. (don't agree with automatically installing mono, but it doesn't really matter)
    * Use your "`WINEPREFIX=`" folder for *everything* you run with `wine`, `winetricks`, `winecfg` ...  
I will not mention this again.  
(Doesn't really matter, but this way you will have wineprefix just for running Ultima, without wineprefix it defaults to your home/.wine/ , you can nuke this by accident really easy.)

4. Run winecfg, and set default environment to windows 10.

5. Run `winetricks` install dll module -> to install .NET 4.8

6. First make sure standalone CUO client can run through CUO launcher.
    * This could be probably HW dependent -
I'm running on laptop with integrated INTEL graphics.  
        * Run `wine ClassicUOlauncher`
        * go to settings for your profiles
        * and change graphics driver to OpenGL.
    * When you launch CUO through CUOlauncher, it should work.
    * Exit.

Now we make sure standalone RazorEnhanced can run:

1. Unzip it somewhere.
2. Go to RazorEnhanced folder.
3. Try run it with `wine RazorEnhanced.exe`
4. If you get a "LDAP something" error,
fix this by
    * running `wine regedit`
    * Add key "Drives" into path `HKLM/Software/Wine/`
5. Fill clients paths into razor.
    * Try launching it with Client button (it should launch RazorEnh with osi client)
    * Try launching it with CUO button, it should launch CUOclient with RazorEnh.
    * Launching through ClassicUOLauncher.exe works for me too, I've added plugin with "add from .zip", from file `RazorEnhanced**.zip`.
