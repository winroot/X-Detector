# X-Detector
X-Detector is a collection of several object detection algorithms. And some of those have not appeared in any academic papers.

Up to now, this repository contains code of the re-implementent of [Light-Head R-CNN](https://arxiv.org/abs/1711.07264) and this trained version had got to 72.8%mAP(75.1%mAP using VOC12 evaluation alogorithm), more improvement is still in process. You can download the latest model weights (trained on PASCAL-07+12) from [GoogleDrive](https://drive.google.com/open?id=1hOvHnvl4hY6A1hawI3cTxpXY6GcPENMG).

Below is the training timeline of Light-Head RCNN for single 480x480 input image.

![](demo/timeline.JPG "Timeline of Light-Head RCNN")

Besides, several other detectors(named X-Det now) are also included, the main idea behind X-Det is to introduce explicit attention mechanisms between feature map channels, so I would like to change its name to "ABCD (**A**ttention **B**etween **C**hannels **D**etector)" later when the performance get to 0.7+mAP on PASCAL VOC 2007 Test Dataset (now only ~0.68mAP was achieved, improvement is still in process).

The pre-trained weights of backbone network can be found in [Resnet-50 backbone](https://github.com/tensorflow/models/tree/master/official/resnet) and [Xception backbone](https://github.com/HiKapok/Xception_Tensorflow). The latest version of PsRoIAlign is [here](https://github.com/HiKapok/PSROIAlign).

You can use part of these codes for your research purpose, but the ideas like the current implementent of X-Det is not allowed to copy without permissions. While the codes for Light-Head R-CNN can be used for your research without any permission but following [Apache License 2.0](https://github.com/HiKapok/X-Detector/blob/master/LICENSE). All codes were tested under TensorFlow 1.6, Python 3.5, Ubuntu 16.04.

Here are some demo result images of X-Det V2(68%mAP), debugging is still in process to make better performance:

![](demo/1.jpg "Detection Example 1")
![](demo/2.jpg "Detection Example 2")
![](demo/3.jpg "Detection Example 3")

## ##

**Update:**

- More than 7x performance improvement for Light-Head RCNN.
- Fine-tunning modified resnet backbone for X-Det.

## ##
Apache License 2.0
