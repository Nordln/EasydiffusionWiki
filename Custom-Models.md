## What are Stable Diffusion models?
Stable Diffusion UI uses so called models to create the images. The models get trained using many images and image descriptions. During the installation,
a default model gets downloaded, the sd-v1-4 model. Other models exist. Some of them use sd-v1-4 as their base and were then trained on additional images, while other models were trained from scratch.

Depending on the images used during the training, the models generate a different look and understand different prompts.

## Installing a model
If you've downloaded a model, you can make it available to Stable Diffusion UI:
- Copy the model file to `C:\stable-diffusion-ui\models\stable-diffusion`. The file should have the suffix `.ckpt` or `.safetensors`.
- If the model comes with a `.yaml` file, please place that yaml file next to the model, with the same name. For e.g. if the model is `some-model.ckpt` (or `some-model.safetensors`), the yaml file should be `some-model.yaml`, placed next to it in the same folder.
- Reload your browser page. The model should be listed in the "Models" section in the image settings:

    ![image](https://user-images.githubusercontent.com/5852422/197419759-45cba5a7-58ef-4fff-a6b2-80536d7f609e.png)

**Troubleshooting - If you see black images**, please add this to the **end** of the `.yaml` file that came with your model:
```yaml
extra:
  attn_precision: "fp32"
```

For e.g. please see the end of this file for reference: https://github.com/easydiffusion/sdkit/blob/main/sdkit/models/models_db/configs/v2.1-inference-v.yaml

## Web resources
**Note:** These links lead to websites outside of the Stable Diffusion UI project.

**Note:** Stable Diffusion models can contain malware. ALWAYS SCAN FOR VIRUSES.

- https://civitai.com/?types=Checkpoint - Overview of many stable diffusion models. Only models of the type _checkpoint_ can be used by Stable Diffusion UI.
- https://rentry.org/sdmodels - List of stable diffusion models from various sources