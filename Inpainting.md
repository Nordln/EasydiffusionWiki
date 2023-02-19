
![image](https://user-images.githubusercontent.com/5852422/219961229-66175d43-f899-4667-9028-15ee11dd2caa.png)


# Old documentation

**Inpainting** is a stable diffusion mode, in which stable diffusion only changes a part of the initial image, while keeping other parts of the
initial image intact. To use inpainting, first select an initial image using the "Choose file" button (①), then put a checkmark into the In-Painting checkbox (②):

![image](https://user-images.githubusercontent.com/5852422/197878159-8edda335-5cfa-4080-aec4-f245038a6bfc.png)

The In-Painting tool gets activated by this and can be used to select the area which the AI will paint into:

![image](https://user-images.githubusercontent.com/5852422/197879010-40a51231-2d2c-46b6-a011-9d7df2056aac.png)

The first two buttons activate the brush or the rubber. Using the brush, you mark areas. Using the rubber, you can un-mark areas again. Marked areas 
get desaturated.

The slider can be used to change the size of the brush.

The next two buttons can be used to undo or redo your last actions.

The last button clears the marked area.

Inpainting works together with the prompt. In the prompt, describe the image that you want to get. In general, it helps to also describe the 
part of the picture that the AI shall not change.

## Examples

The following example used the prompt `black woman, niagara falls in the background`, a guidance of 7.5, a prompt strength of 0.8 and 45 steps:

<table><tr><td>

**Initial image**

![image](https://user-images.githubusercontent.com/5852422/197881315-20581991-ceb2-4961-ae8c-a2eea33663eb.png)

</td><td>

**Mask**

![image](https://user-images.githubusercontent.com/5852422/197881528-f8edc50f-6a1f-4e59-9c47-ef9e63454dc1.png)

</td><td>

**Result**

![image](https://user-images.githubusercontent.com/5852422/197881635-1500caad-339a-4cb9-8951-be1ec3b467e4.png)

</td></tr></table>

You can notice how the initial image impacted the result image: green and brown areas of the initial image result in green and brown areas of the result image. It's usually hard to get e.g. a blue sky if there's nothing blue in the initial image. To guide the AI, paint some sky into the initial image
using a painting software:

<table><tr><td>

**Initial image**

![image](https://user-images.githubusercontent.com/5852422/197882984-7cb0795f-8e22-42a2-a757-4e46d8862994.png)

</td><td>

**Mask**

![image](https://user-images.githubusercontent.com/5852422/197883385-87ec0b37-c83d-4d01-b31b-09ceed75bbb8.png)

</td><td>

**Result**

![image](https://user-images.githubusercontent.com/5852422/197883112-e6273d5f-dd31-46ce-a9bd-c0b331bc5302.png)

</td></tr></table>

## Tips
* Larger areas work better than smaller areas.
* The initial image impacts the result. If you can't get good results, try to sketch the desired results using a simple paint program.
* The unmasked area will be slightly changed by the inpainting process. This is a known bug and shall be fixed in upcoming versions.
    Compare the camera lens in the above examples:
        
    ![image](https://user-images.githubusercontent.com/5852422/197884233-b28dc993-9a38-49f7-b36a-e81497e16ef5.png)
    ![image](https://user-images.githubusercontent.com/5852422/197884029-1d30eed1-e6b3-4317-8c3e-d847766d4cae.png)

    To repair these distortions, open the initial and result images as two layers in a photo editor and create a mask to select the initial image
    where it should be kept intact.

## Copyright notice
The [initial image](https://commons.wikimedia.org/wiki/File:Femmes_Photographes.jpg) used in the examples above is © Moussa Kalapo and licensed 
under the [CC-BY-SA-4.0 license](https://creativecommons.org/licenses/by-sa/4.0/).