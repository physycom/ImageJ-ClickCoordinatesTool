# Image Annotator

This repository contains the instruction to set up an image annotator for CV purposes.

## Requirements and installation

This tool is based on `ImageJ`, which requires a java environment to run. If you are not sure about it, please install it from the [official website](https://www.java.com/it/download/).

1. Download `ImageJ` from [here](https://imagej.nih.gov/ij/download.html)
1. Unzip the content of the archive
1. Append the code contained in `ClickCoordinatesTool.txt` to this file: `ImageJ\macros\StartUpMacros.txt`. To do it, open both files with your preferred text editor and copy/paste the text from the first at the end of the second file.
1. Run `ImageJ` (a double click on it should be enough on most systems)!

## Usage

With `ImageJ` opened, to annotate a picture follow this procedure:

1. Click on `File`, then `Open` and select an image on your computer
1. Click on the third-last button, which is identifiable as a star
1. Click on **each and every** person you can identify in the picture. This is the most important step and you should devote enough time to it. **DO NOT** click on an item if you are not sure it is a person, and please put the crossmark precisely on the people's heads.
1. In case you put a cross by mistake, please follow this other step accurately: go to `Edit` and then `Undo` into the image window and inside the Results window select the last entry and remove it going to `Edit` and then `Cut`.
1. At the end of the annotation, save the picture going to `File`, `Save as`, `Jpeg...` and then giving it a name like the original but with `_ann` appended to it. You also have to save the Results, going to the Results window and saving it through `File`, `Save as` and then giving it a name which is the original name but with `_count` appended to it. Example: from a given `image.jpg` you should obtain `image_ann.jpg` and `image_count.xls`

## Acknowledgements

Thanks to Flavio Bertini that pointed me to this tool.
