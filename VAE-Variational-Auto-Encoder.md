
## What does a VAE do? 

In short, it improves the generated images. A VAE is trained for certain aspects of the image, and the default VAE bundled in our UI (`vae-ft-mse-840000-ema-pruned`) improves the eyes in generated images.

Stable Diffusion UI installs and starts using the `vae-ft-mse-840000-ema-pruned` VAE file that works with all Stable diffusion models. This uses the official one: https://huggingface.co/stabilityai/sd-vae-ft-mse-original

## How to use a custom VAE?
Put your VAE file ending with `.ckpt` or `.vae.pt` inside the `models/vae` folder, like this:
![image](https://user-images.githubusercontent.com/844287/200801595-17276b3a-62e0-4d06-bfe1-a6481ba7921d.png)

Then refresh your browser UI. After that, you can select the desired VAE file in Image Settings:
![image](https://user-images.githubusercontent.com/844287/200802028-d35ceda1-8816-4d5a-958e-168c6ad3fbd5.png)
