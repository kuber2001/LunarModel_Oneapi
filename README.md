# LunarModel_Oneapi

This Model was constucted by me and other team members including Akanksha Bansal, Nehal Sahukar and Aditya Kumar choubey of my team, for the Intel OneAPI Hackathon. 
It contains code for the constructed model of object detection using OpenCV library and Convolutional networks. The model is designed to recognise the big rocks present on the surface of the moon so that it can help the rover to navigate using its sensors.
The model is developed using U-Net architecture and OpenCV library.

# Introduction

The model is using instance segmentaion to classify the images into 4 classes of sky, ground, small rocks and big rocks denoted by grey, black, deep grey and white respectively. Further information about the Unet architecture can be viewed at :- "https://towardsdatascience.com/unet-line-by-line-explanation-9b191c76baf5"

The model can be optimized using parallel processing libraries or Intel Open Vino Toolkit, which we shall try to update soon.

# Description

Our project lunar api as established in the documentation uses Segmentation model that is developed using CNN in a U-net Architecture. As a result based on the huge dataset we are training the model on, it requires optimization. 
The average time for training of the model was approx. 50 mins to 1 hr in our local systems. Moreover in some local system it failed to execute at all. In comes the oneapi, using the devcloud access provided to us by Shriram Vasudevan sir and with the guidance of other mentors such as Arun, Akshay and Joel, we learnt how to migrate our code to devcloud and use the Intel Analytics toolkit.
The most prominent of them all, was onednn, which was optimized in tensorflow 11.0 version to get the required training output in mere 35 mins. It boosted the speed significantly, additionally we are trying to use openvino toolkit to make it more faster and perhaps reducing the training time to 20 mins.

# TechStack

- Python


## Run Locally

### To construct model

Clone the project

```bash
  git clone https://github.com/Demogorgon24242/LunarModel_Oneapi.git
```

* Go to the project directory
* Download the dataset using kaggle api or website and provide proper path details
* Execute all the cells

## Run on Intel Devcloud

1) go to the website "https://devcloud.intel.com/oneapi/get_started/"
2) Register for the intel Devcloud 
3) Launch with JupyterLab Notebook and follow the video "https://youtu.be/Cz32tlMs78c" to install additional libraries
  (if not working then open the console and use "git clone -b 2023.0.0 https://github.com/oneapi-src/oneAPI-samples.git" in terminal and cd oneapi_samples )
4) In order to download the dataset in intel devcloud using kaggle
    * open a new terminal using the add console button
    * create a new directory using "mkdir .kaggle" 
    * upload the kaggle.json file in the intel devcloud profile downloaded from the kaggle profile 
    * cp kaggle.json .kaggle
    * then go to notebook and execute the command "pip install kaggle"
    * Execute the command "kaggle -d (link of kaggle)"
5) Make the necessary changes to the path of the directories in the notebook
6) Finally create a notebook and upload the above notebook to run and execute the cells

## To run the Django Server with the pretrained model on local server

1) Download both the folders and place them in the new folder say Lunar11
2) open terminal at Lunar11 and type ".\myproject\Scripts\activate"
3) Execute "cd LunarRockSeg"
4) Execute "python manage.py runserver"
5) Click on the local https link and run the model

There is a demonstration video available on the link :- "https://youtu.be/1RoidkvrFAM"

P.S. Ignore the quality degradation of the video and mail us for any queries


## Note :- This is for testing only not for deployment
