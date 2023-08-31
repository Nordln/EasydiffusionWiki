# Input

![image](https://github.com/easydiffusion/easydiffusion/assets/844287/ad9e8d5f-44f4-44ed-8da9-5b45c3e44ea1)

* **Prompt**: Describe the image that you want to create. E.g. `photograph of an astronaut riding a horse`.

* **Load from a file** (optional): Load a prompt from a .txt file. This is useful for creating multiple tasks. Please put one prompt per line.

* **Negative Prompt** (optional): Describe what to *avoid* when rendering your image. E.g. `bad hands, grainy, fog`.

* **Initial Image** (optional): Choose an image from your PC (or paste an image), to describe to the AI visually. The AI will try to create a similar image. Choose an image from your computer.

* **Image Modifiers** (optional): A collection of useful words that guide the AI to make images in a particular style, e.g. "line art". You can read more about Image Modifiers at [this link](https://github.com/easydiffusion/easydiffusion/wiki/Image-Modifiers).

* **Embeddings** (optional): A collection of words whose meaning you can customize by downloading special files to the `models/embeddings` folder. You can read more about Embeddings at [this link](https://github.com/easydiffusion/easydiffusion/wiki/Embeddings).

# Image Settings

![image](https://github.com/easydiffusion/easydiffusion/assets/844287/3dfe1cf6-2d50-4b68-b1cd-7549da691160)

* **Seed**: A number that will be used to randomize your image. If you use the same number, the same image will be generated.

* **Number of Images**: 
  * (total): How many images are to be generated in total.
  * (in parallel): How many images are to be generated at the same time.

* **Model**: Select the Stable Diffusion model which will be used to determine how to render your image. You can read more about [[custom models]].

* **Clip Skip**: Advanced topic. Read more about [[Clip Skip]].

* **ControlNet Image**: Advanced topic. Read more about [[ControlNet]].

* **Custom VAE**: Advanced topic. Read more about [[VAE Variational Auto Encoder]].

* **Sampler**: The technique used by the AI to create the image. Read more about [[Samplers]].

* **Image Size**: Select what the resolution of the image should be. You can click the settings icon ![image](https://github.com/easydiffusion/easydiffusion/assets/844287/6897a367-0754-4e7c-b8d1-026ad01df9b6) to edit the image size or select common image sizes. You can click the exchange icon ![image](https://github.com/easydiffusion/easydiffusion/assets/844287/683b1799-5ad7-4fed-a8d4-7d5af82d4f84) to exchange the width and height values.

* **Inference Steps**: Stable Diffusion works by generating images in multiple steps. The number of steps is what's called `Inference Steps`. The more steps you draw, the more the AI gets to modify the image. Read more about [inference steps](https://getimg.ai/guides/interactive-guide-to-stable-diffusion-steps-parameter).

* **Guidance Scale**: Controls how strongly the AI should follow your prompt. Read more about [guidance scale](https://getimg.ai/guides/interactive-guide-to-stable-diffusion-guidance-scale-parameter).

* **LoRA**: Select the LoRA model to use, and change the number to alter the strength of its effect. Read more about [[LoRA]].

* **Seamless Tiling**: Generates repeatable images, for e.g. for repeating textures in games or artwork as backgrounds. Read more about [[Seamless Tiling]].

* **Output Format**: To select the file format of the rendered image. Can be either `JPEG`, `WEBP`, or `PNG`.

## Render Settings

* **Show a live preview**: Shows a live preview of the image while it's rendering. Otherwise the image will only be displayed when the image has finished rendering. This is off by default.

* **Fix incorrect faces and eyes**: Uses GFPGAN or CodeFormer - a face restauration algorithm to fix glitches in faces & eyes.

* **Upscale image**: Uses [RealESRGAN](https://github.com/xinntao/Real-ESRGAN) or [Latent Upscale](https://huggingface.co/docs/diffusers/api/pipelines/stable_diffusion/latent_upscale) to increase the resolution of the final image by 2x or 4x (i.e. 512x512 will be 2048x2048)
  * RealESRGAN_x4plus is general-purpose
  * RealESRGAN_x4plus_anime_6B is optimized for anime

* **Show only corrected image**: Shows only the final image, e.g. the scaled up/fixed image. Disable to see both the images, i.e. the image before applying "fix faces" or "upscale", as well as the final image.

# Settings

![image](https://github.com/easydiffusion/easydiffusion/assets/844287/6c5d520e-b6fe-493c-9535-4a83ec1736b6)

* **Theme**: A color theme for the UI.

* **Auto-Save Images**: Automatically saves the generated images (and optionally the settings used) to a folder in your PC.
  * **Save Location**: The folder where the images will be saved.
  * **Metadata format**: The format to optionally save the settings used to generate the image. Options: `none` (i.e. metadata won't be saved), `txt` (a plain text file), `json`, `embed` (i.e. embed it in the image file), `embed & txt`, and `embed & json`.

* **Block NSFW images**: Blurs images with nudity or content that's not suitable for everyone to see. This will download an AI model the first time you use it, to help with NSFW detection.

* **Enable Sound**: Plays a sound when all pending tasks have been completed.

* **Process newest jobs first**: Reverses the normal processing order.

* **Extract LoRA tags from the prompt**: Automatically extract lora tags like <lora:name:0.4> from the prompt, and apply the correct LoRA (if present).

* **Open browser on startup**: Starts the default browser on startup with http://localhost:9000/ as URL.

* **GPU Memory Usage**: *Low*, *Balanced*, and *High*. Increasing levels generate images faster, but uses additional GPU memory.

* **Use CPU (not GPU)**: Will generate images using the CPU. Nearly 20 times slower compared to using a graphics card.
  * **Automatically pick the GPUs (experimental)**: Visible only if you have multiple GPUs. Will pick the GPUs automatically based on their processing power and free memory.
  * **GPUs to use**: Visible only if you have multiple GPUs, and want to manually select which GPUs to use for generating images.

* **Auto-Save Settings**: Saves your settings, so that they're preserved even if you restart your browser.
  * **Configure**: Opens a menu to set which settings will be saved automatically.

* **Profile Name**: Use this to have different settings for different users.

* **Beta Channel**: Get the latest features under development immediately, but they might contain a few bugs. Please press `Save` and restart the program after changing this.

* **Use the new v3 engine**: Use version 3 of Easy Diffusion's engine, which contains the latest features like SDXL, ControlNet, LoRAs etc. Disable this to use the older version 2 engine. Please press `Save` and restart the program after changing this.

# Buttons in the rendered image 
This is visible if the user hovers with the mouse over a rendered image.

![image](https://user-images.githubusercontent.com/2499585/200590572-b2ef2d74-1a5d-4394-8899-47c8578bedf1.png)

**Seed**: The seed this particular image used.

**Use as Input**: Uses the image as Input for img2img.

**Download**: Downloads the image.

**Make Similar Images**: Enqueues a task using this image for img2img and generates 5 images.

**Draw another 25 steps**: Enqueues a task using the the settings of that image and increases the Inference Step Count by 25.

**Upscale**: Re-Renders the image with 4x-Upscaling enabled. Visible if images wasn't already upscaled.

**Fix Faces**: Fixes incorrect faces and eyes using GFPGAN.

# NSFW Filter
You can prevent NSFW images from being displayed by enabling the `Blur NSFW` option in the Settings tab.

![image](https://user-images.githubusercontent.com/844287/236732669-4996a782-04c1-4d57-b2c2-e49e43c563dd.png)
