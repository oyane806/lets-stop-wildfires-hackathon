# Let's Stop Wildfires Hackathon

You can find more information on **let's stop wildfires hackathon** in the official [repo]( https://github.com/aiformankind/lets-stop-wildfires-hackathon).

I built a few notebooks in google colab. Feel free to use it, comment it or improve it!

## 1. Hackathon preparation

#### :one: First challenge
The first task is to build a classifier to separate images with smoke and images without smoke.

:point_right: For the moment, I have around 0.142857 error_rate using a simple resnet30 after a lot of epochs.

#### :two: Second challenge
The second task is almost the same: to build a classifier to separate images with smoke and images without smoke. Images are pieces of the images used in the first challenge.

:point_right: The classifier is faster to train. After a few epochs, the error_rate is around 0.066207.

#### :three: Third challenge
Given a sequence of images, the task is to detect the fire as early as possible.

## 2. Hackathon

The goal of this hackathon is:
- decrease the number of false positive
- detect fire as early as posssible

We found out three ideas to try that take into account a sequence of 2 images as an output of a CNN.

First, we need to build a dataset. The hackathon organizers provided us a dataset of 23 sequences of images. Because this is not a lot of data, we are building a new dataset consisting of a combination of two images.

Rules used to build the new dataset:
- no_smoke(t) + no_smoke(t+1) = no_smoke
- no_smoke(t) + smoke(t+1) = smoke
- smoke(t) + smoke(t+1) = smoke
- no_smoke(t) + smoke_(t+2) = smoke

You can find the new dataset with differences [here](https://drive.google.com/open?id=1qrPpc37hXSDLz8JOZbnTLiMEktxjYHk0)

#### :one: 2 images difference

##### To do list

- [x] List all the images we have and label them in a csv file (mapping.csv) -- Oceane
- [x] Write in a csv file all the combination of images to build our dataset (see above rules) -- Oceane Jared
- [x] Build our new dataset -- Oceane [new dataset](https://drive.google.com/open?id=1qrPpc37hXSDLz8JOZbnTLiMEktxjYHk0)
- [x] Write a function to calculate the difference of two image -- Oceane
- [ ] Create a validation set
- [ ] Write a script to split a picture into 81 pictures (for production)

#### :two: 2 images stacking

#### :three: CNN then neural network



## Team