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