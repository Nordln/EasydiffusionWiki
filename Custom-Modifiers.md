This feature allows adding custom modifiers with images, instead of just text values.

It looks for images in a `modifiers` folder and adds them to the object read from `modifiers.json`.  If an image is directly inside of `modifiers` then it will be added to a Modifiers category. Images in direct subfolders will have the folder names as the category. Otherwise images in sub-sub folders etc... will have the folder path be the category (ex: `modifiers/Foo/Bar` will become `Foo/Bar`). The order of categories defined in `modifiers.json` is preserved, and new categories will be added at the end sorted alphabetically.

If the image ends in ` Portrait`, `.Portrait`, `-Portrait`, or `_Portrait` (case insensitive) it will be considered a portrait image, and if it has Landscape instead it would be a landscape image, and the portrait/landscape suffix will be removed from the modifier name. Otherwise the image will be used as both the portrait and landscape.

![image](https://user-images.githubusercontent.com/8977984/219980954-c2b350ab-c3d1-45dc-b6a6-7d04af5b8693.png)
![image](https://user-images.githubusercontent.com/8977984/219980980-df896285-0229-4516-9c71-31d91cde41c6.png)
![image](https://user-images.githubusercontent.com/8977984/219980995-1095b386-bbf0-47a9-8ba6-d18140684c32.png)
![image](https://user-images.githubusercontent.com/8977984/219981075-90f2c758-c136-4901-a040-638c23440f0f.png)
![image](https://user-images.githubusercontent.com/8977984/219981125-02bf603a-d1b1-400c-bc0a-9f8f10b5c3ea.png)
![image](https://user-images.githubusercontent.com/8977984/219981180-f8fef917-94bc-4750-9eb4-9cf2c3618031.png)
![image](https://user-images.githubusercontent.com/8977984/219981157-3e61b812-a362-4bc8-b9eb-72530b60bd05.png)