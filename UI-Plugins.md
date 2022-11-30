## User interface plugins
Using user interface plugins, additional functionality can be added to the user interface of Stable Diffusion UI.

**Note:** Plugins have not been reviewed for malicious code. Please only use plugins that you trust.

## Installing plugins
If not stated otherwise in the plugin description, right click on the plugin link and save the plugin to `C:\stable-diffusion-ui\plugins\ui` (Or the drive that you've installed to, respectively). The file name must have the suffix `.plugin.js`.

### Post processing plugins
- **[Mad's Render Tasks](https://raw.githubusercontent.com/madrang/sd-ui-plugins/master/mads-render_tasks.plugin.js) by [Marc-Andre Ferland](https://github.com/madrang)**

    Adds a Resize option with a UI to select the output resolution, change the prompt, guidance scale, etc...
    A Redo button to retry quickly with a new seed.
    And an option to keep only the last N tasks.
    _[Github Repo](https://github.com/madrang/sd-ui-plugins)_

- **[Scaleup](https://www.computingbits.com/software/scaleup.plugin.js) by Avidgamefan#4035**

    Modest scaling up, maintaining close ratio, with img2img to increase resolution of output while adding minor details.
    Maximum output is 1536 along one axis, but generally, things are kept at 1024x1024 and below.  One-click workflow!

- **[Scaleup(preserve)](https://www.computingbits.com/software/scaleuppreserve.plugin.js) by Avidgamefan#4035**

    Same as above, but with a low Prompt Strength, to preserve more details.

- **[ScaleupMAX](https://www.computingbits.com/software/scaleupMAX.plugin.js) by Avidgamefan#4035**

    Scales up to the largest resolution your card can handle, with one click. This requires you to test to determine your highest, maximum resolution, and set it inside the script.  Currently defaulted to safe settings for the Nvidia 2060 Super with 8GB VRAM.

- **[Draw Another X Steps](https://andrewjnuttall.com/stable-ui/plugins/render_more_steps.plugin.js) by [Andrew Nuttall]**

    Give options to draw X additional steps where X is a list of steps defined in the file. Default is 50, 100, 150, 200 and as such will give the options "Draw Another 50 Steps", "Draw Another 100 Steps", etc. To modify open in a text editor and change the stepList to include desired step options.

### General UI changes
- **[History](https://raw.githubusercontent.com/rbertus2000/sd-ui-plugins/main/history.plugin.js) by [rbertus2000](https://github.com/rbertus2000)**

    Adds a new column to keep a history of all prompts/settings that were used in this session.
    _[Github Repo](https://github.com/rbertus2000/sd-ui-plugins)_

- **[More resolutions](https://raw.githubusercontent.com/superskirv/stable-diffusion-ui-plugins/main/Ski-SDUI-MoreRes.plugin.js) by [Super.Skirv](https://github.com/superskirv) and [JeLuF](https://github.com/JeLuF)**

    Adds all resolutions from 128 to 2048 in steps of 64 to the width and height dropdowns.
    _[Github Repo](https://github.com/JeLuF/stable-diffusion-ui-plugins/)_

- **[Don't leave](https://raw.githubusercontent.com/JeLuF/stable-diffusion-ui-plugins/main/Don-t-leave.plugin.js) by [JeLuF](https://github.com/JeLuF)**

    Warn the user before leaving/reloading/closing the Stable Diffusion tab. Unsaved images might get lost when the tab is being closed.
    The current version of the plugin does not check for changes - the warning will always be shown.
    _[Github Repo](https://github.com/JeLuF/stable-diffusion-ui-plugins/)_

- **[DateFolders](https://raw.githubusercontent.com/JeLuF/stable-diffusion-ui-plugins/main/DateFolders.plugin.js) by [JeLuF](https://github.com/JeLuF)**

    Changes how autosave's session folders are named. The folders will have names like _2022_11_05T18_58_05_757Z_ instead of _1667674597680_.
    _[Github Repo](https://github.com/JeLuF/stable-diffusion-ui-plugins/)_

### Information plugins
- **[Copy Settings (JSON)](https://raw.githubusercontent.com/JeLuF/stable-diffusion-ui-plugins/main/copy-settings-json.plugin.js) by [JeLuF](https://github.com/JeLuF)**

    Copy the settings used to create the image as machine readable JSON string to the clipboard. 
    _[Github Repo](https://github.com/JeLuF/stable-diffusion-ui-plugins/)_

- **[Copy Settings (TXT)](https://raw.githubusercontent.com/JeLuF/stable-diffusion-ui-plugins/main/copy-settings-txt.plugin.js) by [JeLuF](https://github.com/JeLuF)**

    Copy the settings used to create the image as human readable text string to the clipboard.
    _[Github Repo](https://github.com/JeLuF/stable-diffusion-ui-plugins/)_

### Third party site integration plugins
The Stable Diffusion UI project is not partnered with any of the services mentioned below.

- **[Open in Photopea](https://raw.githubusercontent.com/JeLuF/stable-diffusion-ui-plugins/main/photopea.plugin.js) by [JeLuF](https://github.com/JeLuF)**

    Open the image in [Photopea](https://www.photopea.com/), a commercial web service that can be used to edit photos.
    _[Github Repo](https://github.com/JeLuF/stable-diffusion-ui-plugins/)_

### Prompt related plugins

- **[Surprise Me!](https://raw.githubusercontent.com/madrang/sd-ui-plugins/master/mads-surprise_me.plugin.js) by [Marc-Andre Ferland](https://github.com/madrang)**

    _Surprise me!_ adds a button that generates a random prompt. You need to download these three files and put them into the `plugins\ui` folder:

    1.  [Surprise Me! Plugin](https://raw.githubusercontent.com/madrang/sd-ui-plugins/master/mads-surprise_me.plugin.js)
    2.  [rita.js](https://raw.githubusercontent.com/madrang/sd-ui-plugins/master/rita.js)
    3.  [rita_grammar.json](https://raw.githubusercontent.com/madrang/sd-ui-plugins/master/rita_grammar.json)

    _[Github Repo](https://github.com/madrang/sd-ui-plugins)_

- **[Spell tokenizer](https://raw.githubusercontent.com/Sidem/sd-ui-plugins/main/spell-tokenizer.plugin.js) by [Sidem](https://github.com/Sidem)**

    Script to help with spell (prompt) building.
    Create individual spell tokens to rearrange and modulate by using commas.
    Drag and drop tokens to rearrange order.
    Hold ALT+scroll over a token to emphasize or de-emphasize.
    Right click to delete a token.
    _[Github Repo](https://github.com/Sidem/sd-ui-plugins)_

- **[Tag autocomplete](https://gist.githubusercontent.com/nedius/bd5a1af78dc71a762fe76bd6d05631d5/raw/97ce564d585582876fa163392b8246732fb5c597/nedius.tagcomplete.plugin.js) by [nedius](https://github.com/nedius)**

  Tag autocomplete for prompts using booru style tags. _[Gist](https://gist.github.com/nedius/bd5a1af78dc71a762fe76bd6d05631d5)_