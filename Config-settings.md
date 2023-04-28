# Installation time settings
## Network ports
During installation, the installer tries to start a web server on port `0.0.0.0:9000`. If this port is already in use, the startup will fail. You can change the port that the installer will use by creating a file `scripts/config.json` before starting EasyDiffusion:
```json
{
  "net": {
    "listen_port": 9000,
    "listen_to_network": true
  }
}
```

## Prevent browser start
If you're installing on a headless system, you might need to prevent the browser startup that normally occurs during installation. To do so, create a file `config.json` in the `scripts` folder with this content:
```
{"render_devices": "auto", "update_branch": "main", "ui": {"open_browser_on_start": false} }
```

# Runtime settings
The runtime settings are stored in the following files:
* `scripts/config.json`
* `scripts/user_config.sh`
* `scripts/user_config.bat`
The user_config files can be used to set environment variables for some of the AI runtimes, e.g. for ROCm settings.