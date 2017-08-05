# Keras-PoseNet
**This is a an implementation in Keras v2 of the [PoseNet architecture](http://mi.eng.cam.ac.uk/projects/relocalisation/). This code is based off Kent Sommer's implementation in v1 Keras of [PoseNet](https://github.com/kentsommer/keras-posenet)**

## Contributions

 * Ported v1 Keras code into v2 Keras. The new posenet architecture is structurally the same as the original, however the training results of the v1 and v2 implementations are different using the default parameters. Tuning the hyperparameters can lead to comparable results. 
 * Added matplot of predicted v ground truth pose estimation. This is automatically plotted when test.py is run.

## Introduction
As described in the ICCV 2015 paper **PoseNet: A Convolutional Network for Real-Time 6-DOF Camera Relocalization** Alex Kendall, Matthew Grimes and Roberto Cipolla [http://mi.eng.cam.ac.uk/projects/relocalisation/]

Note that this requires the TensorFlow backend for Keras, however, only minor modifications to the model as well as the helper.py file would be required in order to use the Theano backend. If someone would like assistance with this, simply open an issue. 

## Getting Started

 * Download the Cambridge Landmarks King's College dataset [from here.](https://www.repository.cam.ac.uk/handle/1810/251342)

 * Download the starting and trained weights [from here.](https://drive.google.com/file/d/0B5DVPd_zGgc8RU82RkNLWUVOLWc/view?usp=sharing)

 * The PoseNet model is defined in the posenet.py file

 * The starting and trained weights (posenet.npy and trained_weights.h5 respectively) for training were obtained by converting caffemodel weights [from here](http://vision.princeton.edu/pvt/GoogLeNet/Places/) and then training.

 * To run:
   * Extract the King's College dataset to wherever you prefer
   * Extract the starting and trained weights to the same location as test.py and train.py
   * Update the dataset path on line 9 in helper.py
   * If you want to retrain, simply run train.py (note this will take a long time)
   * If you just want to test, simply run test.py 
