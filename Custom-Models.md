## What are Stable Diffusion models?
Stable Diffusion UI uses so called models to create the images. The models get trained using many images and image descriptions. During the installation,
a default model gets downloaded, the sd-v1-4 model. Other models exist. Some of them use sd-v1-4 as their base and were then trained on additional images, while other models were trained from scratch.

Depending on the images used during the training, the models generate a different look and understand different prompts.

## Installing a model
If you've downloaded a model, you can make it available to Stable Diffusion UI:
- Copy the model file to `C:\stable-diffusion-ui\models\stable-diffusion`. The file should have the suffix `.ckpt` or `.safetensors`.
- Reload your browser page. The model should be listed in the "Models" section in the image settings:

    ![image](https://user-images.githubusercontent.com/5852422/197419759-45cba5a7-58ef-4fff-a6b2-80536d7f609e.png)

## Stable Diffusion v2 models
Stable Diffusion v2 models are currently only supported in the beta version of the Stable Diffusion UI, with some restrictions. *After* joining our [discord server](https://discord.com/invite/u9yhsFmEkB), you can take a look at this [post](https://discord.com/channels/1014774730907209781/1023840914667483166/1046703577126678608) for details on how to enable the SD2 support.

## Web resources
**Note:** These links lead to websites outside of the Stable Diffusion UI project.

**Note:** Stable Diffusion models can contain malware. ALWAYS SCAN FOR VIRUSES.

- https://civitai.com/?types=Checkpoint - Overview of many stable diffusion models. Only models of the type _checkpoint_ can be used by Stable Diffusion UI.
- https://rentry.org/sdmodels - List of stable diffusion models from various sources