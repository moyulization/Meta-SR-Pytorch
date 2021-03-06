# Meta-SR
Official implementation of **Meta-SR: A Magnification-Arbitrary Network for Super-Resolution(CVPR2019)(PyTorch)**
  
[Paper](https://arxiv.org/pdf/1903.00875.pdf)

Our code is built on [EDSR(PyTorch)](https://github.com/thstkdgus35/EDSR-PyTorch).
# Requirements

* Pytorch 0.4.0
* Python 3.5
* numpy
* skimage
* imageio
* cv2  
*note that if you use another version of pytorch (>0.4.0), you can rewrite the dataloader.py
# Train and Test
* prepare dataset: we follow the previous work, that is, we use the matlab imresize function to generate the LR images.
you can run the matlab files to get the training and test dataset :  /prepare_dataset/geberate_LR_metasr_X1_X4.m
* change the config file option.py : include dir_data
* pre_train model   
  [BaiduYun](https://pan.baidu.com/s/14L4Aut-F4JoSRfkJh6vr4Q) fetch code: btc5  
  [GoogleDrive](https://drive.google.com/open?id=1tGjz_pzgvo1T2N4f_ZjuqmxQHdpeDiSB)
## train 
```
cd /Meta-SR-Pytorch 
python main.py --model metardn --save metardn_model_name --ext sep --lr_decay 200 --epochs 1000 --n_GPUs 4 --batch_size 16 
```
## test 
```
python main.py --model metardn --save metardn_model_name --ext sep --pre_train **** --test_only --data_test BSD or Set14 orSet5  --scale 2.3
```
# Citation
```
@article{hu2019meta,
  title={Meta-SR: A Magnification-Arbitrary Network for Super-Resolution},
  author={Hu, Xuecai and Mu, Haoyuan and Zhang, Xiangyu and Wang, Zilei  and Tan, Tieniu and Sun, Jian},
  booktitle={IEEE Conference on Computer Vision and Pattern Recognition},
  year={2019}
}
```
# Contact
Xuecai Hu (huxc@mail.ustc.edu.cn)
