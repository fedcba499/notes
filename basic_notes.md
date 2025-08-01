## What is decorator?
Decorate mean to enhance the appearance of something by adding something unessential.
- Painting building
- Adding lights, screens etc to event

> Decorator in Python implies - a function that takes another function as an argument and returns a new function with enhanced functionality.

## What is requirement of VIrtual Environments?
The more Python projects you have, the more likely it is that you need to work with different versions of Python libraries, or even different version of Python itself. Newer versions of libraries for one project can break compatibility in another project.

Virtual environments are used to create independent groups of Python libraries, one for each project. Packages installed for one project will not affect other projects or the operating system’s packages.

## Web Apps Python Library

Streamlit | For Single Page Web Apps ( Interactive)
--- | --- 
Gradio | Mainly used displaying ML Models
Flask | Multiple Web Pages, has routing feature 

## Python Library for OCR

pytesseractOCR | Light | Less Accurate
--- | --- | ---
EasyOCR | Medium | Good Accuracy
PaddleOCR | Heavy | Best Accurarcy

## What is FLOPS (B)
- Hardware FLOPS stands for Floating-Point Operations Per Seconds.
- Model FLOPS stand for Floating Point Operations
- How many billion mathematical operations the model performs for one forward pass (one input image)
> FLOPs = how much work the model does when you give it 1 image

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

## Public Datasets
- ImageNet Dataset has 14 million images accross 20k Categories
- COCO (Common Objects in COntext) Dataset has 80 different type of object, it comes in various sizes
- CIFAR-10 / 100 (Canadian Institute For Advanced Research) contain 60k images accross 10 / 100 categories
- DOTA (Dataset for Object deTection in Aerial Images) has 15 Categories

# What is yaml ?
YAML is to create configuration files. It's recommended that configuration files be written in YAML rather than JSON, even though they can be used interchangeably in most cases, because YAML has better readability (like Python Syntax, white space) and is more user-friendly.  


```yaml
# A sample yaml file
company: spacelift
domain:
 - devops
 - devsecops
tutorial:
  - yaml:
      name: "YAML Ain't Markup Language"
      type: awesome
      born: 2001
  - json:
      name: JavaScript Object Notation
      type: great
      born: 2001
  - xml:
      name: Extensible Markup Language
      type: good
      born: 1996
author: omkarbirade
published: true
```

## What is Epoches ?
In machine learning, an epoch refers to one complete pass through the entire training dataset where every data sample is passed through the model and its parameters are updated based on the calculated error. 

The training process requires multiple epochs, allowing the model to improve iteratively by adjusting its parameters based on the calculated error.

## What are Weights?
**Purpose:** During forward propagation, inputs are multiplied by their respective weights before being passed through an activation function. This influences how strongly each input contributes to the final output. 
> Like, we did in course grading prediction model, where each parameter like (married or unmarried, trade, state etc ) each column or parameter to be multiplied with certain weight based on its influence on final outcome.

Imagine you're trying to decide whether to go outside based on different factors:
### Your Inputs (Information):
- Temperature: 75°F
- Chance of rain: 20%
- Wind speed: 5 mph

### But Not All Factors Matter Equally
Some factors are more important to you than others. In neural networks, we call this importance "weights."

### Your Personal Weights (How Much You Care):
- Temperature importance: Very high (weight = 0.8)
- Rain chance importance: Medium (weight = 0.5)
- Wind speed importance: Low (weight = 0.2)

### The Multiplication Step
Now we multiply each input by how much it matters to you:
- Temperature influence = 75 × 0.8 = 60
- Rain influence = 20 × 0.5 = 10
- Wind influence = 5 × 0.2 = 1

Total influence = 60 + 10 + 1 = 71

## The Activation Function (Decision Making)
The activation function is like your brain's final decision-making step. It takes that total influence (71) and decides:

- If the number is high enough → "Yes, go outside!"
- If it's too low → "No, stay inside"

Think of it as your personal threshold. Maybe you go outside if the total is above 50, stay inside if below.

### Learning Mechanism
During training, weights are updated iteratively through optimization algorithms like gradient descent to minimize the difference between predicted and actual outcomes.


## Best Practises of Python
### Requirements File 
It is good method to use requirements file to use for listing dependency library. In future if we want to rerun program we can uses same set of library which were functional.

### Virtual Environment 
It is good practise to create separate Virtual environment for each project so that has its own dependent library in separate  folder can be added to gitignore.

### Version Control 
To test and add to Main Brach.

## What is IPython?
IPython stands for Interactive Python is an enhanced interactive Python shell designed for interactive computing and exploratory data analysis.

## Before training custom data on yonov11n.pt, model size is 5.35 mb, after training on aadhar data set size it still the same. Why?
- yolov11n.pt - Pretrained weights — default weights trained on COCO or another base dataset.
- best.pt - Your trained weights — same architecture, but learned parameters updated based on your dataset.

YOLOv11n (nano) has a fixed architecture with ~2.58 million parameters.
So, both files store weights for the same number of layers and tensors.
Only the values of those parameters (weights, biases, batch norms) are different.
This is why both files are ~5.3 MB, but they encode different model behavior.

> Think of it like saving two versions of the same Excel sheet — same format, different data.

In Aadhar card, licence plate and helmet we are using object detection model.

```python

!yolo task=detect mode=train \
  data={dataset.location}/data.yaml \
  model="yolov11s.pt" \
  epochs=100 \ ( number of times it should look at data)
  batch=16 \ ( look 16 images at a time, helps in recognition of pattern, better learining)
  imgsz=640 \ (set to 640 x 640 px) 
  val=True \ ( Progress monitoring - Check for validation, check whether model is improving. Like taking practise test while learning)
  patience=20 \ (Smart stopping - Stop, if no improvement for 20 rounds )
  device=0 \ (GPU)
  cache=True \ (Faster training )
  project="improved_detection" \
  name="better_model_v1" \
  plots=True (Visual progress )
```

🏗️ Basic Building Blocks
1. Model
model = yolov8n.pt
You are using YOLOv8n, where n stands for nano (small and fast, good for beginners).

.pt is a PyTorch model file. You're starting from a pre-trained model that already knows general shapes.

2. Dataset
data = /content/Helmet-Detection-2/data.yaml
This file tells YOLO where your training and validation images are.

It also lists the names of the objects (like “helmet”).

3. Training Duration
epochs = 100
One epoch = one full pass through your dataset.

You’ll train for 100 passes to let the model learn better.

4. Image Size
imgsz = 640
All images are resized to 640 x 640 pixels before training.

This keeps the training stable and fast.

5. Batch Size
batch = 16
16 images are processed at a time.

A bigger batch trains faster but uses more memory.

6. Device
device = 0
It means you’re using the first GPU in your system (GPU index 0).

If you were using CPU, this would be device=cpu.

🎨 Data Augmentation
These are tricks used to make more variations of your images to help the model generalize better.

1. auto_augment = randaugment
It automatically applies smart image transformations (like rotating, flipping, etc.).

Helps model handle real-world variations.

2. mosaic = 1.0
Combines 4 training images into one. Helps detect small objects better.

3. translate = 0.1
Randomly moves objects by up to 10% of the image size.

4. scale = 0.5
Randomly zooms in or out on the object.

5. fliplr = 0.5
50% chance of flipping the image left to right.

6. erasing = 0.4
Randomly removes parts of the image to help the model become more robust.

🧠 Learning Parameters
These control how the model learns.

1. lr0 = 0.01
Starting learning rate — how fast the model adjusts its guesses.

2. momentum = 0.937
Helps smooth the learning over time.

3. weight_decay = 0.0005
Keeps the model from memorizing the training data.

4. warmup_epochs = 3.0
For the first 3 epochs, the model starts slowly before speeding up learning.

📂 Saving and Logging
These control what gets saved and where.

1. project = improved_detection
2. name = better_model_v1
Your model and results will be saved under a folder:

improved_detection/better_model_v1/
3. save = True
It saves trained models, graphs, etc.

4. save_dir = improved_detection/better_model_v1
This is the exact folder where your model will be saved.

🧪 Evaluation & Validation
These settings help you test how good your model is.

1. val = True
YOLO will evaluate your model on validation images after each epoch.

2. patience = 20
If the model doesn’t improve after 20 epochs, it stops training early.

⚡ Speed Boost Options
1. amp = True
Uses mixed precision training (faster and uses less GPU memory).

2. cache = True
Loads images into memory to speed up training.

3. workers = 8
Uses 8 CPU threads to load data in parallel.

 What is a Quantized Model?
A quantized model is a compressed version of your trained model, where floating point numbers (32-bit) are converted into smaller numbers, like 8-bit integers (int8).

Types of Quantization 
Dynamic Quantization	Only weights are quantized (int8)	Good, fast, easy
Static Quantization	Weights + activations are int8	More accurate but complex
Quantization Aware Training (QAT)	Trained with quantization in mind	Best accuracy, slow to train

For YOLO, dynamic or static quantization is often used after training.

ONNX stands for Open Neural Network Xchange
 It’s like exporting a Word document as PDF — any device can open it the same way.
