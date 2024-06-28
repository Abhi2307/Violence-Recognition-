INTRODUCTION:

Automatic detection of violence in videos, whether involving individuals or crowds, attracts significant attention. This study introduces an end-to-end deep neural network designed specifically for identifying violence in video content. The proposed model leverages a pre-trained MobileNet from ImageNet to extract spatial features, supplemented by a Time Distributed layer and Gated Recurrent Units (GRU) for temporal feature extraction. This architecture enables the model to capture meaningful actions from both individual frames and sequences. Classification is performed using a series of fully connected layers. The model achieves an accuracy close to the current state-of-the-art. Fine-tuning is conducted on Real-Life Violence Situations, a dataset comprising 2000 short videos categorized into 1000 violence and 1000 non-violence instances, resulting in the highest accuracy recorded at 97.0%.

PROJECT DESCRIPTION :

The Goal of the project is to classify real-life videos into Violence and Non-Violence categories. This prediction can be used combined with CCTV cameras to alert police regarding the Violence and stop the violence. This can be used along with facial recognition to identify people involved in Violence.

DATASET :

The dataset "real-life-violence-situations-dataset" is taken from Kaggle competition. The Dataset Contains 1000 Violence and 1000 non-violence videos collected from youtube videos, violence videos in the dataset contain many real street fights situations in several environments and conditions. Non-Violence videos from the dataset are collected from many different human actions like sports, eating, walking …etc.

Preprocessing:

Frames are sampled from each video using Keras' VideoFrameGenerator, ensuring uniform extraction throughout the video duration. These frames provide the basis for feature extraction, employed alongside a Time Distributed layer and GRU to capture dynamic actions.

Data Augmentation:

To mitigate overfitting caused by the limited dataset of 2000 images, the VideoFrameGenerator can be complemented with Keras' ImageDataGenerator for data augmentation. This approach enhances the dataset size by generating varied transformations of existing frames.

Accuracies Achieved After Training Models Using Different Methods:

VGGNet: 92.81%
GoogleNet: 93.0%
ResNet: 96.79%
MobileNet: 97.0%
Conclusion:

The highest accuracy of 97.0% was achieved by fine-tuning the top 9 layers of the MobileNet model, integrating a time distributed layer with a GRU layer, and extracting 6 frames per video.
