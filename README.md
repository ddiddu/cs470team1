# Mask Verification

This is the project named Mask Verification by Team 1 in CS470 class.

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
    ├── Code                                                    # Contain all models
       ├── face_mask_detection_CNN                              # CNN model for verify with mask/ without mask, correct mask/ incorrect mask
       ├── face_preprocessing                                   # Pre-trained model for face preprocessing and test file
       ├── linear_regression                                    # for keypoint detection and linear regression in report 2.b.i.
       ├── Extract_clothes_color_keypoint_test.ipynb            # Pose estimation and Extracting color code test
       ├── face_recognition_test.ipynb                          # test the face recognition for linear regression
       └── mask_verification.ipynb                              # Overall step for mask verification
    ├── dataset_new                                             # 
    ├── dataset_synthetic                                       # dataset made with a synthetic image of a mask on people's faces, includes correctly/incorrectly weared mask image.
    ├── demo                                                    # demo video and gif 
    ├── output                                                  # other test output video and gif
    └── README.md                                               # ReadMe
 
### Dataset Link

We attach the dataset link because of the size

> [dataset_new](https://drive.google.com/drive/folders/1AnYcCi4T8itP_FeezB3idte4wExbyfsv?usp=sharing)
>
> [dataset_synthetic](https://drive.google.com/drive/folders/1PrsfmC3AmG8uguJ6qNfVfQeaRTQNxSXH?usp=sharing)
>
> [demo](https://drive.google.com/drive/folders/1PszHdBOKmlFfmP06AeyT97JBAhTnVpfm?usp=sharing)
>
> [output](https://drive.google.com/drive/folders/1ae7mBPWKeLFmBNWJ-0zfpKu2PdiG9TdB?usp=sharing)

## Result

### Face Recognition & Face Preprocessing

We want to mark the face in our model application image. Correct results were obtained from facial area extraction to mask area extraction.

<img src="https://drive.google.com/uc?export=view&id=1XHjKrnt2ngbORXSFp99b_Cb4__fyG4QT" height="200">

### Two CNN Model(Mask Verification)(Class 2*2)

Classifying with mask and without mask CNN model loss was 0.040 and accuracy was 0.991. 

Classifying incorrect mask and without mask CNN model loss was 0.104  and accuracy was 0.989.

When tested with our new datasets, it successfully classified with correct mask, incorrect mask and without mask.

<img src="https://drive.google.com/uc?export=view&id=1GNghsfmsDIpFYKL5Noi9548S33xdUIlu" height="250"> <img src="https://drive.google.com/uc?export=view&id=1GQrK8Mran1_DotuF_dVadbqOKlRv5Y7W" height="250"> <img src="https://drive.google.com/uc?export=view&id=1GWfoCOKp4c4AW-nCyP3PW5bOeRWot9nL" height="250">

### Extracting Color of Clothes

When there is no mask or incorrect mask on a human's face, we made a notification with the clothes color text. 

<img src="https://drive.google.com/uc?export=view&id=1x3hcLB9P7vkfIPOoAZArAK3oAM39f3Rc" height="300">


## Conclusion

For mask verification, first we detect humans in the image and then detect a face in each cropped person's images. After the Pre-processing of face image, this is used to the input image of our two CNN models for verifying their mask wearing. If the model finds that someone wears a mask incorrectly, we express the color of clothes of the person to alert the warning to wear the mask correctly. 

If the system becomes available in real time, our system will be able to identify and alert people's characteristics who don't wear masks correctly in real time. The characteristic that we used in this project was the color of the clothes, and we thought we could also use the patterns or kind of clothes.

## Reference

> Lee S.H. (2020) Deep learning based face mask recognition for access control. Journal of the Korea Academia-Industrial cooperation Society, 21(8), 395~400
