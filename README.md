<!-- PROJECT LOGO -->
<br />
<p align="center">
  <img src="Final Project Submission/images/sss.jpeg" alt="Logo" width="250" height="250">
</p>


<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#dependencies">Dependencies</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#authors">Authors</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

This project focuses on detecting handwritten (one or more) digit(s) created by... surprise surprise... 'hand', with love, from our own EEL5840/EEL4773 course students. To start with, we had 4190 images and the corrosponding labels.

<!-- GETTING STARTED -->
## Getting Started

This Git Repo contains the following files:  
yolov8.pt - The YOLO model from the Ultralytics library  
train.py - The training script which can be used to train the YOLOv8 model.  
test.py - The test script which can be ran to test the unseen data and calculate IoU and mAP metrics  
Results folder - Folder with results of our training on given training data  
weights - folder containing weights -> best.pt file which has to be loaded before running the predictions on the test data.  
data.yaml - Used data.yaml file to showcase how it needs to be structured  
Report - Project Report

### Dependencies

To use the 'torchmetrics' package for evaluating preformance metrices, we need to install 'torchmetrics'.  
!pip install torchmetrics should do the job.

<!-- USAGE EXAMPLES -->
## Usage
##### For Training
The first action required is to download the yolov8.pt file in the current working directory so that it is accessible.  
YOLO requires a specific directory structure in order to train the model on custom dataset. It needs a 'train' and a 'valid' folder and inside each of the folders, there should be 'images' and 'labels' folders containing the images and labels files with same name. It is important to note that the folder names must be kept as instructed, else the model will run into errors.  
The folder structure is specified in the .yaml file, which also resides in the present working directory.  
For example, my .yaml file cotans the following information:  
  
""  
train: /blue/eel5840/b.gandhi/Final Project/datasets/train/images  
val: /blue/eel5840/b.gandhi/Final Project/datasets/valid/images

nc: 10  
names: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]  
""  
After the training, a folder named 'runs' will be created which will contain the results and predictions of any subsequent runs.  
  
#### For Testing
For testing, the provided 'best.pt' file can be used to load the model weights, as instructed in the 'test.ipynb' notebook. It is also important to load the test images and labels in the respective variables created for them in the notebook. After this step, the subsequent cells can be ran and the model will predict the labels and coordinates for the test images and save them in the 'runs/' folder. The IoU and mAP scores can be generated using the provided functions in the 'test.ipynb' notebook.


<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.


<!-- Authors -->
## Authors

Bharat Gandhi - b.gandhi@ufl.edu  
Yongkyoon Park - yo.park@ufl.edu  
Nicholas Vasconcellos - nicholas.silyvas@ufl.edu

Project Link: https://github.com/UF-EEL5840-EEE4773-Fall-2024/final-project-code-report-samba-spice-and-seoul.git


<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements

* [Catia Silva] - Our Amazing Instructor
* [Dhruv Kushwaha] - Our Cool Supervised Teacher
* [Spencer Chang] - Our Wizard of FML
* [Joseph Conroy] - Our Fire Fighter  

and the complete FML Fall'24 Team at UF

## Thank you
