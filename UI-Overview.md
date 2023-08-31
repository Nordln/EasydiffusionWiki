# Input

![image](https://github.com/easydiffusion/easydiffusion/assets/844287/ad9e8d5f-44f4-44ed-8da9-5b45c3e44ea1)

**Prompt**: Describe the image that you want to create. E.g. `photograph of an astronaut riding a horse`.

**Load from a file** (optional): Load a prompt from a .txt file. This is useful for creating multiple tasks. Please put one prompt per line.

**Negative Prompt** (optional): Describe what to *avoid* when rendering your image. E.g. `bad hands, grainy, fog`.

**Initial Image** (optional): Choose an image from your PC (or paste an image), to describe to the AI visually. The AI will try to create a similar image. Choose an image from your computer.

# Image Settings

![image](https://github.com/easydiffusion/easydiffusion/assets/844287/3dfe1cf6-2d50-4b68-b1cd-7549da691160)

## Image Settings
**Seed**: A number that will be used to randomize your image. 

**Number of Images**: 
  * (total): How many images are to be generated in total.
  * (in parallel): How many images are to be generated at the same time.

**Model**: Select a data model which will be used to determine how to render your image.

**Custom VAE**: Selecting a `Variational Auto Encoder`.

**Image Size**: Select what the resolution of the image should be.

**Inference Steps**: Stable Diffusion works by generating images in multiple attempts. The number of attempts is what's called `Inference Steps`. 
[Example](https://getimg.ai/guides/interactive-guide-to-stable-diffusion-steps-parameter)

**Guidance Scale**: Controls how much the image generation should follow the prompt. [Example](https://getimg.ai/guides/interactive-guide-to-stable-diffusion-guidance-scale-parameter)

**Output Format**: To select the file format of the rendered image. Can be either `JPEG` or `PNG`.

## Render Settings

**Show a live preview**: Shows a live preview of the image while it's rendering. Otherwise the image will only be displayed when the image has finished rendering. This is off by default.

**Fix incorrect faces and eyes**: Uses GFPGAN - a face restauration algorithm to fix glitches in faces & eyes.

**Upscale image by 4x**: Uses [RealESRGAN](https://github.com/xinntao/Real-ESRGAN) to upscale the final image to 4x the size (512x512 will be 2048x2048)
  * RealESRGAN_x4plus is general-purpose
  * RealESRGAN_x4plus_anime_6B is optimized for anime

# Image Modifiers

![image](https://user-images.githubusercontent.com/110454200/213927607-9a4323cb-4178-4645-9645-43bf768641f4.png)

**Cogwheel Icon**: To define custom image modifiers.

**Image Style**: To change the type of icon for the pre-defined modifiers.
  * Face: Shows faces for the icons in the style of the modifiers.
  * Landscapes: Shows landscapes for the icons in the style of the modifiers.

**Thumbnail Size**: A slider to change the size of the clickable modifiers.

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
