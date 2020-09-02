# KPN_Denoising_Pytorch

Reimplement of Burst Denoising with Kernel Prediction Networks (KPN) and Multi-Kernel Prediction Networks (MKPN) for Denoising of Image Burst by using PyTorch.

## KPN Framework

![image](https://github.com/WenxueCui/KPN_Denoising_Pytorch/raw/master/images/framework.png)

## Requirements and Dependencies

* Ubuntu 16.04 CUDA 10.0
* Python3 （Testing in Python3.5）
* Pytorch 1.1.0   
* Torchvision 0.2.2

## Details of Implementations

In our code, two model version are included:

* simple version of CSNet (Similar with paper ICME2017)
* Enhanced version of CSNet (local skip connection + global skip connection + resudial learning)

## How to Run

### Training CSNet
* Preparing the dataset for training

* Editing the path of training data in file `train.py`.

* For CSNet training in terms of subrate=0.1:

```python train.py --sub_rate=0.1 --block_size=32```

### Testing CSNet
* Preparing the dataset for testing

* Editing the path of trained model in file `test.py`.

* For CSNet testing in terms of subrate=0.1:

```python test.py --sub_rate=0.1 --block_size=32```

* For CSNet testing (new testing code) in terms of subrate=0.1:

```python test_new.py --cuda --sub_rate=0.1 --block_size=32```

## CSNet results
### Subjective results

![image](https://github.com/WenxueCui/KPN_Denoising_Pytorch/raw/master/images/result1.png)

### Objective results
![image](https://github.com/WenxueCui/CSNet-Pytorch/raw/master/images/table.jpg)

## Additional instructions

* For training data, you can choose any natural image dataset.
* The training data is very important, if you can not achieve ideal result, maybe you can focus on the augmentation of training data or the structure of the network.
* If you like this repo, Star or Fork to support my work. Thank you.
* If you have any problem for this code, please email: wenxuecui@stu.hit.edu.cn

