# RSOS

## RSOS-Net: Real-time Surface Obstacle Segmentation Network for Unmanned Waterborne Vehicles

### Introduction

RSOS-Net is a real-time surface obstacle segmentation network designed for unmanned waterborne vehicles. Utilizing deep learning and computer vision techniques, it accurately segments waterborne obstacles, providing crucial information for autonomous navigation and safe operation of unmanned waterborne vehicles.

### Installation

This code is implemented based on MMSegmentation. Please refer to [https://github.com/open-mmlab/mmsegmentation/tree/main](https://github.com/open-mmlab/mmsegmentation/tree/main) for the required libraries to install. Ensure that Python and its dependencies are installed, and follow the MMSegmentation instructions for environment configuration.

### Data

Download the LaRS dataset: [https://lojzezust.github.io/lars-dataset/](https://lojzezust.github.io/lars-dataset/)

The dataset contains annotated images and corresponding obstacle labels for training and testing RSOS-Net. Please ensure that the data is downloaded and organized correctly according to the dataset instructions.

### Getting Started

#### Training

To start the training process, use the following command:

```bash
python tools/train.py RSOS-Net/rsos_r18_4xb4-160k_cocostuff164k-512x1024.py
```

This will initiate training using the specified configuration file `rsos_r18_4xb4-160k_cocostuff164k-512x1024.py`. Ensure that the configuration file exists and the path is correct.

#### Inference

To run inference on the model and segment input data, use the following command:

```bash
python tools/test.py $CONFIG $WEIGHTS --show-dir $OUT_DIR
```

* `$CONFIG`: The path to the configuration file used during training.
* `$WEIGHTS`: The path to the trained model weights file.
* `$OUT_DIR`: The output directory to save the visualized segmentation results.

Before running inference, ensure that you have trained the model and specified the correct weight file path. Additionally, set the output directory according to your preference to view the segmentation results.

### Notes

* Ensure that the environment is properly configured, and all necessary dependencies are installed before starting training or inference.
* Depending on your dataset and hardware configuration, you may need to adjust parameters in the configuration file to achieve optimal training results.
* If you encounter any issues or errors, refer to the MMSegmentation documentation or relevant communities for assistance.

### Contact Information

If you encounter any problems or require further assistance while using RSOS-Net, please contact us at [fengyuan@dlmu.edu.cn].

### Acknowledgments

We would like to thank the MMSegmentation project for providing a powerful framework and tools that enabled us to quickly implement and deploy RSOS-Net. Additionally, we acknowledge the contributors of the LaRS dataset for providing valuable data resources.
