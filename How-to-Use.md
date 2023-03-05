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

## Samplers

Here is a rough overview of the behaviors of different sampler implementations:

[![SD](https://user-images.githubusercontent.com/7282547/222912410-32e65aef-317f-4f35-89bd-45d92569c317.jpg)](https://user-images.githubusercontent.com/7282547/222912410-32e65aef-317f-4f35-89bd-45d92569c317.jpg)

Most samplers are deterministic. If re-run with the same seed and settings, it will generate the same image. You can also increase the step size to see if artifacts in the image clear up, but it may be a slightly different image.

Note that `euler_a` and `dpm2_a` are *not always* deterministic. They can create different images when run in different batch sizes.

[![SD2](https://user-images.githubusercontent.com/7282547/222918227-052d5c8f-f6db-4bcb-bfe8-2902228171db.jpg)](https://user-images.githubusercontent.com/7282547/222918227-052d5c8f-f6db-4bcb-bfe8-2902228171db.jpg)
[![SD-full_small](https://user-images.githubusercontent.com/7282547/222926791-728d2f46-fd16-4b93-a929-dc33f2fe4e92.jpg)](https://user-images.githubusercontent.com/7282547/222926791-728d2f46-fd16-4b93-a929-dc33f2fe4e92.jpg)

# Troubleshooting
Please try the common [troubleshooting](https://github.com/cmdr2/stable-diffusion-ui/wiki/Troubleshooting) steps. If that doesn't fix it, please ask on the [discord server](https://discord.com/invite/u9yhsFmEkB), or [file an issue](https://github.com/cmdr2/stable-diffusion-ui/issues).