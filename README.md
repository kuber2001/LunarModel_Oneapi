# LunarModel_Oneapi

This Model was constucted by me and other team members including Akanksha Bansal, Nehal Sahukar and Kuber Vajpayee of my team, for the Intel OneAPI Hackathon. 
It contains code for the constructed model of object detection using OpenCV library and Convolutional networks. The model is designed to recognise the big rocks present on the surface of the moon so that it can help the rover to navigate using its sensors.
The model is developed using U-Net architecture and OpenCV library.

# Introduction

The model is using instance segmentaion to classify the images into 4 classes of sky, ground, small rocks and big rocks denoted by grey, black, deep grey and white respectively. Further information about the Unet architecture can be viewed at :- "https://towardsdatascience.com/unet-line-by-line-explanation-9b191c76baf5"

The model can be optimized using parallel processing libraries or Intel Open Vino Toolkit, which we shall try to update soon.


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



## Note :- This is for testing only not for deployment
