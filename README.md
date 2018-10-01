# deep_segmentation_for_taxiing

This is the source code implementation for deep segmentation for taxiing assistance purposes. 

___

Files:

  * deep_segmentation_for_taxiing.onnx - Deep-learning model in an universal format to compute semantic segmentation. 
  * demo_deep_segmentation_for_taxiing.ipynb - Demonstration of semantic segmentation on an test image. 
  * data/ - contains an original image of runway and its ground truth annotation

___

The network model used is inspired on [Deeplab v3](https://arxiv.org/abs/1706.05587).
The network is first trained with Cityscape datasets on the *train_fine* set only. 
The weights are then fine-tuned on specific images for taxiing assistance purposes. 

The image is partitioned in four classes:
  1. Foreground Stuff (ID 0)
  2. Grass (ID 1)
  3. Runway (ID 2)
  4. Sky (ID 3)

