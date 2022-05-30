
# Intruder detection using Object detection Algorithm

The project is about detecting intruder in hostel room when roommates are not present


## Deployment and System Requirement

As YOLOv5 is a deep nural network so it require good GPU processing 

which is not possible in local system. 

Therefore, we require [GOOGLE Colab](https://colab.research.google.com/drive/1BF6YS6apacdORPHZRop2pMEhWtQLD7eK)

We have to mount the G-drive for better acess of dataset for training and testing purpose

```bash
  from google.colab import drive
drive.mount('/content/drive')
```

To run the juypter notebook provided at `Code\notebook` we have to upload the `Code` folder in drive
## Installation

Install my-project with npm

```bash
  # pip install -r requirements.txt

# Base ----------------------------------------
matplotlib>=3.2.2
numpy>=1.18.5
opencv-python>=4.1.2
Pillow>=7.1.2
PyYAML>=5.3.1
requests>=2.23.0
scipy>=1.4.1
torch>=1.7.0
torchvision>=0.8.1
tqdm>=4.41.0

# Logging -------------------------------------
tensorboard>=2.4.1
# wandb

# Plotting ------------------------------------
pandas>=1.1.4
seaborn>=0.11.0

# Export --------------------------------------
# coremltools>=4.1  # CoreML export
# onnx>=1.9.0  # ONNX export
# onnx-simplifier>=0.3.6  # ONNX simplifier
# scikit-learn==0.19.2  # CoreML quantization
# tensorflow>=2.4.1  # TFLite export
# tensorflowjs>=3.9.0  # TF.js export

# Extras --------------------------------------
# albumentations>=1.0.3
# Cython  # for pycocotools https://github.com/cocodataset/cocoapi/issues/172
# pycocotools>=2.0  # COCO mAP
# roboflow
thop  # FLOPs computation

```
    
## Documentation

The official documentation of YOLOv5 is available at

[YOLOv5](https://github.com/ultralytics/yolov5)


## Dataset 

Dataset is created manually using [makesene.ai](https://www.makesense.ai/)

Images for data is at `CODE\DATA\Images`

Anotated txt of all the image dataset is at  `CODE\DATA\Labels`


## Training of Model 

Run this code in colab cell
```python
 !python train.py --img 640 --batch 16 --epochs 300 --data customdata.yaml --weights yolov5s.pt --cache
```
4 models of YOLOv5 are used
    
    +YOLOv5s 
    +YOLOv5m 
    +YOLOv5l 
    +YOLOv5x
 ![alt text](https://github.com/ultralytics/yolov5/releases/download/v1.0/model_comparison.png)
## Training of Model 

Run this code in colab cell
```python
 !python train.py --img 640 --batch 16 --epochs 300 --data customdata.yaml --weights yolov5s.pt --cache
```
4 models of YOLOv5 are used
    
    +YOLOv5s 
    +YOLOv5m 
    +YOLOv5l 
    +YOLOv5x
 ![alt text](https://github.com/ultralytics/yolov5/releases/download/v1.0/model_comparison.png)
## Testing of dataset

Run this code in colab cell
```python
!python detect.py --weights "/content/drive/MyDrive/Kunal_Python/Code/yolov5/runs/train/exp12/weights/best.pt" --img 640 --conf 0.25 --source "## Source of vedio to be tested"
```
### Trained model
  The model is at `code\YOLOv5\run\train\exp12` for YOLOv5s

  The model is at `code\YOLOv5\run\train\exp13` for YOLOv5m

  The model is at `code\YOLOv5\run\train\exp14` for YOLOv5l

  The model is at `code\YOLOv5\run\train\exp17` for YOLOv5x

  -->`code\YOLOv5\run\train\exp12` contain output images 
  after training of the dataset on that particular model

  
## Output and performance of models

The predicted images and vedios are saved at ` Code\yolov5\detect\.. `

The validated images and vedios features like precision curve, recall curve,mAP curve

is at folder `Code\yolov5\runs\val\exp2`





Run this code in colab cell to generate ouput parameters
```python
!python val.py --weights "/content/drive/MyDrive/Kunal_Python/Code/yolov5/runs/train/exp13/weights/best.pt" --data customdata.yaml --img 640 --iou 0.65 --half --task test
```


## Authors

- [Kunal Shaw](kunals19@iiserb.ac.in)
   
-   [Aman Mishra](amanm19@iiserb.ac.in)

