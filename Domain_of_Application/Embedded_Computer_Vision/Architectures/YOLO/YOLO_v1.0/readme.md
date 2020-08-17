
# Overview 

YOLO v.10 

Paper: [You Only Look Once: Unified, Real-Time Object Detection](https://arxiv.org/abs/1506.02640)



# Architecture 

![YOLO_Architecture1](https://www.researchgate.net/publication/329038564/figure/fig2/AS:694681084112900@1542636285619/YOLO-architecture-YOLO-architecture-is-inspired-by-GooLeNet-model-for-image.ppm)

Structure: 

Block 1: ConvBlocks 

- Set of Convolutional Layers 

Block 2_ Dense Layers 

- 2 x Dense hence Fully Connected Layers 

Definition of components, assuming Pytorch 

- [nn.Conv2d](https://pytorch.org/docs/stable/generated/torch.nn.Conv2d.html)
- [nn.MaxPool2d](https://pytorch.org/docs/master/generated/torch.nn.MaxPool2d.html)
- [nn.LeakyReLU](https://pytorch.org/docs/master/generated/torch.nn.LeakyReLU.html)

## Block 1 - ConvLayers 

In the ConvBlock the activations are all leaky relus, from the paper 

![Img1](YOLOv1_LeakyRELU1.png)

Subblock 1 : 

| From the Picture | Pytorch | Comment | 
| --- | --- | --- |
| Input 448x448x3 |  |  | 
| > Conv. Layer, 7x7x64-s-2 | `nn.Conv2d(in_channels=3, out_channels=64, kernel_size=7, stride=2)` | Padding? |
| > LeakyRELU 0.1 | `nn.LeakyReLU(negative_slope=0.1)` |  | 
| > Maxpool Layer 2x2-s-2 | `nn.MaxPool2d(kernel_size=2, stride=2)` | Before, what activation? | 

Work in progress 


