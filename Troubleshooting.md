Common issues and their solutions. If these solutions don't work, please feel free to ask at the [discord server](https://discord.com/invite/u9yhsFmEkB) or [file an issue](https://github.com/cmdr2/stable-diffusion-ui/issues).

## RuntimeError: CUDA out of memory
This can happen if your PC has less than 6GB of GPU RAM.

Try setting a lower "VRAM Usage Level" setting in the "Settings" tab.

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

## Could not load the Qt platform plugin "xcb"
In Linux, please run this before running start.sh: `export QT_QPA_PLATFORM=offscreen`

## ImportError: DLL load failed while importing cv2: The specified module could not be found.
If you're running Windows 10 N or Windows 10 KN (or any of its Pro, Education, ... variants), [the Microsoft Media Feature Pack](https://www.microsoft.com/en-us/software-download/mediafeaturepack) is needed to run Stable Diffusion.

## Killed uvicorn server:app --app-dir ... --port 9000 --host 0.0.0.0
This happens if your PC ran out of RAM. Stable Diffusion requires a lot of RAM, and requires atleast 10 GB of RAM to work well. You can also try closing all other applications before running Stable Diffusion UI.

## The revocation function was unable to check revocation because the revocation server was offline
A temporary workaround is to disable SSL checks. Run this in the developer console:
```
git config --global http.sslBackend schannel
git config --global http.sslVerify false
```
To re-enable SSL checks, run:
```
git config --global http.sslVerify true
```
Disabling SSL checks can enable attackers to inject malware into your downloads.

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
