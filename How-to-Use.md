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


# Troubleshooting
Please try the common [troubleshooting](https://github.com/cmdr2/stable-diffusion-ui/wiki/Troubleshooting) steps. If that doesn't fix it, please ask on the [discord server](https://discord.com/invite/u9yhsFmEkB), or [file an issue](https://github.com/cmdr2/stable-diffusion-ui/issues).