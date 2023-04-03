# supersickrobot
Fruit Classification: Apple, Banana, Orange


# Data preprocessing:
1. Removed XML file with no corresponding image file
2. Separated test dataset
3. Resized to (150,150) and normalized
4. Used rotation, shifting, shearing, and zooming for augmentation

# Model architecture:
Tested various models (pretraind as well as simple CNNs) but Inception V3 was more accurate in prediction.

# Training:
1. Transfer learning for 10 epochs and Fine-tuned for 3 epochs.
2. Compiled using RMSprop optimizer 

# Evaluation:
The model was accurate in predicting fruits in single class images (only apple/banana/orange), but while testing with the mixed dataset it was partially correct most of the time with a single wrong prediction in the test dataset. The threshold was chosen to be 30%.

# Deployment:
The model was saved in .pb format. To deploy the model in an application it needs to be converted into .tflite format. After that, it can be easliy integrated with any mobile application which is built using tensorflow binaries and NDK. 
