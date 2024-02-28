#铁网
“FE-Net:高效特征提取类别级6D姿态估计网络”的代码

##要求
代码已经过测试
-python 3.6.5
-pytorch 1.3.0
-CUDA 10.2

其他依赖关系:

```
sh依赖项。sh
```

##数据处理

请参考我们的另一部作品[自我DPDN](https://github.com/JiehongLin/Self-DPDN).


##网络培训


用于旋转估计的训练有限元网络:

```
python train . py-GPU 0-数据集$ {数据集} -模式r
```

训练…的网络[点网++](https://github.com/charlesq34/pointnet2)对于翻译和大小估计:

```
python train . py-GPU 0-数据集$ {数据集} -模式ts
```

字符串“数据集”可以设置为`数据集=REAL275`或者`数据集=相机25`.

##估价

要测试模型，请运行:

```
python train . py-GPU 0-数据集${DATASET}
```
字符串“数据集”可以设置为`数据集=REAL275`或者`数据集=相机25`.

##承认

我们的实现利用了来自[虚拟网络](https://github.com/JiehongLin/VI-Net),[国家奥委会](https://github.com/hughw19/NOCS_CVPR2019), [双PoseNet](https://github.com/Gorilla-Lab-SCUT/DualPoseNet)，以及[（speed）速度](https://github.com/mentian/object-deformnet).


