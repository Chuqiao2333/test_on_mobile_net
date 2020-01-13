# Instruction

Here is the instruction to sample 1000 classes images from ImageNet 2012 and test the pre-trained images.

The purpose is compared the accuracy on RGB and Gray Scale images

1. 

The following command will download 10 images from each of selected class, the 1000 classes list is already in the code :

```

python ./downloader.py 
    -data_root /test_images \
    -use_class_list True \
    -images_per_class 10
```

2. 

The labels of 1000 images is saved in [this file](https://github.com/Chuqiao2333/test_on_mobile_net/blob/master/imagenet_class_index.json)

Run this [notebook](https://github.com/Chuqiao2333/test_on_mobile_net/blob/master/test_RGB%26Gray.ipynb), Change it to compare RGB and Gray Scale images.

3. Current results

|Nets   |RGB|Gray|
|--        |-- |--  |
|MobileNet     |77.22%   |59.44%|
|AlexNet     |64.06%   |33.56%|
|VGG16  |78.81%|60.34%|
|ResNet19|73.58%|55.68%|

4. To do

More pre_trained nets needed to be test
