# Faceswap

This is the code forked form [here](https://github.com/matthewearl/faceswap)


## origin README.md

This is the code behind the [Switching Eds blog post](http://matthewearl.github.io/2015/07/28/switching-eds-with-python/).

See the link for an explanation of the code.

To run the script you'll need to install dlib (http://dlib.net) including its
Python bindings, and OpenCV. You'll also need to obtain the trained model [from
sourceforge](http://sourceforge.net/projects/dclib/files/dlib/v18.10/shape_predictor_68_face_landmarks.dat.bz2).

Unzip with `bunzip2` and change `PREDICTOR_PATH` to refer to this file. The
script is run like so:

    ./faceswap.py <head image> <face image>

If successful, a file `output.jpg` will be produced with the facial features
from `<head image>` replaced with the facial features from `<face image>`.

## README

### Requirements
* [pretrained model](https://sourceforge.net/projects/dclib/files/dlib/v18.10/shape_predictor_68_face_landmarks.dat.bz2/download)
* opencv
* dlib

### install for linux
Make sure you have `cmake` ,`cblas` ,`lapack`, `blas` before you install `dlib`. Or you may encounter `ImportError`


if you use pipenv, you can just run

```
pipenv install --dev
````

to install `opencv` and `dlib`

change the path of PREDICTOR_PATH to where you put your pretrained model download from previous url

### Usage

```
./faceswap.py <head image> <face image>
```

### Details
* set PREDICTOR_PATH as absolute path may encounter cannot open error
* There should be one and only one face in each image