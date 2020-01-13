# Instruction

Here is the instruction to sample 1000 classes images from ImageNet 2012 and test the pre-trained images.

The purpose is compared the accuracy on RGB and Gray Scale images

1. 

The following command will download 200 images from each of selected class, the 1000 classes list is already in the code :

```

python ./downloader.py 
    -data_root /test_images \
    -use_class_list True \
    -images_per_class 200
```

2. 

The labels of 1000 images is saved in [this file](https://github.com/Chuqiao2333/test_on_mobile_net/blob/master/imagenet_class_index.json)

Run this [notebook](https://github.com/Chuqiao2333/test_on_mobile_net/blob/master/test_RGB%26Gray.ipynb), Change it to compare RGB and Gray Scale images.

3. Current results

|Nets   |RGB|Gray|loss|
|--        |-- |--  |--|
|MobileNet     |77.22%   |59.44%|18%|
|AlexNet     |64.06%   |33.56%|31%|
|VGG16  |78.81%|60.34%|18%|
|ResNet19|73.58%|55.68%|18%|
|GoogleNet|71.09%|58.77|13%|

4. Fine-tune the classifier layer on gray scale images

More pre_trained nets needed to be test
