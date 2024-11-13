# Image-Fusion-for-Enhanced-Shape-Classification
 ## Introduction
 In this task, a low and high level fusion strategy is used to improve the classification
 performance of a synthetic dataset. The 1000 instances in the dataset each have three
 32x32 images that represent one of the four geometric shapes (pentagon, circle, square, or
 triangle). Three distinct background types—gradient, noise, and spotlight—are used to
 create the images. To classify these shapes, a convolutional neural network called LeNet
 5 is implemented. To compare performance improvements, 3 LeNet5 models are trained
 and evaluated on the images without fusion at first and then another LeNet5 model is
 trained and evaluated on fused image dataset obtained from the defined fusion strategy.
 Finally the increased accuracy of the CNN model is achieved for the shape classification
 task. At the end confusion matrices are plot to demonstrate these accuracies.

 Dataset Overview :

 
  Image 1 - Gradient background 
 
  
  Image 2 - Noise background 
  
  
  Image 3 - Spotlight background




 ##  Step 1: Change LeNet5 Architecture
![image](https://github.com/user-attachments/assets/57dac9e6-c8c1-46bb-8fbb-589060cbbafe)

 
## Step 2: Train and Evaluate LeNet without Fusion 
1. Dataset Preparation:


2. Training 


3. Evaluation 
![image](https://github.com/user-attachments/assets/f0c99e68-7764-4257-bb52-36b4b6d5aec7)



## Step 3: Implementing fusion Strategy
1. Low-Level Fusion:


a.Pixel-based Average Fusion: It involves directly combining the pixel values of the three images and take average value to create a new, fused image.


b. Pixel-based Maximum Fusion: It involves directly combining the pixel values of the three images and take maximum value to create a new, fused image.


c. Pixel-based Minimum Fusion: It involves directly combining the pixel values of the three images and take minimum value to create a new, fused image.


![image](https://github.com/user-attachments/assets/c77a6c23-3213-4b3c-ba10-bbabe200ef7f)


2.High Level Fusion :
• Majority Voting : Among all four models, the final classification is decided by majority vote. In this method, the predicted class that receives the most votes from the individual models is selected as the final prediction.            


## Results 
![image](https://github.com/user-attachments/assets/3eb2656c-cc2a-4cc7-b1ba-d76375de7468)

 
