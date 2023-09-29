# Installation time settings
## Network ports
During installation, the installer tries to start a web server on port `0.0.0.0:9000`. If this port is already in use, the startup will fail. You can change the port that the installer will use by creating a file `config.yaml` in the EasyDiffusion directory before starting EasyDiffusion:
```yaml
net:
    listen_port: 9000
    listen_to_network: true
```
The `listen_to_network` setting configures whether to only listen on `localhost` (false) or on all interfaces (true). Please note that indentation is important and the space characters in front of `listen_port` and `listen_to_network` are required.

## Prevent browser start
If you're installing on a headless system, you might need to prevent the browser startup that normally occurs during installation. To do so, create a file `config.yaml` in the EasyDiffusion directory with this content:
```yaml
ui: 
    open_browser_on_start: false
```
Please note that indentation is important and the space characters in front of `open_browser_on_start` are required.

## Prevent users from changing the folder path to save images
This is useful if you're sharing Easy Diffusion over the network, and want to prevent users from changing the folder in which images will be saved.

To do so, please edit `config.yaml` and add the `force_save_path` entry:
```yaml
force_save_path: F:/path/to/save/in
```

You can also save metadata by default, by setting the `force_save_metadata` entry:
```yaml
force_save_metadata: json
```

`force_save_metadata` can take one of the following values: `json`, `txt`, `embed`, `embed,txt`, `embed,json`

# Runtime settings
The runtime settings are stored in the following files:
* `config.yaml`
* `scripts/user_config.sh`
* `scripts/user_config.bat`
The user_config files can be used to set environment variables for some of the AI runtimes, e.g. for ROCm settings.