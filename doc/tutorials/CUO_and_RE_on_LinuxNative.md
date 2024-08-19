# CUO and RE native

## Instructions

1. Prerequisite packages that need to exist before RE can run on linux
   * libZ - used for unpacking data sent from server
   * mono-complete - used for windows gui libraries
   * Thats all I remember, add more as we try

2. Download/Install CUO
   1. https://www.classicuo.eu/
   2. cd ~/Downloads
   3. unzip it into a directory, for this example we'll use CUO on the Desktop    (e.g. unzip -o -d ~/Desktop/CUO/  ClassicUOLauncher-linux-x64-release.zip )
   4. Run their launcher, you dont have to always use it, but it pulls down all their code

3. Download RazorEnhanced
   1. Go to Razorenhanced web site and Download the latest package
   2a. Use web browser 
   2b. (optional cli) wget -c https://github.com/RazorEnhanced/RazorEnhanced/releases/download/v0.8.2.185/RazorEnhanced-0.8.2.185.zip 

4. Using the CUO launcher set up a profile for your server
   1. Click the little gear at bottom and fill in server port etc. information
   2. click on plugins tab and add the RazorEnhanced zip file you downloaded earlier in step 3
   3. You'll see it appear in the selection, click its select box
   4. save profile
   5. Play -- but I cant test because ClassicUO launcher cant update :( 


Optional thoughts. 
   I don't like having the plugin burried inside the Classic UO folder, because all your scripts etc. end up in there, and I use the same stuff on many servers. So what I did was I didn't add the zip in 4.2, but instead went into the cli, and in the folder ~/Desktop/CUO/ClassicUO/Data/Plugins/ I created a sym link to a RazorEnhanced folder thats on my desktop. 
   1. unzip the RazorEnhanced file into a folder, for this example we'll use ~/Desktop/RazorEnhanced.  Do one of these 2:
      1a. Use File Explorer (Dolphin or whatever) to open the zip file and drag all its contents to a folder named RazorEnhanced on your desktop
	  1b. unzip -o -d ~/Desktop/RazorEnhanced  ./RazorEnhanced-0.8.2.185.zip
   2. cd to ~/Desktop/CUO/ClassicUO/Data/Plugins
   3. ln -s ~/Desktop/RazorEnhanced ./
   
   Now in the launcher profile you'll see an option for RazorEnhanced, but its the sym link and you can manage all your RE stuff in the ~/Desktop/RazorEnhanced folder
   


