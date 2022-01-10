# A<sup>2</sup>-FPN for Semantic Segmentation of Fine-Resolution Remotely Sensed Images

In this repository, we implement the Feature Pyramid Network (FPN) with Attention Aggregation Module (AAM), i.e., A<sup>2</sup>-FPN, for semantic segmentation of fine-resolution remotely sensed images.

The detailed results can be seen in the [A<sup>2</sup>-FPN for Semantic Segmentation of Fine-Resolution Remotely Sensed Images](https://arxiv.org/pdf/2102.07997.pdf).

The related repositories include:
* [ABCNet](https://github.com/lironui/ABCNet)->An efficient segmentation model.
* [MACU-Net](https://github.com/lironui/MACU-Net)->A modified version of U-Net.
* [BANet](https://github.com/lironui/BANet)->A Transformer-based segmentation network.
* [MAResU-Net](https://github.com/lironui/MAResU-Net)->A ResNet-based network with attention mechanism.
* [Multi-Attention-Network](https://github.com/lironui/Multi-Attention-Network)->A network with multi kernel attention mechanism.

If our code is helpful to you, please cite:

`Li, Rui, Libo Wang, Ce Zhang, Chenxi Duan, and Shunyi Zheng. "A<sup>2</sup>-FPN for Semantic Segmentation of Fine-Resolution Remotely Sensed Images." arXiv preprint arXiv:2102.07997 (2021).` (The paper has been accepted by International Journal of Remore Sensing, the citation form will be updated soon)

Requirements：
------- 
```
numpy >= 1.16.5
PyTorch >= 1.3.1
sklearn >= 0.20.4
tqdm >= 4.46.1
imageio >= 2.8.0
```

Network:
------- 
![network](https://github.com/lironui/A2-FPN/blob/main/figure/network.png)  
Fig. 1.  The overall architecture of A<sup>2</sup>-FPN.

Result:
------- 
The result on the [UAVid dataset](https://uavid.nl/) can seen from [here](https://competitions.codalab.org/competitions/public_submissions/25224) or download by this [link](https://competitions.codalab.org/my/competition/submission/1055948/input.zip):

| Method    | building | tree     | clutter   | road     | vegetation | static car | moving car | human    | mIoU     | 
|-----------|----------|----------|-----------|----------|------------|------------|------------|----------|----------| 
| MSD       | 79.8     | 74.5     | 57.0      | 74.0     | 55.9       | 32.1       | 62.9       | 19.7 | 57.0     | 
| BiSeNet   | 85.7     | 78.3     | 64.7      | 61.1     | **77.3**   | **63.4**   | 48.6       | 17.5     | 61.5     | 
| SwiftNet  | 85.3     | 78.2     | 64.1      | 61.5     | 76.4       | 62.1       | 51.1       | 15.7     | 61.1     | 
| ShelfNet  | 85.3     | 78.2     | 44.1      | 61.4     | 43.4       | 21.0       | 52.6       | 3.6      | 47.0     | 
| MANet     | 85.4     | 77.0     | 64.5      | 77.8     | 60.3       | 53.6       | 67.2        | 14.9      | 62.6    | 
| BANet     | 85.4     | 78.9 | 66.6  | 80.7 | 62.1       | 52.8       | 69.3   | 21.0 | 64.6 | 
| ABCNet    | 86.4 | 79.9 | **67.4**  | **81.2** | 63.1       | 48.4       | 69.8   | 13.9     | 63.8 | 
| A<sup>2</sup>-FPN | **87.2** | **80.1** | **67.4**  | 80.2 | 63.7       | 53.3       | **70.1**   | **23.4**     | **65.7** | 

![Result](https://github.com/lironui/A2-FPN/blob/main/figure/UAVid.png)  
Fig. 2.  The experimental results on the UAVid test set. The first column illustrates the input RGB images, the second column depicts the outputs of MSD and the third column shows the predictions of our A<sup>2</sup>-FPN. 

