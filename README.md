# Developing an Image Classifier using Pretrained Model

Project code for Udacity's AI Programming with Python Nanodegree program. In this project, we developed code for an image classifier built with PyTorch, then converted it into a command line application.


- `torchvision` transforms are used to augment the training data with random scaling, rotations, mirroring, and/or cropping
- The training, validation, and testing data is appropriately cropped and normalized
- The data for each set is loaded with `torchvision`'s `DataLoader`
- The data for each set (train, validation, test) is loaded with torchvision's `ImageFolder`
- A pretrained network such as `VGG16` is loaded from `torchvision.models` and the parameters are frozen
- A new feedforward network is defined for use as a classifier using the features as input
- The parameters of the feedforward classifier are appropriately trained, while the parameters of the feature network are left static
- The network's accuracy is measured on the test data
- During training, the validation loss and accuracy are displayed
- There is a function that successfully loads a checkpoint and rebuilds the model
- The trained model is saved as a checkpoint along with associated hyperparameters and the class_to_idx dictionary
- The process_image function successfully converts a PIL image into an object that can be used as input to a trained model
- The predict function successfully takes the path to an image and a checkpoint, then returns the top K most probably classes for that image
- A `matplotlib` figure is created displaying an image and its associated top 5 most probable classes with actual flower names
- `train.py` successfully trains a new network on a dataset of images and saves the model to a checkpoint
- The training loss, validation loss, and validation accuracy are printed out as a network trains
- The `predict.py` script successfully reads in an image and a checkpoint then prints the most likely image class and it's associated probability
- The `predict.py` script allows users to print out the top K classes along with associated probabilities
- The `predict.py` script allows users to load a JSON file that maps the class values to other category names
- The `predict.py` script allows users to use the GPU to calculate the predictions