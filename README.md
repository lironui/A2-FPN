# A<sup>2</sup>-FPN for Semantic Segmentation of Fine-Resolution Remotely Sensed Images

⭐ [Welcome to my HomePage](https://lironui.github.io/) ⭐ 

In this repository, we implement the Feature Pyramid Network (FPN) with Attention Aggregation Module (AAM), i.e., A<sup>2</sup>-FPN, for semantic segmentation of fine-resolution remotely sensed images.

The detailed results can be seen in the [A<sup>2</sup>-FPN for Semantic Segmentation of Fine-Resolution Remotely Sensed Images](https://www.tandfonline.com/doi/full/10.1080/01431161.2022.2030071).

The related repositories include:
* [ABCNet](https://github.com/lironui/ABCNet)->An efficient segmentation model.
* [MACU-Net](https://github.com/lironui/MACU-Net)->A modified version of U-Net.
* [BANet](https://github.com/lironui/BANet)->A Transformer-based segmentation network.
* [MAResU-Net](https://github.com/lironui/MAResU-Net)->A ResNet-based network with attention mechanism.
* [Multi-Attention-Network](https://github.com/lironui/Multi-Attention-Network)->A network with multi kernel attention mechanism.

If our code is helpful to you, please cite:

`Rui Li, Libo Wang, Ce Zhang, Chenxi Duan & Shunyi Zheng (2022) A2-FPN for semantic segmentation of fine-resolution remotely sensed images, International Journal of Remote Sensing, 43:3, 1131-1155, DOI: 10.1080/01431161.2022.2030071.`

Network:
------- 
![network](https://github.com/lironui/A2-FPN/blob/main/figure/network.png)  
Fig. 1.  The overall architecture of A<sup>2</sup>-FPN.

Result:
------- 
The result on the [UAVid dataset](https://uavid.nl/) can seen from [here](https://competitions.codalab.org/competitions/public_submissions/25224) or download by this [link](https://competitions.codalab.org/my/competition/submission/1055948/input.zip):

| Method    | Backbone  | building | tree     | clutter   | road     | vegetation | static car | moving car | human    | mIoU     | 
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:| 
| MSD <sup>[1]</sup>      |- | 79.8     | 74.5     | 57.0      | 74.0     | 55.9       | 32.1       | 62.9       | 19.7 | 57.0     | 
| BiSeNet <sup>[2]</sup>  |ResNet-18 | 85.7     | 78.3     | 64.7      | 61.1     | **77.3**   | **63.4**   | 48.6       | 17.5     | 61.5     | 
| SwiftNet <sup>[3]</sup>  |ResNet-18 | 85.3     | 78.2     | 64.1      | 61.5     | 76.4       | 62.1       | 51.1       | 15.7     | 61.1     | 
| ShelfNet <sup>[4]</sup>  |ResNet-18 | 85.3     | 78.2     | 44.1      | 61.4     | 43.4       | 21.0       | 52.6       | 3.6      | 47.0     | 
| MANet <sup>[5]</sup>    |ResNet-18 | 85.4     | 77.0     | 64.5      | 77.8     | 60.3       | 53.6       | 67.2        | 14.9      | 62.6    | 
| BANet <sup>[6]</sup>    |ResNet-18 | 85.4     | 78.9 | 66.6  | 80.7 | 62.1       | 52.8       | 69.3   | 21.0 | 64.6 | 
| ABCNet <sup>[7]</sup>   |ResNet-18 | 86.4 | 79.9 | **67.4**  | **81.2** | 63.1       | 48.4       | 69.8   | 13.9     | 63.8 | 
| A<sup>2</sup>-FPN <sup>[8]</sup> |ResNet-18 | **87.2** | **80.1** | **67.4**  | 80.2 | 63.7       | 53.3       | **70.1**   | **23.4**     | **65.7** | 

Reference:  
`[1] Lyu, Y., Vosselman, G., Xia, G. S., Yilmaz, A., & Yang, M. Y. (2020). UAVid: A semantic segmentation dataset for UAV imagery. ISPRS journal of photogrammetry and remote sensing, 165, 108-119.`  
`[2] Yu, C., Wang, J., Peng, C., Gao, C., Yu, G., & Sang, N. (2018). Bisenet: Bilateral segmentation network for real-time semantic segmentation. In Proceedings of the European conference on computer vision (ECCV) (pp. 325-341).`
`[3] Oršić, M., & Šegvić, S. (2021). Efficient semantic segmentation with pyramidal fusion. Pattern Recognition, 110, 107611.`
`[4] Zhuang, J., Yang, J., Gu, L., & Dvornek, N. (2019). Shelfnet for fast semantic segmentation. In Proceedings of the IEEE/CVF International Conference on Computer Vision Workshops (pp. 0-0).`
`[5] R. Li, S. Zheng, C. Zhang, C. Duan *, J. Su, L. Wang, and P. M. Atkinson. (2021). Multiattention network for semantic segmentation of fine-resolution remote sensing images. IEEE Transactions on Geoscience and Remote Sensing, doi: 10.1109/TGRS.2021.3093977.`  
`[6] L. Wang, R. Li, D. Wang, C. Duan, T. Wang, and X. Meng. (2021). Transformer Meets Convolution: A Bilateral Awareness Network for Semantic Segmentation of Very Fine Resolution Urban Scene Images. Remote Sensing, 13(16), 3065, doi: 10.3390/rs13163065.`  
`[7] R. Li, S. Zheng, C. Zheng, C. Duan *, L. Wang, and P. M. Atkinson. ABCNet: Attentive bilateral contextual network for efficient semantic segmentation of Fine-Resolution remotely sensed imagery. ISPRS Journal of Photogrammetry and Remote Sensing, 181, 84-98, doi: 10.1016/j.isprsjprs.2021.09.005.`  
`[8] R. Li, L. Wang, C. Zhang, C. Duan, S. Zheng. (2022) A<sup>2</sup>-FPN for semantic segmentation of fine-resolution remotely sensed images. International Journal of Remote Sensing, 43:3, 1131-1155, doi: 10.1080/01431161.2022.2030071.`


![Result](https://github.com/lironui/A2-FPN/blob/main/figure/UAVid.png)  
Fig. 2.  The experimental results on the UAVid test set. The first column illustrates the input RGB images, the second column depicts the outputs of MSD and the third column shows the predictions of our A<sup>2</sup>-FPN. 

