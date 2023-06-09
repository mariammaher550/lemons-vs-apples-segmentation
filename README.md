# lemons-vs-apples-segmentation
What would you do if life gives you lemons? easy, make a photo session for some lemons and apples then see if a YOLOv8 and Faster-RCNN will be able to detect lemons from sweet-sweet apples.


## 1. Dataset Collection
- There were two lemons and two apples, a green one and a red one in my humble fridge. so I took a 100 picture of them collectively. I made sure to take them under different light conditions and using different backgrounds
- <img src="https://user-images.githubusercontent.com/36730799/223129385-48e43120-95f6-4de5-a9b7-cf509ec9a52c.png" width=25% height=25%> <img src="https://user-images.githubusercontent.com/36730799/223129324-8f483327-38a3-43ca-b481-15382c466d4f.png" width=25% height=25%>
- Then annonated the pictures using Roboflow 
- Applied resizing and rotation for data preprocessing and agumentation

## 2. Model Training and Inference 
I used Mask-RCNN and YOLOV8 for this image segmentation  task. 

### 2.1 Mask-RCNN
You can find my notebook [here](https://colab.research.google.com/drive/1v9dNxB-gxV1bEndYhBuodas6BHYMeBrN?usp=sharing) for the source code. 
#### Training, Inference and Metrics
- I used detectron2 to load and train Mask-RCNN from detectron2 model zoo. You could find their official repo [here](https://github.com/facebookresearch/detectron2) 
- The training has taken 14 minutes with 300 epochs and 16 batch size
- Metrics :
-  <img src= "https://user-images.githubusercontent.com/36730799/235318562-7b7f1a21-47cb-4c41-b1c6-0cc87d9452d7.png" width=60% height=60% >
- Samples detected : 
- <img src="https://user-images.githubusercontent.com/36730799/235318587-8707744c-2d61-498a-ae18-2e021a61dc7b.png"
 width=20% height=20%>  <img src="https://user-images.githubusercontent.com/36730799/235318605-ea43be48-3b3f-4fde-96ae-bafa0288523c.png"
 width=20% height=20%> 

### 2.2 YOLOv8
You can find my notebook [here](https://colab.research.google.com/drive/1yIWEb8iHm8ef9_UBb5Eb2l0U6tdcfTvy?usp=sharing) for the source code
#### Training, Inference and Metrics
- The training has taken less than 10 minutes with 100 epochs 
- Metrics :
-

-  <img src= "https://user-images.githubusercontent.com/36730799/235319603-6385202c-8cb8-4b16-8752-bab2aefa99fd.png"
 width=80% height=80% > 
