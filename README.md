<!-- PROJECT LOGO -->
<br />
<p align="center">
  <img src="images/sss.jpeg" alt="Logo" width="250" height="250">
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
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#authors">Authors</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

This project focuses on detecting handwritten (one or more) digit(s). To start with, we had 4190 images and the corrosponding labels. Image augmentation was done and every image was rotated by 90, 180, and 270 degrees to get 3 copies, and the total training set contained close to 14000 images and labels. The YOLOv8 model was fine tuned and trained on these images and labels, carrying out transfer learning.

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

<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements

* [Catia Silva] - Our Amazing Instructor
* [Dhruv Kushwaha] - Our Cool Supervised Teacher
* [Spencer Chang] - Our Wizard of FML
* [Joseph Conroy] - Our Fire Fighter  

## Thank you
