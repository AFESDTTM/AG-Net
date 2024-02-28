# FE-Net
Efficient Feature Extraction Category Level 6D Pose Estimation Network

# Requirements
The code has benn tested with
python 3.6.5
pytorch 1.3.0
CUDA 10.2
Other dependencies:
 sh dependencies.sh
# Data Processing
Please refer to our another work of Self-DPDN.
# Network Training
Train VI-Net for rotation estimation:

python train.py --gpus 0 --dataset ${DATASET} --mode r
Train the network of pointnet++ for translation and size estimation:

python train.py --gpus 0 --dataset ${DATASET} --mode ts 
The string "DATASET" could be set as DATASET=REAL275 or DATASET=CAMERA25.
# Evaluation
To test the model, please run:
python test.py --gpus 0 --dataset ${DATASET}
The string "DATASET" could be set as DATASET=REAL275 or DATASET=CAMERA25.
