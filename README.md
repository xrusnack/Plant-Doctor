# Plant Disease Classification Project

## Dataset 
The dataset contains a total of 54 000 examples of 38 classes (10 healthy, 28 affected) over 14 crop species.

Available here: https://github.com/spMohanty/PlantVillage-Dataset 

## Methods
The repository contains jupyter notebook documenting the dataset preparation and model training.
We’ve fine-tuned two vgg19 models on two versions of the dataset: original rgb images and their segmented
versions, and additionaly created an ensemble model. 

The best-performing model was vgg19 fine-tuned on the original versions of the images (not segmented) achieving 92.83% accuracy.

## Gradio App
A simple app enabling an easy usage of the model's predicions available at: https://vojtam-plantdoctors.hf.space/

