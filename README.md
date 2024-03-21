# FE-Net
Code for "FE-Net:Efficient Feature Extraction Category Level 6D Pose Estimation Network"

## Requirements
The code has been tested with
- python 3.6.5
- pytorch 1.3.0
- CUDA 10.2

Other dependencies:

```
sh dependencies.sh
```

## Data Processing

Please refer to  work of [Self-DPDN](https://github.com/JiehongLin/Self-DPDN).




## Evaluation

To test the model, please run:

```
python train.py --gpus 0 --dataset ${DATASET}
```
The string "DATASET" could be set as `DATASET=REAL275` or `DATASET=CAMERA25`.




## Results
Qualitative results on REAL275 test set:
<p align="center">
	<img src ="Result/result.png" width="600" />
</p>

Qualitative Comparison between FE-Net and VI-Net on the REAL275 Datasets.
<p align="center">
	<img src ="Result/isualization.png" width="600" />
</p>

## Acknowledgements

Our implementation leverages the code from [VI-Net](https://github.com/JiehongLin/VI-Net),[NOCS](https://github.com/hughw19/NOCS_CVPR2019), [DualPoseNet](https://github.com/Gorilla-Lab-SCUT/DualPoseNet), and [SPD](https://github.com/mentian/object-deformnet).
