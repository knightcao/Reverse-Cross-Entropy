# Reverse Cross Entropy Training
Reverse Cross Entropy Training (RCE) is a novel training method, which can learn more distinguished feature representations for detecting adversarial examples.
Technical details are specified in:

[Towards Robust Detection of Adversarial Examples](http://arxiv.org/abs/1706.00633)

Tianyu Pang, Chao Du, Yinpeng Dong and Jun Zhu

## Training
We provide codes for training [ResNet](https://github.com/tensorflow/models/tree/master/research/resnet) on MNIST and CIFAR-10. Our codes are based on [Tensorflow](https://github.com/tensorflow). 

<b>Prerequisite:</b>
1. Install TensorFlow.

2. Download MNIST/CIFAR-10 dataset.

<b>How to run:</b>

An example of using RCE to train a ResNet-32 on MNIST is

```shell
python train.py --train_data_path='mnist_dataset/data_train.bin' \
                --log_root=models_mnist/resnet32 \
                --train_dir=models_mnist/resnet32/train \
                --dataset='mnist' \
                --num_gpus=1 \
                --num_residual_units=5 \
                --mode=train \
                --Optimizer='mom' \
                --total_steps=20000 \
                --RCE_train=True
```

## Test in the Normal Setting
