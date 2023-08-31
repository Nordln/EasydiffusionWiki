Easy Diffusion includes a number of different "samplers", which create slightly different images. Each sampler follows a different process for converting your input into a final image.

It's best to experiment with different samplers to find one that works well for the image that you're making. For e.g. one image may look better to you with one sampler, and another image might look better with another sampler.

Here is a rough overview of the behaviors of different sampler implementations:

[![SD](https://user-images.githubusercontent.com/7282547/222912410-32e65aef-317f-4f35-89bd-45d92569c317.jpg)](https://user-images.githubusercontent.com/7282547/222912410-32e65aef-317f-4f35-89bd-45d92569c317.jpg)

Most samplers are deterministic. If re-run with the same seed and settings, it will generate the same image. You can also increase the step size to see if artifacts in the image clear up, but it may be a slightly different image.

Note that **Ancestral** sampler, `euler_a`, `dpm2_a` and `dpmpp_2s_a` are *not always* deterministic. They can create different images when run in different batch sizes. 
`dpm_adaptive` use an automatic steps count algorithm, ignoring the user Inference Steps setting.

[![SD2](https://user-images.githubusercontent.com/7282547/222918227-052d5c8f-f6db-4bcb-bfe8-2902228171db.jpg)](https://user-images.githubusercontent.com/7282547/222918227-052d5c8f-f6db-4bcb-bfe8-2902228171db.jpg)

[![SD-full2_small](https://user-images.githubusercontent.com/7282547/222985489-b14b160f-ea79-464f-80f7-45092f5b35f9.jpg)](https://user-images.githubusercontent.com/7282547/222985489-b14b160f-ea79-464f-80f7-45092f5b35f9.jpg)