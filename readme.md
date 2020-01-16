# Instruction

Here is the instruction to sample 1000 classes images from ImageNet 2012 and test the pre-trained images.

The purpose is compared the accuracy on RGB and Gray Scale images

### Usage

1. 

The following command will download 200 images from each of selected class, the 1000 classes list is already in the code :

```

python ./downloader.py 
    -data_root /test_images \
    -use_class_list True \
    -images_per_class 200
```

IMPORTANT: There are four classes' urls invali, to get the same classes as the ImageNet 2012, you need to add 638,850,134,343 these folders manully.

2. 

The labels of 1000 images is saved in [this file](https://github.com/Chuqiao2333/test_on_mobile_net/blob/master/imagenet_class_index.json)

Run this [notebook](https://github.com/Chuqiao2333/test_on_mobile_net/blob/master/test_RGB%26Gray.ipynb), Change it to compare RGB and Gray Scale images.

### Current results

|Nets       |State_of_art   |Sampled RGB images |Gray   |Fine-tune Gray |loss|
|--         |--             |--                 |--     |  --           |--|
|MobileNet  |74.7%          |77.22%             |59.44% |  %            |18%|
|AlexNet    |63.3%          |64.06%             |33.56% |               |31%|
|VGG16      |74.4%          |78.81%             |60.34% |  %            |18%|
|ResNet19   |72.19%         |73.58%             |55.68% |               |18%|
|GoogleNet  |69.8%          |71.09%             |58.77% |               |13%|

#### Pre-trained model
The pretrained models are trained by RGN images so the smapled images accuracy is closed to state-of-art, while The accuracy on gray scale images are lower. 
#### Fine-tune the claasifier
To improve the accuracy of gray scale images, we use transfer learning and fine-tune the fully connective layer, while the results seems bad. The model is easily to overfit.
