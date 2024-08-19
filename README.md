
The original repositry is private due to confidentiality agreements.
# PalmVein-identification
# The General Idea
Palmvein recognition is a biometric authentication method that utilizes the unique vascular patterns in the human palm. Unlike fingerprints, palm vein patterns are more complex and are located beneath the skin, making them less prone to forgery.
![image](https://github.com/user-attachments/assets/779e3f56-e210-4077-b066-fc4acce03a66)

The primary objective of this project is to develop a robust palmvein recognition system that can identify individuals based on the unique vein patterns in their palms. This system has potential applications in security, access control, and identity verification.
# preprocessing
used U^2net to remove the background

![0f112ed8-d937-4c2b-8e1e-a0b178a74a58](https://github.com/user-attachments/assets/851fea87-2f80-43b8-9602-cd2dea2e88ff)

used mediapipe to extract the palm part an applied some filters like gabor filter then extracted the vein skeleton

![40e6c991-e50e-423f-a0df-e80bfb5954c6](https://github.com/user-attachments/assets/4aeb1815-13e5-4ec2-8834-ae820f7d8878)

# Model Architecture

![354240800-a1896e33-3049-482a-bdc2-a5cc49eb436f](https://github.com/user-attachments/assets/31e9ab5a-171a-407e-b6ea-2183a33e3934)

A Convolutional Neural Network (CNN) based on ResNet18 was utilized for feature extraction. This architecture was chosen for its proven effectiveness in handling complex image data. For the identification process, an incremental classifier (SGD) was employed. This approach allows for continuous learning, making the model adaptable to new data without the need for retraining from scratch.

# Evaluation

![image](https://github.com/user-attachments/assets/d63a2331-65f4-48e3-a44e-c248a8a9f36b)

Achieving 1 Precision and 0.97 accuracy even on an other bigger test dataset

# Deploying the model on a mobile app

the deployment was done by saving the model as tflite file and the classifier as pickle and then integrating it in a kivy mobile app that i created to test it on our Raspberry pi 4 with the special hardware ( NOIR Camera, near infrared leds...)

here is a llittle demo of the apps on my pc without the special hardware.
**Identification App**

https://github.com/user-attachments/assets/2a683ba2-711b-4683-9de1-7a594ec9e2d4

**Administration App**


https://github.com/user-attachments/assets/b58047c8-8de7-4240-86ba-d85f2862bac7

**After updating the classifier**


https://github.com/user-attachments/assets/8f59d4da-78a8-40ec-abc3-c6afb56b4b72


