SDXL offers two models. You can use whichever one you prefer.

* Base model (works for text-to-image, image-to-image, and inpainting): https://huggingface.co/stabilityai/stable-diffusion-xl-base-1.0/resolve/main/sd_xl_base_1.0.safetensors
* Refiner model (image-to-image only): https://huggingface.co/stabilityai/stable-diffusion-xl-refiner-1.0/resolve/main/sd_xl_refiner_1.0.safetensors

Save the model to the `models/stable-diffusion` folder.

Then in the Easy Diffusion UI, click the "refresh" icon next to the Models dropdown, and select the downloaded model and generate the image.

Tip: If you get "Out of Memory" errors, try setting the `VRAM Usage Level` setting to `"low"` in the Settings tab, and press `Save`.