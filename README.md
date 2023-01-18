# Crack-Detection-with-Transfer-Learning
Crack detection model using transfer learning based on the Resnet50 model

dataset: https://www.kaggle.com/datasets/xinzone/surface-crack


Metrics for trained model

Accuracy: 99.219%

Precisin: 100%

Recall: 98.403%

f1-score: 99.195%


Dataset:

training data - split into 2 classes: Positive and Negative with 300 images in each of size 224x224

test data - 2 classes: Positive and negative with 100 images in each of size 224x224

validation data - 2 classes: Positive and negative with 100 images in each of size 224x224

predict set - 6 images of size 4800x3200


data augmentation:

methods: 
         
         rotation_range = 3,
         
         vertical_flip=True,
         
         horizontal_flip = True,
         
         brightness_range = (0.5, 1.2))
         

training data: augmented to 23,907 images in each class

test data: augmented to 7232 images in each class

validation data: augmented to 7248 images in each class


model architecture:

base model: Resnet50, without Dense layers

subsequent layers: Dense layer of size 2048, Dense layer of size 128, softmax layer for 2 classes
optimizer: Adam - learning rate 0.001

Sample training images:

![image](https://user-images.githubusercontent.com/81284513/213267807-47243ad1-a49f-4981-9423-26bd1d1193a2.png)

![image](https://user-images.githubusercontent.com/81284513/213267917-a27004b9-5f05-4260-9038-5d2cccb5a3fc.png)


sample prediction with image:

![image](https://user-images.githubusercontent.com/81284513/213268087-e0521485-def3-4b5a-8602-1baff377bfca.png)

prediction: Cracked
