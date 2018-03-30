# ClickCoordinatesTool physycom mod

This repository contains a mod of the standard `ClickCoordinatesTool` macro from ImageJ, better suited for our image annotation requirements.

## Description

[ImageJ](https://github.com/imagej/imagej) is a popular open source image processing program designed for scientific multidimensional images. It already includes a macro for image annotation, which does not scale well for bigger pictures and crowd-counting. We slightly modified it with this very simple snippet:

```cpp
  setLineWidth(3);
  setColor(0,255,0);
  tickLength = 9;
```

so that green crosses are drawn for each click and they are bigger than the default size (otherwise the crosses were undetectable on 16+ MP photos).

## Installation

This macro requires a valid installation of an `ImageJ` distribution. There are many of them, including our preferred, which is called [Fiji](https://imagej.net/Fiji/Downloads) (whose meaning is a recursive acronym: Fiji is just imagej). Download it from [its website](https://imagej.net/Fiji/Downloads). In case you choose a *non-JRE* version, you have to provide a valid java installation to the software.

Many of these distributions already include a basic `ClickCoordinatesTool.txt` macro, which is **not** suitable for our requirements! So please use our tool instead, downloading this file to your computer: [`ClickCoordinatesTool.txt`](https://raw.githubusercontent.com/physycom/image-annotator/master/ClickCoordinatesTool.txt) (right click on the link and select `Save link as...`)

## Usage

To annotate a picture follow this procedure:

1. Open your ImageJ software
1. Click on `File`, then `Open` and select an image on your computer
1. Click on `Plugins`, then `Macros`, then `Install...` and then double click on the file `ClickCoordinatesTool.txt` (our version!) which you downloaded previously
1. Click on **each and every** person you **can distinguish** in the picture. This is the most important step and you should devote enough time to it. **Do not** click on an item if you are not sure it is a person, and please put the crossmark precisely on the people's heads.
1. In case you need to zoom in/out of the picture, please use the `+` and `-` keys on your keyboard.
1. In case you put a cross by mistake, please follow this other step accurately: go to `Edit` and then `Undo` into the image window and inside the Results window select the last entry and remove it going to `Edit` and then `Cut`.
1. At the end of the annotation, save the picture going to `File`, `Save as`, `Jpeg...` and then giving it a name like the original but with `_ann` appended to it. You also have to save the Results, going to the Results window and saving it through `File`, `Save as` and then giving it a name which is the original name but with `_count` appended to it. Example: from a given `image.jpg` you should obtain `image_ann.jpg` and `image_count.xls`
