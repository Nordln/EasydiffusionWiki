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

* **Image Size**: Select what the resolution of the image should be. You can click the ![image](https://github.com/easydiffusion/easydiffusion/assets/844287/6897a367-0754-4e7c-b8d1-026ad01df9b6) icon to edit the image size or select common image sizes. You can click the ![image](https://github.com/easydiffusion/easydiffusion/assets/844287/683b1799-5ad7-4fed-a8d4-7d5af82d4f84) icon to exchange the width and height values.

* **Inference Steps**: Stable Diffusion works by generating images in multiple steps. The number of steps is what's called `Inference Steps`. The more steps you draw, the more the AI gets to modify the image. Read more about [inference steps](https://getimg.ai/guides/interactive-guide-to-stable-diffusion-steps-parameter).

* **Guidance Scale**: Controls how strongly the AI should follow your prompt. Read more about [guidance scale](https://getimg.ai/guides/interactive-guide-to-stable-diffusion-guidance-scale-parameter).

* **LoRA**: Select the LoRA model to use, and change the number to alter the strength of its effect. Read more about [[LoRA]].

* **Seamless Tiling**: Generates repeatable images, for e.g. for repeating textures in games or artwork as backgrounds. Read more about [[Seamless Tiling]].

* **Output Format**: To select the file format of the rendered image. Can be either `JPEG`, `WEBP`, or `PNG`.

## Render Settings

**Show a live preview**: Shows a live preview of the image while it's rendering. Otherwise the image will only be displayed when the image has finished rendering. This is off by default.

**Fix incorrect faces and eyes**: Uses GFPGAN - a face restauration algorithm to fix glitches in faces & eyes.

**Upscale image by 4x**: Uses [RealESRGAN](https://github.com/xinntao/Real-ESRGAN) to upscale the final image to 4x the size (512x512 will be 2048x2048)
  * RealESRGAN_x4plus is general-purpose
  * RealESRGAN_x4plus_anime_6B is optimized for anime

# Settings

![image](https://user-images.githubusercontent.com/844287/227230807-58edc7a0-5744-48c6-a6bb-3b06b21e8c8e.png)

**Theme**: A color theme for the UI.

**Auto-Save Images**: Automatically saves images and a .txt-file with the settings to your specified location.

**Save Location**: A folder for where images will save.

**Enable Sound**: Plays a sound when a task is completed.

**Open browser on startup**: Starts the default browser on startup with http://localhost:9000/ as URL.

**VRAM Usage Level**: *Low*, *Balanced*, and *High*. Increasing levels generate images faster, but uses additional GPU memory.

**Use CPU (not GPU)**: Will force CPU-Rendering. Very slow compared to GTX/RTX-Cards.

**Automatically pick the GPUs (experimental)**: Will select a GPU automatically.

**GPUs to use**: A list of available GPUs including the CUDA-ID.

**Use Full Precision**: Will use more GPU Memory, required for NVIDIA GTX 1650/1660.

**Auto-Save Settings**: Restores Settings on browser load.
  * Configure: Opens a menu to set which settings are stored.

**Beta Channel**: Get the latest features immediately with the downside of decreased stability. Please restart the program after changing this.

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
