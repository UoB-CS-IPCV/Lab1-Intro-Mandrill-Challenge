# Lab 1: Introduction to OpenCV and the Mandrill Challenge

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

## Using the lab sheet

There are two ways to use the lab sheet, you can either:

- [create a new repo from this template](https://github.com/UoB-CS-IPCV/Lab1-intro-mandrill-challenge/generate) - **this is the recommended way**
- download a [zip file](https://github.com/UoB-CS-IPCV/Lab1-intro-mandrill-challenge/archive/master.zip)

## Task 1: HelloOpenCV program 
Study `hello.py` and run it using `python hello.py`.
<details>
    <summary>Hint</summary>
<img src="https://github.com/UoB-CS-IPCV/Lab1-intro-mandrill-challenge/blob/main/hint/helloOpenCV.png" height=200>
</details>

## Task 2: Load, display, create, draw and save the image
Try to understand pixel representation in the image
- `display.py` to load and display an image
- `draw.py` to create, draw and save
- `pixels.py` to access and set pixel values
<details>
    <summary>Hint</summary>
<img src="https://github.com/UoB-CS-IPCV/Lab1-intro-mandrill-challenge/blob/main/hint/draw.png" height=200> <img src="https://github.com/UoB-CS-IPCV/Lab1-intro-mandrill-challenge/blob/main/hint/pixels.png" height=200>
</details>

# Pixel Manipulation and Thresholding

## Task 3: Implementing Thresholding
- Now that you are able to handle images, your next task is to write an OpenCV-based program that loads the `mandrill.jpg` greyscale image and that, pixel by pixel, sets all pixels above a certain value (maybe start with 128) to white (255) and all pixels equal or below the value to black (0).
- Experiment with different thresholding values and examine the resulting images. Can you highlight certain parts of the face (e.g. the nose, the eyes) with one or more specific thresholds?
- Compare your results to the output of the inbuilt OpenCV function `threshold`.
<details>
    <summary>Hint</summary>
Sample answers are available at `thr.py` if you are stuck.
</details>

## Task 4: Thresholding Colour Images
- Whilst in greyscale images the brightness of a pixel is usually represented as a single byte in 2D array, colour images use three bytes to store information for one pixel, become 3D array. Bytes represent the BLUE, GREEN and RED channel in this order. 
- Now, try to implement thresholding of the red, green and/or blue channels to highlight facial components in mandrillRGB.jpg, which now contains colour information.
- Also check the OpenCV function `inRange`.
<details>
    <summary>Hint</summary>
Sample answers are available at `colourthr.py` if you are stuck.
</details>

# Representation Basics – Pixels, Colours & Channels

## Task 5: Help mandrill
Your task is to recover as much of the original mandrill colour image (3 channels, 8 bits per channel) from corrupted images, `mandrill0.jpg`, `mandrill1.jpg`, `mandrill2.jpg` and `mandrill3.jpg`.

1. View the corrupted images and, for each image, make a prediction of what has happened to it. Maybe look at individual colour channels or histograms to investigate your hypothesis.
2. Write a small OpenCV program for each image which can reconstruct the original mandrill colour image from it as well as possible.

Some images cannot be fully reconstructed.

- Original mandrill `mandrillRGB.jpg`

<img src="https://github.com/UoB-CS-IPCV/Lab1-intro-mandrill-challenge/blob/main/mandrillRGB.jpg" height=200> 

- Corrupted images, `mandrill0.jpg`, `mandrill1.jpg`, `mandrill2.jpg` and `mandrill3.jpg`

<img src="https://github.com/UoB-CS-IPCV/Lab1-intro-mandrill-challenge/blob/main/mandrill0.jpg" height=200> <img src="https://github.com/UoB-CS-IPCV/Lab1-intro-mandrill-challenge/blob/main/mandrill1.jpg" height=200> <img src="https://github.com/UoB-CS-IPCV/Lab1-intro-mandrill-challenge/blob/main/mandrill2.jpg" height=200> <img src="https://github.com/UoB-CS-IPCV/Lab1-intro-mandrill-challenge/blob/main/mandrill3.jpg" height=200>


