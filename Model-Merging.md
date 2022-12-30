**This feature is available in versions 2.5.0 and higher**

You can merge two Stable Diffusion models (in `.ckpt` or `.safetensors` formats). A UI is planned for this, but for now, you can follow these steps to merge models easily:

1. Double-click the `Developer Console.cmd` file (on Linux: open terminal, and run `./developer_console.sh`)
2. Type `python` and press Enter.
3. Type `from sdkit.train import merge_models` and press Enter.
4. Type:
```python
merge_models('C:/path/to/first_model.ckpt', 'C:/path/to/second_model.safetensors', ratio=0.3, out_path='C:/path/to/merged_model.safetensors', use_fp16=True)
```
and press Enter.

Set the correct paths to the two models.

Set the `ratio` to a number between 0 and 1. This decides the contribution of the two models. A ratio of 0 means only the first model will be used, and a ratio of 1 means only the second model will be used. A ratio of 0.5 means half of each model will be used.

That's it. Your merged model will be stored at the path you mentioned.

We're working on providing a UI for this as well.