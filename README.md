# Plant Disease Classification Project

This project is concerned with training deep learning models to identify plant diseases from leaf images.

## Dataset 
The dataset contains a total of 54 000 examples of 38 classes (10 healthy, 28 affected) over 14 crop species.

Available here: https://github.com/spMohanty/PlantVillage-Dataset 

## Gradio App
A simple app enabling an easy usage of the model's predicions available at: https://huggingface.co/spaces/xrusnack/plant_doctor

## Methods
The repository contains jupyter notebook documenting the dataset preparation and model training.
We’ve fine-tuned two vgg19 models on two versions of the dataset: original rgb images and their segmented
versions, and additionaly created an ensemble model. 

The best-performing model was vgg19 fine-tuned on the original versions of the images (not segmented) achieving 92.83% accuracy.

### Model comparison
| Model | Precision | Recall | F1 Score | Accuracy |
| --- | --- | --- | --- | --- |
| vgg19_original | 0.90 | 0.93 | 0.91 | 0.93 |
| vgg19_SEG | 0.88 | 0.91 | 0.89 | 0.91 |
| ensemble | 0.88 | 0.91 | 0.90 | 0.91 |

#### Class-wise results of the performance of the best model:
| Class | Precision | Recall | F1-Score | Support |
| --- | --- | --- | --- | --- |
| Tomato__Late_blight | 0.89 | 0.72 | 0.80 | 385 |
| Tomato__Tomato_Yellow_Leaf_Curl_Virus | 0.98 | 0.95 | 0.96 | 1087 |
| Peach__healthy | 0.84 | 0.98 | 0.90 | 86 |
| Grape__Esca_(Black_Measles) | 0.94 | 0.94 | 0.94 | 261 |
| Potato__Late_blight | 0.91 | 0.89 | 0.90 | 205 |
| Pepper,_bell__Bacterial_spot | 0.88 | 0.95 | 0.91 | 191 |
| Strawberry__healthy | 0.98 | 1.0 | 0.99 | 88 |
| Orange__Haunglongbing_(Citrus_greening) | 0.99 | 0.99 | 0.99 | 1112 |
| Tomato__Leaf_Mold | 0.70 | 0.88 | 0.78 | 176 |
| Apple__Black_rot | 0.88 | 0.97 | 0.93 | 140 |
| Strawberry__Leaf_scorch | 0.97 | 0.99 | 0.98 | 218 |
| Tomato__Early_blight | 0.68 | 0.67 | 0.67 | 204 |
| Cherry_(including_sour)__healthy | 0.96 | 0.98 | 0.97 | 176 |
| Corn_(maize)__Common_rust_ | 0.98 | 0.99 | 0.98 | 222 |
| Blueberry__healthy | 0.95 | 0.99 | 0.97 | 283 |
| Potato__Early_blight | 0.97 | 0.97 | 0.97 | 178 |
| Pepper,_bell__healthy | 0.93 | 0.96 | 0.95 | 281 |
| Apple__Cedar_apple_rust | 0.92 | 0.97 | 0.95 | 63 |
| Grape__Leaf_blight_(Isariopsis_Leaf_Spot) | 1.0 | 0.98 | 0.99 | 222 |
| Tomato__Tomato_mosaic_virus | 0.72 | 0.94 | 0.81 | 77 |
| Tomato__Target_Spot | 0.82 | 0.77 | 0.80 | 284 |
| Tomato__healthy | 0.96 | 0.94 | 0.95 | 331 |
| Peach__Bacterial_spot | 0.98 | 0.94 | 0.96 | 475 |
| Corn_(maize)__Cercospora_leaf_spot_Gray_leaf_spot | 0.76 | 0.84 | 0.80 | 103 |
| Tomato__Spider_mites_Two-spotted_spider_mite | 0.84 | 0.88 | 0.86 | 331 |
| Corn_(maize)__healthy | 1.0 | 1.0 | 1.0 | 247 |
| Squash__Powdery_mildew | 0.99 | 0.99 | 0.99 | 356 |
| Cherry_(including_sour)__Powdery_mildew | 0.97 | 0.96 | 0.96 | 214 |
| Tomato__Bacterial_spot | 0.84 | 0.89 | 0.86 | 441 |
| Grape__Black_rot | 0.92 | 0.94 | 0.93 | 226 |
| Apple__healthy | 0.99 | 0.93 | 0.96 | 305 |
| Potato__healthy | 0.58 | 0.97 | 0.72 | 30 |
| Corn_(maize)__Northern_Leaf_Blight | 0.90 | 0.85 | 0.88 | 185 |
| Tomato__Septoria_leaf_spot | 0.82 | 0.76 | 0.79 | 352 |
| Raspberry__healthy | 0.92 | 1.0 | 0.96 | 79 |
| Soybean__healthy | 0.99 | 0.96 | 0.98 | 1000 |
| Apple__Apple_scab | 0.90 | 0.91 | 0.90 | 118 |
| Grape__healthy | 0.98 | 0.99 | 0.99 | 102 |

