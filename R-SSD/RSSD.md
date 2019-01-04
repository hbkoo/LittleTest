# R-SSD

**paper:**[Enhancement of SSD by concatenating feature maps for object detection](https://arxiv.org/abs/1705.09587) `CVPR2017`

## DataSet
PASCAL VOC

## Abstract
We propose an object detection method that improves the accuracy of the conventional SSD (Single Shot Multibox Detector), which is one of the top object detection algorithms in both aspects of accuracy and speed. The performance of a deep network is known to be improved as the number of feature maps increases. However, it is difficult to improve the performance by simply raising the number of feature maps. In this paper, we propose and analyze how to use feature maps effectively to improve the performance of the conventional SSD. The enhanced performance was obtained by changing the structure close to the classifier network, rather than growing layers close to the input data, e.g., by replacing VGGNet with ResNet. The proposed network is suitable for sharing the weights in the classifier networks, by which property, the training can be faster with better generalization power. For the Pascal VOC 2007 test set trained with VOC 2007 and VOC 2012 training sets, the proposed network with the input size of 300 x 300 achieved 78.5% mAP (mean average precision) at the speed of 35.0 FPS (frame per second), while the network with a 512 x 512 sized input achieved 80.8% mAP at 16.6 FPS using Nvidia Titan X GPU. The proposed network shows state-of-the-art mAP, which is better than those of the conventional SSD, YOLO, Faster-RCNN and RFCN. Also, it is faster than Faster-RCNN and RFCN.

我们提出了一种能够改进传统的SSD检测精度的对象检测的方法，它具有很好的检测精度和速度，是最好的对象检测方法之一。因为特征图数目的增加我们也知道深度网络的表现也会提高。然而，仅仅增加特征图的数目来改进表现是很困难的。在这篇论文中，我们提出并且分析了高效实用特征图来提高传统的SSD的表现。这个表现的提高是通过改变靠近分类器网络的结构，而不是增加输入数据的层，比如把VGGNet替换成ResNet。我们提出的网络适合在分类器网络里共享权重，通过这种特性，我们的训练可以更快。在Pascal VOC2007和2012数据集上训练，然后在VOC2007数据集上测试，当网络输入的图片为300×300时mAp达到78.5%并且速度为35FPS，当网络输入的图片为512×512时mAp达到80.8%并且速度为16.6FPS，使用的是Nvidia Titan X GPU。提出的网络展现了最好的mAp，它比传统的SSD、yolo、faster-RCNN和RFCN更好。而且，它比Faster-RCNN和RFCN很快。


## Contribution

- it creates a relationship between each scale of feature pyramid to prevent unnecessary detection such as multiple boxes in different scales for one object.

它创造了在特征金字塔中的每个尺度之间的联系，从而避免了不必要的检测，比如在不同尺度的多个boxes检测同一个物体。
- by efficiently increasing the number of feature maps of each layer in the feature pyramid, the accuracy is improved without much time overhead.

通过高效增加了特征金字塔中的每层特征图的数量，提高了精度而且没有过多的时间消耗。
- the number of feature maps for different layers are matched so that a single classifier can be used for different scales

不同层之间的特征图的数量是相同匹配的，因此在不同的特征尺度上可以使用单一的分类器网络。




