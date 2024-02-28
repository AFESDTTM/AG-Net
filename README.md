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

Please refer to our another work of [Self-DPDN](https://github.com/JiehongLin/Self-DPDN).


## Network Training


Train FE-Net for rotation estimation:

```
python train.py --gpus 0 --dataset ${DATASET} --mode r
```

Train the network of [pointnet++](https://github.com/charlesq34/pointnet2) for translation and size estimation:

```
python train.py --gpus 0 --dataset ${DATASET} --mode ts 
```

The string "DATASET" could be set as `DATASET=REAL275` or `DATASET=CAMERA25`.

## Evaluation

To test the model, please run:

```
python train.py --gpus 0 --dataset ${DATASET}
```
The string "DATASET" could be set as `DATASET=REAL275` or `DATASET=CAMERA25`.

## Acknowledgements

Our implementation leverages the code from [VI-Net](https://github.com/JiehongLin/VI-Net),[NOCS](https://github.com/hughw19/NOCS_CVPR2019), [DualPoseNet](https://github.com/Gorilla-Lab-SCUT/DualPoseNet), and [SPD](https://github.com/mentian/object-deformnet).
