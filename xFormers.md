Support for [xFormers](https://github.com/facebookresearch/xformers) is available experimentally.

xFormers speeds up image generation, but can sometimes produce non-deterministic results (i.e. the same prompt+settings may not always produce the same results as before).

**Important!!** xFormers will only help on PCs with NVIDIA GPUs (or AMD with ROCm, if you've installed it). It is not useful on CPU-only computers or M1/M2 Macs.

# Installing xFormers
1. Double-click `Developer Console.cmd` (on Windows) or run `./developer_console.sh` (on Linux/Mac)
2. Run `python -m pip show torch torchvision` (**important:** please make a note of these two versions, incase you need to revert back to them)
3. Run the follow command:
 `python -m pip install --upgrade torch==2.0.1+cu118 torchvision==0.15.2+cu118 xformers==0.0.21 --extra-index-url https://download.pytorch.org/whl/cu118`
or use the [command generator](https://pytorch.org/get-started/locally/) (at the top of the page) from pytorch. That should be enough, you can now start Easy Diffusion like normal.

# Removing/uninstalling xFormers
If you face an issues, please rollback by:
1. Double-click `Developer Console.cmd` (on Windows) or run `./developer_console.sh` (on Linux/Mac)
2. Run `python -m pip uninstall xformers`
3. Optionally, revert the `torch` and `torchvision` version to what you had previously:
- Windows or Linux: Run `python -m pip install torch==version_noted_above torchvision==version_noted_above --index-url https://download.pytorch.org/whl/cu116`
- Mac: Run `python -m pip install torch==version_noted_above torchvision==version_noted_above`