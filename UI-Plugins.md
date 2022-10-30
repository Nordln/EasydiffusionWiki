## User interface plugins
Using user interface plugins, additional functionality can be added to the user interface of Stable Diffusion UI.

**Note:** Plugins have not been reviewed for malicious code. Please only use plugins that you trust.

## Installing plugins
If not stated otherwise in the plugin description, right click on the plugin link and save the plugin to `C:\stable-diffusion-ui\plugins\ui` (Or the drive that you've installed to, respectively). The file name must have the suffix `.plugin.js`.

### Post processing plugins
- **[Mad's Render Tasks](https://raw.githubusercontent.com/madrang/sd-ui-plugins/master/mads-render_tasks.plugin.js) by [Marc-Andre Ferland](https://github.com/madrang)**

    Adds the old Resize, but now with a UI for it and an option to keep only the last N tasks. 
    _[Github Repo](https://github.com/madrang/sd-ui-plugins)_

- **[Scaleup](https://www.computingbits.com/software/scaleup.plugin.js) by Avidgamefan#4035**

    Modest scaling up, maintaining close ratio, with img2img to increase resolution of output while adding minor details.
    Maximum output is 1536 along one axis, but generally, things are kept at 1024x1024 and below.  One-click workflow!

### Information plugins
- **[Copy Settings (JSON)](https://raw.githubusercontent.com/JeLuF/stable-diffusion-ui-plugins/main/copy-settings-json.plugin.js) by [JeLuF](https://github.com/JeLuF)**

    Copy the settings used to create the image as machine readable JSON string to the clipboard. 
    _[Github Repo](https://github.com/JeLuF/stable-diffusion-ui-plugins/)_

- **[Copy Settings (TXT)](https://raw.githubusercontent.com/JeLuF/stable-diffusion-ui-plugins/main/copy-settings-txt.plugin.js) by [JeLuF](https://github.com/JeLuF)**

    Copy the settings used to create the image as human readable text string to the clipboard.
    _[Github Repo](https://github.com/JeLuF/stable-diffusion-ui-plugins/)_

### Third party site integration
The Stable Diffusion UI project is not partnered with any of the services mentioned below.

- **[Open in Photopea](https://raw.githubusercontent.com/JeLuF/stable-diffusion-ui-plugins/main/photopea.plugin.js) by [JeLuF](https://github.com/JeLuF)**

    Open the image in [Photopea](https://www.photopea.com/), a commercial web service that can be used to edit photos. 