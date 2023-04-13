## What are Stable Diffusion models?
Stable Diffusion UI uses so called models to create the images. The models get trained using many images and image descriptions. During the installation,
a default model gets downloaded, the sd-v1-4 model. Other models exist. Some of them use sd-v1-4 as their base and were then trained on additional images, while other models were trained from scratch.

Depending on the images used during the training, the models generate a different look and understand different prompts.

## Installing a model
If you've downloaded a model, you can make it available to Stable Diffusion UI:
- Copy the model file to the `models\stable-diffusion` folder (inside the installed folder). The file should have the suffix `.ckpt` or `.safetensors`.
- If the model comes with a `.yaml` file, please place that yaml file next to the model, with the same name. For e.g. if the model is `some-model.ckpt` (or `some-model.safetensors`), then please rename the yaml file to `some-model.yaml`, and place it next to the model file in the same folder.
- Refresh the model list using the "reload"-icon in the "Models" section in the image settings:

    ![image](https://user-images.githubusercontent.com/5852422/231899233-cafd4449-e2a0-4a46-8308-b6ee4bc1cbfe.png)

  The model should now be visible in the "Models" dropdown.

### Troubleshooting - Black images?
Please add this to the **end** of the `.yaml` file that came with your model:
```yaml
extra:
  attn_precision: "fp32"
```

For e.g. please see the end of this file for reference: https://github.com/easydiffusion/sdkit/blob/main/sdkit/models/models_db/configs/v2.1-inference-v.yaml#L69

## Web resources
**Note:** These links lead to websites outside of the Stable Diffusion UI project.

**Note:** Stable Diffusion models can contain malware. ALWAYS SCAN FOR VIRUSES.

- https://civitai.com/?types=Checkpoint - Overview of many stable diffusion models. Only models of the type _checkpoint_ can be used by Stable Diffusion UI.
- https://rentry.org/sdmodels - List of stable diffusion models from various sources