The beta version includes new features that we're working on. New beta versions are announced
in our [discord community](https://discord.com/invite/u9yhsFmEkB). 
There might still be some bugs in the version. If you find some, please report them to `#beta`
on discord.

# Joining
To join the beta program, switch to the beta chanel in the system settings:

![image](https://user-images.githubusercontent.com/5852422/201432828-3d777a81-8ce0-4303-aaac-1ebd5b277deb.png)

You can return to the stable version by unchecking the checkbox.

You must restart the application to switch between the beta version and the stable version. When you
are using the beta version, the version number at the top left of the web page will include `(beta)`.

# Leaving the beta program
You can return to the stable version by unchecking the beta-channel checkbox in the system settings.

If this is not possible (sometimes the beta version breaks and doesn't start any more), you can leave
the beta program by editing the configuration manually:
1. In your installation directory (e.g. `C:\stable-diffusion-ui`), there's a subdirectory `scripts`. 
    Navigate to this directory.
2. In this directory, edit the two files `config.json` and `config.bat` (`config.sh` if you're on Linux).
    Replace the word `beta` in both files by `main`.
3. Restart the Stable Diffusion UI application.
