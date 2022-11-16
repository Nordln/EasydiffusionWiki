# Prompt and Base Image
![image](https://user-images.githubusercontent.com/2499585/200661360-90c87055-b351-4946-801b-fd053eb84a45.png)
* Prompt: A textual prompt for stable diffusion to render - [[More on prompts|Writing prompts]]
* Load from a file: Load textual prompt from a .txt-file - one prompt per line
* Negative Prompt: A textual prompt for stable diffusion to avoid - [[More on negative prompts|Writing-prompts#negative-prompts]]
* Initial Image: A selector for a base image

# Image Settings
![image](https://user-images.githubusercontent.com/2499585/200583269-79c246a1-eadb-4685-bcb4-3ce3c67a9a95.png)
## Image Settings
* Seed: A number to prime the random generator with
* Number of images: 
  * (total) A number for how many images are to be generated in total
  * (in parallel) A number for how many images are to be generated at the same time
* Model: A drop-down-menu for selecting data models - [[More on data models|Custom-Models]]
* Custom VAE: A drop-down-menu for selecting Variational Auto Encoder - [[More on VAE|VAE-Variational-Auto-Encoder]]
* Image Size: drop-down-menus to select the resolution of the image to be generated
* Inference steps: A number for how many steps stable diffusion should use - [Example](https://getimg.ai/guides/interactive-guide-to-stable-diffusion-steps-parameter)
* Guidance Scale: A slider & number field that controls how much the imgage generation should follow the prompt - [Example](https://getimg.ai/guides/interactive-guide-to-stable-diffusion-guidance-scale-parameter)
* Output format: A drop-down-menu for selecting either jpeg or png
## Render Settings
* Show a live preview: Shows a live preview if enabled, otherwise will display the image when finished
* Fix incorrect faces and eyes: Uses GFPGAN - a face restauration algorithm to fix glitches in faces & eyes
* Upscale image by 4x: Uses [RealESRGAN](https://github.com/xinntao/Real-ESRGAN) to upscale the final image to 4x the size (512x512 will be 2048x2048)
  * RealESRGAN_x4plus is general-purpose
  * RealESRGAN_x4plus_anime_6B is optimized for anime

# Image Modifiers
![image](https://user-images.githubusercontent.com/2499585/200583339-783e49a6-8131-4bea-af66-cc311d626156.png)
* Cogwheel icon: Define custom image modifiers
* Image style: A pull-down-menu to change the type of icon for the pre-defined modifiers
  * Face: Shows faces for the icons in the style of the modifiers
  * Landscapes: Shows landscapes for the icons in the style of the modifiers
* Thumbnail size: A slider to change the size of the clickable modifiers
* Image modifiers: These are simply prompt parts, which will be added to the prompt if selected

# Settings
![image](https://user-images.githubusercontent.com/2499585/202213868-8137c365-5a1b-4dd2-ba9a-a5efb7f06dbd.png)
* Theme: A colour theme for the UI
* Auto-Save Images: Automatically saves images and a .txt-file with the settings to the specified location
* Save Location: A folder for saved images
* Enable Sound: Plays a sound on task completion
* Open browser on startup: Starts the default browser on startup with http://localhost:9000/ as URL
* Turbo Mode: generates images faster, but uses an additional 1 GB of GPU memory
* Use CPU (not GPU): Will force CPU-Rendering (very slow compared to GTX/RTX-Cards)
* Automatically pick the GPUs (experimental): Will select a GPU automatically
  * GPUs to use (experimental): A List of availible GPUs including the CUDA-Id
* Use Full precision: Will use more GPU Memory, required for NVidia GTX 1650/1660.
* Auto-Save Settings: Restore Settings on browser load
  * Configure: Opens a menu to set which settings are stored
* Beta Channel: Get the latest features immediately (but could be less stable). Please restart the program after changing this.

# Buttons in the rendered image (these are visible if the user hovers with the mouse over a rendered image)
![image](https://user-images.githubusercontent.com/2499585/200590572-b2ef2d74-1a5d-4394-8899-47c8578bedf1.png)
* Seed: The seed this particular image used
* Use as input: Uses the image as Input for img2img
* Download: Downloads the image
* Make Similar images: Enqueues a task using this image for img2img and generates 5 images
* Draw antoher 25 steps: Enquees a task using the the settings of that image and increases the Inference Step Count by 25
* Upscale (only visible if images wasn't already upscaled): Re-Renders the image wtih 4x-Upscaling enabled
* Fix Faces: Fixes incorrect faces and eyes using GFPGAN
