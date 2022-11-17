**Experimental support for multiple GPUs!**

![image](https://user-images.githubusercontent.com/844287/202389537-3114474a-a850-49c7-800d-8db891e93fd9.png)

![image](https://user-images.githubusercontent.com/844287/202389573-8406ef69-0f58-402c-a6b2-2fbc135c0c89.png)

The project will now automatically run on multiple GPUs by default, if your PC has them. For e.g. two tasks will run in parallel across two GPUs, if you have them.

## How can I use this?
To use this feature, please start one browser tab per GPU, and spread your image tasks across the browser tabs. Start your tasks in each browser tab, and they'll run in parallel on your GPUs.

We're working on removing the need to open multiple browser tabs.

For finer control, you can manually choose which GPUs you want in the `Settings` tab. Otherwise the program will decide which GPUs to run on, based on their free memory.

## Why don't I see this option in the Settings tab?
This multi-GPU option will be visible in the UI only if you have more than 1 GPU. Once you change your GPU settings, please press the Save button.

## What is automatic GPU selection? Why should I use that?
The program picks the GPUs automatically, unless you customize them in the `Settings` tab. **We recommend you use automatic GPU selection**, since it'll automatically stop using GPUs that you're using for something else (e.g. for gaming). And once a GPU becomes free (e.g. you finished gaming), it'll automatically start using that GPU again.

## How does automatic GPU selection work?
The automatic GPU selection works by picking the 65 percentile of GPUs, by free memory. In simpler terms, it'll automatically pick GPUs that are similar (in terms of free memory).

For example:
- if your PC has two or more similar GPUs, e.g. a `2070 8gb` and a `2060 6gb`, it'll start on both GPUs by default
- if your PC has very different GPUs, e.g. `3060 8gb` and a `1660 4gb`, it'll only start on `3060` by default, because it'll be much faster overall. *You can still choose to start on both `3060` and `1660`, by selecting both GPUs in the `Settings` tab in the UI. This choice will be saved across restarts.*
- if one of the GPUs is already being used heavily, for e.g. for gaming (i.e. it's low on free memory), that GPU won't be selected, even if it's a powerful GPU
- conversely, if a previously heavily-used GPU becomes free in the future (i.e. you finished gaming), it'll automatically start getting used, *without requiring you to restart the program or take any action*