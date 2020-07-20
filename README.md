# Finding sky pixels in an image using pre-trained PSPNet segmentation model

The model takes input as an image containing some sky area and marks the sky area in white and other areas in black.
The [training data](https://mypages.valdosta.edu/rpmihail/skyfinder/images/) consists of hundreds of images taken from a fixed perspective at a location and a mask image denoting the sky pixels in white and other areas of the image in black. The data is downloaded and stored as:-
```bash
├── 1093
│   ├── 1093_mask.png
│   ├── 20140418_215418.jpg
│   ├── 20140419_002403.jpg
│   └── .....
├── 10066
│   ├── 10066_mask.png
│   ├── 20130101_084634.jpg
│   ├── 20130101_091628.jpg
│   └── .....
├── ....
├── SkyPixel.ipynb
├── SkyPixelPredict.ipynb
└── skyPixelModel.h5
```
\
The images were trained after scaling down the resolution to 240 * 240 pixels. The predicted mask image will also be in the same resolution.
\
A sample test on the trained model:-
\
![original image](test_img.jpg?raw=true "test_img.jpg")
\
\
![Generated mask](test_mask.png?raw=true "test_mask.png")


