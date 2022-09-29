# Lab 1: Introduction to OpenCV Basics and Pixels

> We run our labs with [Python 3.6+](https://www.python.org/downloads/).
> For Windows, you might want to use [Conda](https://www.anaconda.com/products/distribution). 

## What is OpenCV?
- OpenCV is a library framework for developing computer vision solutions. 
- It is widely used in industry and research.
- It is (mainly) free for both academic and commercial use.
- It has C++, C, Python and Java interfaces and supports Linux, Windows, Mac OS, iOS and Android.
- OpenCV is designed for computational efficiency and with a strong focus on real-time applications.

## Objectives of the First Lab Session!
1. Your first task is to setup [OpenCV](https://github.com/opencv/opencv-python) on the lab machines or your own machine. We use Python throughout all labs.
2. Start familiarising yourselves with the basics of OpenCV, such that after the lab you should be able to compile and run OpenCV programs, to create, draw into, load, save and display images, and to manipulate pixels.
3. Get familiar with basic representation of the image: pixels, channels, and colours

## Setting up OpenCV
1. Open a terminal and create virtual environment: `$ python -m venv myproject`, or `conda create -n myproject`
2. Activate your environment: `$ source myproject/bin/activate`, or `conda activate pytorch-env`
3. Then it shows: `(myproject) [username@it0number ~]$`
4. Might need to update pip: `$ pip install --upgrade pip`
5. Install OpenCV packages: `$ pip install numpy opencv-python`, or `conda install numpy` then `conda install -c menpo opencv`
6. To get out from the environment (when you finish your work): `$ deactivate`, or `conda deactivate`

## Task 1: HelloOpenCV program 
Study `hello.py` and run it using `python hello.py`.

## Task 2: Load, display, create, draw and save the image
Try to understand pixel representation in the image
- `display.py` to load and display an image
- `draw.py` to create, draw and save
- `pixels.py` to access and set pixel values

# Pixel Manipulation and Thresholding

## Task 3: Implementing Thresholding
- Now that you are able to handle images, your next task is to write an OpenCV-based program that loads the `mandrill.jpg` greyscale image and that, pixel by pixel, sets all pixels above a certain value (maybe start with 128) to white (255) and all pixels equal or below the value to black (0).
- Experiment with different thresholding values and examine the resulting images. Can you highlight certain parts of the face (e.g. the nose, the eyes) with one or more specific thresholds?
- Compare your results to the output of the inbuilt OpenCV function `threshold`.

