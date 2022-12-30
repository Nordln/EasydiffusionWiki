# Installation time settings
## Network ports
During installation, the installer tries to start a web server on port `0.0.0.0:9000`. If this port is already in use, the startup will fail. You can change the port that the installer will use:
### Linux
Start the installer using `SD_UI_BIND_PORT=1234 ./start.sh` (Replace 1234 with the port number you want to use). If you also want to limit the web server to only listen to `localhost`, you can use `SD_UI_BIND_PORT=1234 SD_UI_BIND_IP=127.0.0.1 ./start.sh`

Once the application is running, go to the "Settings" tab in the web interface and click "Save" to persist these settings. You can now use `./start.sh` to start the application and don't need to provide the config settings any more for each startup.

### Windows
First, open a `cmd` window, in which you run the following commands (replace `X` by the drive letter of your installation drive):
```
cd /d X:\stable-diffusion-ui
set SD_UI_BIND_PORT=1234
"Start Stable Diffusion UI.cmd"
```
If you also want to limit the web server to only listen to `localhost`, you can use:
```
cd /d X:\stable-diffusion-ui
set SD_UI_BIND_PORT=1234
set SD_UI_BIND_IP=127.0.0.1
"Start Stable Diffusion UI.cmd"
```

Once the application is running, go to the "Settings" tab in the web interface and click "Save" to persist these settings. You can now use `"Start Stable Diffusion UI.cmd"` to start the application and don't need to provide the config settings any more for each startup.

# Runtime settings
The runtime settings are stored in the following files:
* `scripts/config.json`
* `scripts/config.bat` (Windows) 
* `scripts/config.sh` (Linux)
The `.bat` and `.sh` files contain settings required for the startup of the application. The `.json` file has settings needed at runtime.