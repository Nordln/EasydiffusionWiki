Support for [xFormers](https://github.com/facebookresearch/xformers) is available experimentally.

xFormers speeds up image generation, but can sometimes produce non-deterministic results (i.e. the same prompt+settings may not always produce the same results as before).

# Installing xFormers
1. Double-click `Developer Console.cmd` (on Windows) or run `./developer_console.sh` (on Linux/Mac)
2. Run `python -m pip show torch torchvision` (**important:** please make a note of these two versions, incase you need to revert back to them)
3. Run the follow command, depending on the version of `torch` displayed in the previous command:
a. for `torch` 2.0.0: `python -m pip install xformers==0.0.18`
b. for `torch` 1.13.1: `python -m pip install xformers==0.0.16`

That should be enough, you can now start Easy Diffusion like normal.

# Removing/uninstalling xFormers
If you face an issues, please rollback by:
1. Double-click `Developer Console.cmd` (on Windows) or run `./developer_console.sh` (on Linux/Mac)
2. Run `python -m pip uninstall xformers`
3. Optionally, revert the `torch` and `torchvision` version to what you had previously:
- Windows or Linux: Run `python -m pip install torch==version_noted_above torchvision==version_noted_above --index-url https://download.pytorch.org/whl/cu116`
- Mac: Run `python -m pip install torch==version_noted_above torchvision==version_noted_above`