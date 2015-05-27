# Image Encoding

## Description

Create a program to store a copy of itself (a Quine) as a bitmapped image.

## Objectives

### Learning Objectives

After completing this assignment, you should understand:

* Code Evaluation
* Pixel Manipulation with PIL
* Quine

### Performance Objectives

After completing this assignment, you should be able to:

* Understand how to programatically generate images with Python

## Details

### Deliverables

* A Git repo called image-encoding containing at least:
  * `README.md` file explaining how to run your project
  * a module called `image-encoding`
  * tests for `image-encoding`
  * a file called `documentation.txt` that describes in detail your encoding method

### Requirements

* Passing unit tests
* No PEP8 or Pyflakes warnings or errors
* Usage of Pillow (a maintained fork of PIL)

## Normal Mode

Create a Quine that can store a version of itself in a bitmapped image.

For each pixel you must store a red, green, and blue value that is an encoded representation of a small portion
of the program creating the image.

Writing the pixel values is trivial and can be accomplished with the following snippet. (see below)

```python
from PIL import Image

img = Image.new( 'RGB', (255,255), "black")
pixels = img.load()

for i in range(img.size[0]):
    for j in range(img.size[1]):
        pixels[i,j] = (i, j, 100)

img.show()
```

Your documentation should describe in detail how you encoded your data for storage inside of the image.

## Hard Mode

In addition to the requirements from **Normal Mode**:

* Create a program called `image_reader.py` that can read your `image.bmp` encoded file and print the body of the
python program to the console.

## Notes

The nature of this assignment means that with a slight change in your implementation you should expect a slightly different
resulting image.  Be very careful about hardcoding ANY values.

## Reading

[Quine](http://en.wikipedia.org/wiki/Quine_%28computing%29)
[Python Imaging Library/Editing Pixels](http://en.wikibooks.org/wiki/Python_Imaging_Library/Editing_Pixels)
