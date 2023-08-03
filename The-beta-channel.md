The beta version includes new features that we're working on. New beta versions are announced
in our [discord community](https://discord.com/invite/u9yhsFmEkB). 
There might still be some bugs in the version. If you find some, please report them to `#beta`
on discord.

# Joining
To join the beta program, please follow these steps:
1. Open the `Settings` tab, at the top of the UI.

![image](https://user-images.githubusercontent.com/844287/227228217-c38e29cc-852c-4a94-91e4-392e9b067720.png)

2. Scroll to the bottom, and enable the `Beta Channel` setting.

![image](https://user-images.githubusercontent.com/844287/227228319-16f323ab-2b71-4497-93ef-e81168315b14.png)

3. Press the `Save` button, and restart the program. Please close the command prompt window (or terminal on Linux/Mac), and start Easy Diffusion again.

![image](https://user-images.githubusercontent.com/844287/227228576-45a9a3f8-80c6-4a37-9084-e11dcb934a61.png)

After you restart, you should see a `(beta)` label next to the version number, in the top-left corner of the UI. For e.g. 

![image](https://user-images.githubusercontent.com/844287/227228821-f361fb8f-8ff2-4174-9aad-33353a8a4af5.png)

# Test Diffusers in beta
The "Diffusers" version of beta is our new upcoming engine, and contains a lot of new features like LoRA, textual inversion embeddings, SD-XL, tiling etc.

![image](https://github.com/easydiffusion/easydiffusion/assets/844287/0a90b655-56db-4a32-82dd-41a0417a2704)


You can enable this by following these steps:
1. Enable "Beta channel" in the Settings tab of the UI.
2. Then make sure that `Use the new v2.6 engine (diffusers)` is `ON`.
3. Press `Save`.
4. Close Easy Diffusion by closing the black-and-white command prompt window (or terminal).
5. Restart Easy Diffusion. You'll now be in the diffusers version of Easy Diffusion.

# Leaving the beta program
You can return to the stable version by unchecking the beta-channel checkbox in the Settings tab.

If this is not possible (sometimes the beta version breaks and doesn't start any more), you can leave
the beta program by editing the configuration manually:
1. In your installation directory (e.g. `C:\EasyDiffusion`), there's a subdirectory `scripts`. 
    Navigate to this directory.
2. In this directory, edit the two files `config.json` and `config.bat` (`config.sh` if you're on Linux).
    Replace the word `beta` in both files by `main`.
3. Restart the Easy Diffusion application.