🔥🔥This feature is currently only available on the beta branch, which might be instable and break your installation!🔥🔥

## What does a VAE do? 

In short, it improves the generated images. A VAE is trained for certain aspects of the image, and the default VAE bundled in our UI (`vae-ft-mse-840000-ema-pruned`) improves the eyes in generated images.

Stable Diffusion UI installs and starts using the `vae-ft-mse-840000-ema-pruned` VAE file that works with all Stable diffusion models. This uses the official one: https://huggingface.co/stabilityai/sd-vae-ft-mse-original

To use a custom VAE file, you can place any number of VAE files ending with `.ckpt` or `.vae.pt` inside the `models/vae` folder, and refresh your browser UI. After that, you can select that VAE in Image Settings.