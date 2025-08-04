## What is FLOPS (B)
- Hardware FLOPS stands for Floating-Point Operations Per Seconds.
- Model FLOPS stand for Floating Point Operations
- How many billion mathematical operations the model performs for one forward pass (one input image)
> FLOPs = how much work the model does when you give it 1 image

## Public Datasets
- ImageNet Dataset has 14 million images accross 20k Categories
- COCO (Common Objects in COntext) Dataset has 80 different type of object, it comes in various sizes
- CIFAR-10 / 100 (Canadian Institute For Advanced Research) contain 60k images accross 10 / 100 categories of 32 x 32 Pixels.
- DOTA (Dataset for Object deTection in Aerial Images) has 15 Categories
- fashionMNIST

## What is TorchVision?
TorchVision is a component of PyTorch, which provides pre-trained models, datasets and utility functions to simplify the development process.
- **Pre-trained Models** : ResNet, VGG, Inception etc
- **Datasets** : CIFAR-10. CIFAR-100, COCO, MNIST etc
- **Data Tranformtion** : Image Resizing, Cropping, Rotation, Normalization, Enhancing the Quality etc
- **Object Detect and Segmentation** : Faster R-CNN, Mask R-CNN models etc

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

## The Activation Function (Decision Making)
The activation function is like your brain's final decision-making step. It takes that total influence and decides:

- If the number is high enough → "Yes, go outside!"
- If it's too low → "No, stay inside"

Think of it as your personal threshold. Maybe you go outside if the total is above 50, stay inside if below.

### Learning Mechanism
During training, weights are updated iteratively through optimization algorithms like gradient descent to minimize the difference between predicted and actual outcomes.

## What is Bias?
Even before anything happens in our day, we might naturally lean toward being happy or grumpy. Thats our "bias" - out starting emotional state. Then daily events (inputs) push us up or down from there.

y = mx + b
- m = weight (slope)
- x = input
- b = bias

## What is a Quantized Model?
A quantized model is a compressed version of your trained model, where floating point numbers (32-bit) are converted into smaller numbers, like 8-bit integers (int8).

### Types of Quantization 
- Dynamic Quantization	Only weights are quantized (int8)	Good, fast, easy
- Static Quantization	Weights + activations are int8	More accurate but complex
- Quantization Aware Training (QAT)	Trained with quantization in mind	Best accuracy, slow to train

For YOLO, dynamic or static quantization is often used after training.

## What is ONXX
ONNX stands for Open Neural Network Xchange
 It’s like exporting a Word document as PDF — any device can open it the same way.

## What Are Visual Question Answering (VQA) Models?
Visual Question Answering (VQA) Models takes image and text (prompt) as input, and outputs text based answer.

> What is the color of car in image?
> Is person on bike wearing helmet?

It is multi model arcitecture. 
CNN / Tranformer models for image detection.
LLM models for text generation.
It combines both of them and produce results.

- Gemma 3n
- PaliGemma
- LLaVA
- CogVLM
- InstructBLIP
- DonutBase
- BLIP-2


ReLU - Rectified Linear Unit
Back Propagation to improve accuracy to self learn
Neurons
    input layer
    hidden layer ( apply formula to input in each layer )
    output layer

torchvision is python package consists of popular datasets
Transformers is type of nueral network deals with sequential data. (Like Text, Voice etc) process data in Parallel (faster)
    Self Attention Mechanism ( If you are in busy room, trying to listen to voice )
    This method pays more attention to relevant information, and gets meaningful output
   Think about how you understand this sentence: "The trophy wouldn't fit in the suitcase because it was too big." What does "it" refer to — the trophy or the suitcase? For humans, context makes it clear that "it" refers to the trophy. Transformers can make these connections too, thanks to their attention mechanism.
 
types of neural network - Transformers, RNN (Recurrent Neural Network), CNN ( Convolutional Neural Network)
GPT is type of Transformer (Generative Pretrained Transformer)

Positional Encoding - Position of word in sentence
    Since the Transformer processes all tokens (words) simultaneously, it needs a way to understand their order. This is where positional encoding comes in — additional information added to each embedding that indicates its position in the sequence. Without positional encoding, the sentence "dog bites man" would be indistinguishable from "man bites dog".

Multi Head Attention 
    Think of multi-head attention like having several people read the same text, each focusing on different aspects:
     One person might focus on syntactic relationships
     Another might capture semantic similarities 
     A third might identify subject-object relationships.

Encoder - Decoder

Softmax Activation Function in Neural Networks
Q.    What is Activation Function in Neural Networks

Embedding - Words to Vectors ( Numbers)
Static Embeddings - GloVe (Global Vector) Word2Vec are certain Techniques
Contextual Embeddings
       