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

|#images   |RGB|Gray|
|--        |-- |--  |
|10,000      |77.171875%|57.78125%|
|200,000     |77.22%   |59.44%|

4. To do

More images needed to be test
