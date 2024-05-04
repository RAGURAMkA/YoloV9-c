# YoloV9-c
This model is to generate bounding boxes and segmentation on fashion clothes.

The dataset used to fine-tune is DeepFashion
```!wget https://s3.us-west-2.amazonaws.com/testing.resources/datasets/deepfashion/deep_fashion.tar```

The original repository used to build the model
https://github.com/WongKinYiu/yolov9.git

Download pre-trained weights for the Yolo
```!wget -P {HOME}/weights -q https://github.com/WongKinYiu/yolov9/releases/download/v0.1/yolov9-c.pt```

Yolov9-c model performed well on the deep fashion dataset
accuracy for the train set with 50 images 57.5%

We can improve the metrics by tuning the hyperparameters and increasing the training set.
The uneven class distribution in my dataset played a major role in my metrics.
Adjusting the size and aspect ratios of anchor boxes to our needs will help the accuracy.
Train multiple YOLO models with different initializations or architectures and combine their predictions using techniques like averaging or stacking. Ensemble methods often lead to improved performance by leveraging diverse model predictions.
