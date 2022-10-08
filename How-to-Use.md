# Usage
Open http://localhost:9000 in your browser (after running step 3 previously). It may take a few moments for the back-end to be ready.

## With a text description
1. Enter a text prompt, like `a photograph of an astronaut riding a horse` in the textbox.
2. Press `Make Image`. This will take some time, depending on your system's processing power.
3. See the image generated using your prompt.

## With an image
1. Click `Browse..` next to `Initial Image`. Select your desired image.
2. An optional text prompt can help you further describe the kind of image you want to generate.
3. Press `Make Image`. See the image generated using your prompt.

You can use Face Correction or Upscaling to improve the image further.

**Pro tip:** You can also click `Use as Input` on a generated image, to use it as the input image for your next generation. This can be useful for sequentially refining the generated image with a single click.

**Another tip:** Images with the same aspect ratio of your generated image work best. E.g. 1:1 if you're generating images sized 512x512.

## Problems? Troubleshooting
Please try the common [troubleshooting](Troubleshooting.md) steps. If that doesn't fix it, please ask on the [discord server](https://discord.com/invite/u9yhsFmEkB), or [file an issue](https://github.com/cmdr2/stable-diffusion-ui/issues).

# Image Settings
You can also set the configuration like `seed`, `width`, `height`, `num_outputs`, `num_inference_steps` and `guidance_scale` using the 'show' button next to 'Image settings'.

Use the same `seed` number to get the same image for a certain prompt. This is useful for refining a prompt without losing the basic image design. Enable the `random images` checkbox to get random images.

![Screenshot of advanced settings](media/config-v6.jpg?raw=true)

# System Settings
The system settings are reachable via the cogwheel symbol on the top right. It can be used to configure whether all generated images should 
saved be automically, or to tune the Stable Diffusion image generation.

![Screenshot of advanced settings](media/system-settings-v2.jpg?raw=true)

# Image Modifiers
![Screenshot of advanced settings](media/modifiers-v1.jpg?raw=true)