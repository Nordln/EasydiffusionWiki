🔥🔥This feature is currently only available on the beta branch, which might be instable and break your installation!🔥🔥

----

Here is the format used for the files and produced by the copy setting button.
It should make it easy to exchange settings in chat and then save to file and drop into the interface to load.
``` json
{
    "numOutputsTotal": 6,
    "reqBody": {
        "prompt": "The Sandman fighting a stapler, Evil",
        "negative_prompt": "text prompt words",
        "width": 448,
        "height": 640,
        "seed": 6380250,
        "num_inference_steps": 50,
        "guidance_scale": 7.5,
        "prompt_strength": 0.8,
        "use_face_correction": false,
        "sampler": "euler_a",
        "use_stable_diffusion_model": "arcane-diffusion-v3",
        "numOutputsParallel": 1,
        "stream_image_progress": true,
        "show_only_filtered_image": true,
        "output_format": "jpeg"
    }
}
```
Other properties that can be included in the json.
Those are NOT included by the copy settings button.
But can be added to your own json files manually and they will be applied if present.
Using JSON, all properties are optional, only include those you want to update when loading the file.
``` json
{
    "reqBody": {
        "use_cpu": false,
        "turbo": true,
        "use_full_precision": false,
        "save_to_disk_path": "~/StableDiffusion/renders/"
    }
}
```
For the txt file, the Width, Height and Seed are required and NEEDS to be in that order one per line, not case sensitive.
Prompts can contain anything, including the words seeds, width and height.
There is also no header, quotes or delimiter for when the prompt ends.
Because of this, the sequence marking the end of prompt is the presence of width, height and seed in that order followed by a number each on it's own line.
```
Observing a desolate (landscape of corpses), 17th century japanese painting style
Width: 832
Height: 576
Seed: 2866349
```
The above is the minimum the Web UI will recognize as valid to import.
All the other settings are optional in text format.
```
Steps: 50
Guidance Scale: 15.0
Prompt Strength: 0.8
Use Face Correction: None
Use Upscaling: RealESRGAN_x4plus
Sampler: euler_a
Negative Prompt: text prompt words
Stable Diffusion model: /StableDiffusion/sd-ui/models/stable-diffusion/v1-5-pruned-emaonly.ckpt
```
----
https://discord.com/channels/1014774730907209781/1021695193499582494/1037637483342602320
