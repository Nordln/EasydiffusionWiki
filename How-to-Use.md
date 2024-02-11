# Usage
After installing the software, navigate to your browser (we recommend using either Chrome, Edge or Firefox to prevent issues) and navigate to http://localhost:9000 . It may take the project a few seconds to get ready.
When loaded this is what it should look like:

![image](https://user-images.githubusercontent.com/110454200/213924983-b8e5261a-8545-444c-a8be-271a495f145f.png)

## Tips
* You can enqueue multiple `Jobs`. The project will process them one by one. You don't need to wait until the first job is finished.
* You can queue up many rendering jobs at once by entering one prompt per line. When you click 'Make Image', a job will be generated for each line in the prompt textbox:

![image](https://user-images.githubusercontent.com/110454200/213926311-ba9286d1-00c6-4862-8ba3-6d1f4762e1d5.png)

* You can use `Face Correction` or `Upscaling` to improve the image further.
* You can click `Use as Input` on a generated image, to use it as the input image for your next generation. This can be useful for sequentially refining the generated image with a single click.
* Images with the same aspect ratio of your generated image work best. E.g. 1:1 if you're generating images sized 512x512.

## Image Modifiers

These are just suggestions to get you started.  Different models will give different effects, and settings that are ideal for one model may not be applicable to another.

* Image Size: Start with 512x512 with SD 1.4 or 1.5 models.  With SDXL, start with 1024x1024. You can increase/decrease these slightly - often, 512x768 will still work well with SD 1.5 models, but any larger, and you'll start to see odd duplications in your results.  Use image-to-image to go larger.
* Inference Steps: try using between 30 and 40 for most models.  For Turbo models, use between 5 and 8 to generate faster than non-Turbo models.
* Guidance Scale: 7.5 is a good starting point, but anywhere from 5 to 15 works for many models.  For Turbo models, this should be between 1 and 5, depending upon the model.
* Model: SDXL models can produce better results than SD 1.4 and SD 1.5 models, but require a bit more resources.
The base SDXL model can be found here: [sd_xl_base_1.0.safetensors](https://huggingface.co/stabilityai/stable-diffusion-xl-base-1.0/blob/main/sd_xl_base_1.0.safetensors)
The VAE matching this SDXL model can be found here: [sd_xl_base_1.0_0.9vae.safetensors](https://huggingface.co/stabilityai/stable-diffusion-xl-base-1.0/blob/main/sd_xl_base_1.0_0.9vae.safetensors)
* Sampler: Generally, you can use any sampler, but some models mostly work with one particular sampler.  For example, some Turbo models specifically require DPM++ SDE, or else results will be poorer.

# Troubleshooting
Please try the common [troubleshooting](https://github.com/cmdr2/stable-diffusion-ui/wiki/Troubleshooting) steps. If that doesn't fix it, please ask on the [discord server](https://discord.com/invite/u9yhsFmEkB), or [file an issue](https://github.com/easydiffusion/easydiffusion/issues).