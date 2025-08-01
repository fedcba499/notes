## What is YOLO?
- YOLO Stands for You Only Look One.
- Created for Faster Computer vision Tasks.
- Ultralytics created YOLO V5, V8 & v11
- YOLO can handle 5 type of tasks
    - Detection
    - Instance Segmentation (seg)
    - Pose / Keypoints (pose)
    - Oriented Detection /  Oriented Bounding Box (obb)
    - Classification (cls)
- Each Type of tasks of Yolo V11 comes in 5 Varients
  
  Model | No of Parameters (M) | Size (MB) | Speed T4 GPU (ms) | FLOPS (B)
  --- | --- | --- | --- | ---
  YOLO V11n | 2.6 | 5.35 | 1.5 | 6.5
  YOLO V11s | 9.4 | 18.4 | 2.5 | 21.5
  YOLO V11m | 20.1 | 38.8 | 4.7 | 68
  YOLO V11l | 25.3 | 49 | 6.2 | 86.9
  YOLO V11x | 56.9 | 109 | 11.3 | 194.9

## Before training custom data on yonov11n.pt, model size is 5.35 mb, after training on aadhar data set size it still the same. Why?
- yolov11n.pt - Pretrained weights — default weights trained on COCO or another base dataset.
- best.pt - Your trained weights — same architecture, but learned parameters updated based on your dataset.

YOLOv11n (nano) has a fixed architecture with ~2.58 million parameters.
So, both files store weights for the same number of layers and tensors.
Only the values of those parameters (weights, biases, batch norms) are different.
This is why both files are ~5.3 MB, but they encode different model behavior.

> Think of it like saving two versions of the same Excel sheet — same format, different data.

> In Aadhar card, licence plate and helmet we are using object detection model.

## Parameter of YOLO Models
 
```python

!yolo task=detect mode=train \
# Basic Building Blocks
  data={dataset.location}/data.yaml \
  model="yolov11s.pt" \
  epochs=100 \ # Number of times it should look at data
  batch=16 \ # Look 16 images at a time, helps in recognition of pattern, better learining
  imgsz=640 \ # Set to 640 x 640 px
  val=True \ # Progress monitoring - Check for validation, check whether model is improving. Like taking practise test while learning
  patience=15 \ # Smart stopping - Stop, if no improvement for 15 rounds
  device=0 \ # GPU
  cache=True \ # Faster training 
  project="improved_detection" \
  name="better_model_v1" \
  plots=True # Visual progress

# Data Augmentation - These are tricks used to make more variations of your images to help the model generalize better.

auto_augment = randaugment # It automatically applies smart image transformations (like rotating, flipping, etc.). Helps model handle real-world variations.

mosaic = 1.0  # Combines 4 training images into one. Helps detect small objects better.

translate = 0.1 # Randomly moves objects by up to 10% of the image size.

scale = 0.5 # Randomly zooms in or out on the object.

fliplr = 0.5 # 50% chance of flipping the image left to right.

erasing = 0.4 # Randomly removes parts of the image to help the model become more robust.

### Learning Parameters

lr0 = 0.01 # Starting learning rate — how fast the model adjusts its guesses.

momentum = 0.937 # Helps smooth the learning over time.

weight_decay = 0.0005 # Keeps the model from memorizing the training data.

warmup_epochs = 3.0 # For the first 3 epochs, the model starts slowly before speeding up learning.

```
