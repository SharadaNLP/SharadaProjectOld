# Sharada Phase 1
This reposity holds the code to the multiple classifer models trained in the project

 Main Repo -> https://github.com/sud0x00/SharadaProject-Documentation

##### Image segmentation repo can be downloaded from here : https://github.com/sud0x00/SharadaProject-Segmentation

 

Resnet50 model trained for 50 epochs , with Imagenet pretrained weights can be downloaded here :

[ Model Link ](https://drive.google.com/file/d/13OoUbJaizdSv9gMDeucJbBkE5pJGSDn9/view?usp=sharing)


Model achieved 74.5% accuracy.

1. [dictionary_1](https://drive.google.com/file/d/1mL3qDtw4fHf0MUflVEed29K9BnmYYBQo/view?usp=sharing)
2. [dictionary_2](https://drive.google.com/file/d/1AkGj5mpUPuVwfcqxgsU7WR2gXwYSvORH/view?usp=sharing)


[Samples for inference](https://drive.google.com/file/d/1B7NT19IrtS7TKsc7GLwuLkQpEMy8yAH3/view?usp=sharing)


# Reasons for the bad performance

Similar Feature Space : Multiple letters share similar background and similar foreground which results in lack of diverse feature space. This in turn is turning the model into a bad classifier. 

Overfitting & Lack of enough data to train a cnn

# Alternatives already explored :

 1. Creation of a yolo detection model which detects on a character level -> The yolo model fails miserable due to the extreme number of classes
 2. CapsNet -> https://arxiv.org/abs/1710.09829.

# Ways to overcome the above issues 

Sequence modelling using CTC :

Connectionist Temporal Classification(CTC) is an algorithm used to deal with tasks like speech recognition, handwriting recognition etc. where just the input data and the output transcription is available but there are no alignment details provided i.e how a particular region in images for handwriting is aligned to a specific character. Simple heuristics such as giving each character same area won't work since the amount of space each character takes varies in handwriting from person to person and time to time.

Transformer based approach :

https://arxiv.org/abs/2005.13044

