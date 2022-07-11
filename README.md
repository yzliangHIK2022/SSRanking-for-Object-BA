# SSRanking-for-Object-BA
Dataset of our ICIP2022 paper: "Semi-Supervised Ranking for Object Image Blur Assessment".

![Frame_work](https://github.com/yzliangHIK2022/SSRanking-for-Object-BA/blob/main/FrameWork.PNG)

# Dataset Download

We realease the txt files on the "Release" of this repo: https://github.com/yzliangHIK2022/SSRanking-for-Object-BA/releases/tag/releaseDataset_1.0

Please kindly refer to above URL for downloading.


# Details
## Crop information
We provide the face **cropped information** of dataset images in: 
```LFW_all_imgs_list.txt, CASIA_all_imgs_list.txt, WiderFace_train_all_imgs_list.txt, WiderFace_val_all_imgs_list.txt, MegaFace_all_imgs_list.txt.```

The **format** (for each line) of cropped txtfiles: 
```"DatasetName>>Original_image_name>>crop_x crop_y crop_width crop_height>>Image_name_after_cropping\n".```

e.g. "LFW>>Aaron_Eckhart_0001.jpg>>22 33 202 202>>Aaron_Eckhart_0001.jpg\n": 
It means that image "Aaron_Eckhart_0001.jpg" is cropped from "LFW" dataset based on position of "22 33 202 202" in original image "Aaron_Eckhart_0001.jpg".


## Training datasets
We release our supervised and unsupervised **tranning list**:
```SSRanking_OBA_train_supervised_5k.txt, SSRanking_OBA_train_supervised_10k.txt, SSRanking_OBA_train_unsupervised.txt.```

The **format** (for each line) of **supervised** txtfiles: 
```"Image_left,Image_right\n".```

e.g. "CASIA_WebFace/0000133/039.jpg,LFW/Chris_Neil_0001.jpg\n": 
It means that the face in the "Image_right" in more blur than "Image_left".

The **format** (for each line) of **unsupervised** txtfiles: 
```"Image_left,Image_right\n".```

e.g. "Images_Wider_Train/35--Basketball/35_Basketball_playingbasketball_35_397_2.jpg,Images_Wider_Train/0--Parade/0_Parade_Parade_0_69_5.jpg\n": 
Image "Image_left" and image "Image_right" will be used as unsupervised image-pair for unsupervised training by L_{QRC} which is detailed in our paper.


## Testing dataset
We release our **testing list**: 
```SSRanking_OBA_test_test1.txt, SSRanking_OBA_test_test2.txt SSRanking_OBA_test_test3.txt.```

The **format** (for each line) of txtfiles: 
```"image_name image_order\n".```

e.g. "LFW/Gordon_Brown_0007_2.jpg 1\n": 
It means that image "image_name" rank order "image_order" in current test set. The larger the rank order, the more blur is this image.



# Citation:
```
Qiang Li, Zhaoliang Yao, Jingjing Wang, Ye Tian, Pengju Yang, Di Xie, Shiliang Pu, "Semi-Supervised Ranking for Object Image Blur Assessment," IEEE International Conference on Image Processing, 2022.
```
