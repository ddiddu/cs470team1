# Mask Verification

## Introduction

Due to the spread of COVID-19, social distancing has begun around the world, and masks have become mandatory in public places. 

In any given situation, if we see a video and find people who have not properly worn a mask, the final goal is to extract the person's features (such as the color of the clothes) and to give alert. The goal of this project is to reduce the burden of reporting and to provide continuous attention to properly wearing masks by directly issuing warnings. 

## Overall Method

To observe the people wearing a mask in the crowd, our AI should do object detection. For the step of our project is (1) human detection, (2) face detection, (4) Clothes Color Extraction. 
For the step of (3) mask confirmation, we will apply image classification with CNN for 3 classes, no-mask, correct-mask, and incorrect-mask. We tried to produce and experiment with various possible models to select the most suitable and accurate models for our project.
If our model determines that someone did not wear the mask properly in the (3) Mask Verification above, extract the person's color of clothes for a system that alerts the person's features during the "(4) Clothes Color Extraction" step.

<img src="https://drive.google.com/uc?export=view&id=11Tmwxxs2lXcjo4xAIo9wvnpPLXSJd20d" height="300">

## File Structure

    .
    ├── Code                                                    # 
       ├── face_mask_detection_CNN                              # CNN model for verify with mask/ without mask, correct mask/ incorrect mask
       ├── face_preprocessing                                   # 
       ├── linear_regression                                    # 
       ├── Extract_clothes_color_keypoint_test.ipynb            # 
       ├── face_recognition_test.ipynb                          # 
       └── mask_verification.ipynb                              # Overall step for mask verification
    ├── dataset_new                                             # 
    ├── dataset_synthetic                                       # 
    ├── demo                                                    #
    ├── output                                                  # 
    └── README.md                                               # 
 
 
