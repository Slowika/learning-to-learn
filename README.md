# Neural network learning of object categories from canonicalized feature representations

In this project, we train a neural network on artificial toy data for the task
of object recognition. Each sample is represented by a shape,
color and texture value.

## Requirements & Setup
This code repository requires Keras and TensorFlow. Keras must be
configured to use TensorFlow backend. A full list of requirements can be found
in `requirements.txt`. After cloning this repository, it is recommended that
you add the path to the repository to your `PYTHONPATH` environment variable
to enable imports from any folder:

    export PYTHONPATH="/path/to/toy-neuralnet:$PYTHONPATH"


## Repository Structure
The repository contains 3 folders:

### 1. Data
This is where the artificial toy data sets will be saved to and loaded from.

### 2. Notebooks
This folder contains a collection of Jupyter Notebooks for various small tasks,
such as synthesizing the artificial data sets and wrangling the data once
synthesized.

### 3. Toy-neuralnet
This folder contains core reusable source code for the experiments.

### 3. Scripts
This folder contains short Python scripts for running some experiments. Here
you will find scripts for training a neural network model and evaluating its
performance.

## Demo

To run train_nn.py from the scripts folder, you must indicate the data file and
the labels file to use for training. The command might look as follows:

    python train_nn.py -d ../data/objects.csv -l ../data/labels.csv


## Results (in progress)

For the first experiments, I used a single-layer perceptron with 30 hidden
units. The datasets were one-hot-encoded, meaning that there is one element in
the input vector for each possible feature category.

data set: 10 categories, 2 exemplars per category, 10 textures, 10 colors \
result: 100% classification accuracy after 68 epochs

data set: 100 categories, 5 exemplars per category, 20 textures, 20 colors \
result: 100% classification accuracy after 63 epochs

data set: 1000 categories, 10 exemplars per category, 20 textures, 20 colors \
result: 100% classification accuracy after 50 epochs