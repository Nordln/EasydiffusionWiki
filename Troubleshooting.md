Common issues and their solutions. If these solutions don't work, please feel free to ask at the [discord server](https://discord.com/invite/u9yhsFmEkB) or [file an issue](https://github.com/cmdr2/stable-diffusion-ui/issues).

## RuntimeError: CUDA out of memory
This can happen if your PC has less than 6GB of GPU RAM.

Try disabling the "Turbo mode" setting under "Advanced Settings", since that takes an additional 1 GB of VRAM (to increase the speed).

Additionally, a common reason for this error is that you're using an initial image larger than 768x768 pixels. Try using a smaller initial image.

Also try generating smaller sized images.

## urllib.error.URLError: <urlopen error [Errno 11001] getaddrinfo failed>
This can be due to a Firewall/Antivirus/Proxy/VPN blocking your network connections. Please check those.

Another solution is to switch to Google's DNS server: https://developers.google.com/speed/public-dns/docs/using#windows or Cloudflare's DNS server: https://developers.cloudflare.com/1.1.1.1/setup/windows/

## RuntimeError: Error(s) in loading state_dict fo UNet: size mismatch for model1.diffusion_model.input_blocks.0.0.weight: copying a param with shape torch.Size([320, 9, 3, 3]) from checkpoint, ....
This usually happens when you try to use the v1.5 inpainting model. Unfortunately, it is not compatible with this version of Stable Diffusion.

## 'conda-unpack' is not recognized as an internal or external command
Please try copying the `stable-diffusion-ui` folder inside the zip file and paste that in `C:` (or any other drive). Don't extract the zip file, instead try copying the folder from inside it and paste it in the target drive.

## ImportError libSM.so.6 cannot open shared object file No such file or directory
Please run `apt install libsm6 libxext6 libxrender-dev -y` (you may need to put `sudo` before this)

And try again.

## basicsr module not found
For Windows: Please download and extract basicsr from [here](https://github.com/cmdr2/stable-diffusion-ui/releases/download/v2.16/basicsr-win64.zip), and place the `basicsr` folder inside the `stable-diffusion-ui\stable-diffusion\env\lib\site-packages` folder. Then run the `Start Stable Diffusion UI.cmd` file again.

For Linux: Please contact on the [discord server](https://discord.com/invite/u9yhsFmEkB).

## ClobberError: This transaction has incompatible packages due to a shared path
Please try creating a folder named "profile" inside the "stable-diffusion-ui" folder, and retry the installation.

If that doesn't work - On Windows, please ensure that you had placed the `stable-diffusion-ui` folder after unzipping to the root of C: or D: (or any drive). For e.g. `C:\stable-diffusion-ui`. **Note:** This has to be done **before** you start the installation process. If you have already installed (and are facing this error), please delete the installed folder, and start fresh by unzipping and placing the folder at the top of your drive.

This error can also be caused if you already have conda/miniconda/anaconda installed, due to package conflicts. Please open your Anaconda Prompt, and run `conda clean --all` to clean up unused packages.

If nothing works, this could be due to a corrupted installation. Please try reinstalling this, by deleting the installed folder, and unzipping from the downloaded zip file.

## ImportError: DLL load failed while importing cv2: The specified module could not be found.
If you're running Windows 10 N or Windows 10 KN (or any of its Pro, Education, ... variants), [the Microsoft Media Feature Pack](https://www.microsoft.com/en-us/software-download/mediafeaturepack) is needed to run Stable Diffusion.

## Killed uvicorn server:app --app-dir ... --port 9000 --host 0.0.0.0
This happens if your PC ran out of RAM. Stable Diffusion requires a lot of RAM, and requires atleast 10 GB of RAM to work well. You can also try closing all other applications before running Stable Diffusion UI.

## Green image generated
This usually happens if you're running NVIDIA 1650 or 1660 Super. To solve this, please close and run the Stable Diffusion command on your computer. If you're using the older Docker-based solution (v1), please upgrade to v2: https://github.com/cmdr2/stable-diffusion-ui/tree/v2#installation

If you're still seeing this error, please try enabling "Full Precision" under "Advanced Settings" in the Stable Diffusion UI.

## RuntimeError: Found no NVIDIA driver on your system:
If you have an NVIDIA GPU and the latest [NVIDIA driver](http://www.nvidia.com/Download/index.aspx), please ensure that you've installed [nvidia-container-toolkit](https://stackoverflow.com/a/58432877). (Thanks [u/exintrovert420](https://www.reddit.com/user/exintrovert420/))

## RuntimeError: CUDA error: unknown error
Please ensure that you have an NVIDIA GPU and the latest [NVIDIA driver](http://www.nvidia.com/Download/index.aspx), and that you've installed [nvidia-container-toolkit](https://stackoverflow.com/a/58432877).

Also, if you are using WSL (Windows), please ensure you have the latest WSL kernel by running `wsl --shutdown` and then `wsl --update`. (Thanks [AndrWeisR](https://github.com/AndrWeisR))

## ModuleNotFoundError: No module named 'gfpgan'
If you have moved your installation to a different folder or drive, please follow these steps *exactly*:
1. Open in `notepad` the `stable-diffusion-ui\stable-diffusion\env\Lib\site-packages\easy-install.pth`
2. Change the paths from the old path to the new path. For e.g. if your previous folder was `C:\stable-diffusion-ui`, and the new location is `E:\ai\stable-diffusion-ui`, then change the paths to (**change the path to where your new folder is**):
```
E:\ai\stable-diffusion-ui\stable-diffusion\src\taming-transformers
E:\ai\stable-diffusion-ui\stable-diffusion\src\clip
E:\ai\stable-diffusion-ui\stable-diffusion\src\realesrgan
E:\ai\stable-diffusion-ui\stable-diffusion\src\gfpgan
```
3. Save this file, and try running the project again. The same approach should work for Linux as well.

# For support queries
## Entering a conda environment in an existing installation
This will give you an activated conda environment in the terminal, so you can run commands and force-install any packages, if required.

Users don't need to have the Anaconda Prompt installed to do this anymore, since the installer bundles a portable version of conda inside it. Just follow these steps.

**Windows:**
1. Run the `Developer Console.cmd` file (inside the project folder) by double-clicking it.
2. Type `python --version` and press enter. You should see 3.8.5.

**Linux:**
1. Open the terminal
2. Type `cd /path/to/stable-diffusion-ui` and press enter
3. Type `./developer_console.sh` and press enter
4. Type `python --version` and press enter. You should see 3.8.5.

This will give you an activated conda environment. You can now run conda or pip commands to install or change packages.
