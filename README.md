# Counting Fingers
In this project, convolutional neural network was used to count number of fingers as well as identify which hand was upheld in image
#### [Notebook](https://github.com/bhavikfirke/Counting_Fingers/blob/main/counting_fingers_github.ipynb)

	
## Dataset
The [dataset](https://www.kaggle.com/datasets/koryakinp/fingers) consits of 18000 training images along with 3600 images for testing

## Approach
### Preprocessing
- Resized all images and simple data augmentations tricks such as shear, rotation, etc were used to artifically increase training examples seen by convnet

### Training
- MobileNetV2 architecture along with ImageNet weights was used as convolution base
- As this was multi label classification, binary crossentropy and sigmoid was used as loss function and activation function respectively
- To select threshold value, performance  of various threshold values was evaluated using Matthews Correlation Coefficient

## Outcome
- We obtain **0.73 exact match ratio** and **0.049 hamming loss** on test set 

## Visualizing convnet output
The test image of 5 fingers shown along with activation heatmap of last convolution layer <br>


![Activation heatmap example](https://github.com/bhavikfirke/Counting_Fingers/blob/main/GradCAM_heatmap.png)
