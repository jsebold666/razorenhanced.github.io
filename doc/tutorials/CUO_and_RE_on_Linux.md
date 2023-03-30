# CUO and RE on Linux

Just create a new `WINEPREFIX` exclusively for RE setup.
At least thats what I did here.

* I create a new 64-bit `WINEPREFIX` simply by running winetricks and specifying the new prefix, like this:
  ```WINEPREFIX=/home/<your-username>/wine/cuo winetricks```
  This will create a new `WINEPREFIX` inside `<your-user-home-folder>/wine/cuo`.
  You can just close winetricks once it opens.

* Then run everything specifying that `WINEPREFIX` on every command as an env var, including RE setup and when running CUO
  Like this:

```sh
WINEPREFIX=/home/$USER/wine/cuo wine razorenhanced-setup.exe
```

* And this is the script I use to run RE Launcher:

```sh
#!/bin/bash
cd "/home/$USER/uo/razor-enhanced/"
WINEPREFIX=/home/$USER/wine/cuo wine RazorEnhanced.exe
```

* As you see, I first cd into the folder I put RE executable in (it doesn't have to be inside the `WINEPREFIX` folder), then I run RE executable with wine while specifying the new prefix we created for it.

* Save that bash script, then run `chmod +x` on it:

```bash
chmod +x name-of-the-script.sh
```

* After that run the bash script and RE should open.
