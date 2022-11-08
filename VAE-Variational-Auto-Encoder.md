🔥🔥This feature is currently only available on the beta branch, which might be instable and break your installation!🔥🔥

## What does a VAE do? 

In short, it improves the generated images. A VAE is trained for certain aspects of the image, and the default VAE bundled in our UI (`vae-ft-mse-840000-ema-pruned`) improves the eyes in generated images.

Stable Diffusion UI installs and starts using the `vae-ft-mse-840000-ema-pruned` VAE file that works with all Stable diffusion models. This uses the official one: https://huggingface.co/stabilityai/sd-vae-ft-mse-original

You have two ways to use a custom VAE file:
1. Let's say you're using a model file named `my-model-1.ckpt`. You can now place a VAE file for that model, with the same name (i.e `my-model-1.vae.pt`) inside `models/stable-diffusion`, next to your `my-model-1.ckpt` file. The custom VAE file should have the same name, with `.vae.pt` instead of `.ckpt`. This will result in this VAE file being used (instead of the default) whenever you use `my-model-1` to generate your image.

2. You can place any number of VAE files ending with `.vae.pt` inside `models/stable-diffusion`, and refresh your browser UI. After that, you can set the Default VAE in System Settings (top-right corner of the UI). This VAE will now be used by default, unless a model has custom VAE (set in option 1, described above).
