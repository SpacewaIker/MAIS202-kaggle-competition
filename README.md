# MAIS202-kaggle-competition [colab link](https://colab.research.google.com/drive/15pORIX2VSS85hrqiU7rdzacePyGbK5nH?usp=sharing)
The goal of this kaggle competition was to write or use an ML algorithm to predict images from the Fashion-MNIST database. The training and testing datasets were specific to this competition, with the training dataset having a size of 50 000.

# The model
The model I used to generate the final results is a convolutional neural network (CNN), based on a few other CNNs I found. The references are in the Jupyter notebook. 

The model is made of three main blocks and a flatten-dense block at the end. The main blocks are each composed of two convolutional layers and a max pooling layer, with batch normalization and dropout layers. The activation function used is the exponential linear unit (ELU). The flatten-dense block is composed of two dense layers, also with batch normalization and dropout layers.

# Results
This model achieved the following results:
|Epochs |Accuracy (half) | Accuracy (full)|
|-------|----------------|----------------|
|40     |0.91140         |0.-----         |
|50     |0.91300         |0.-----         |
|60     |0.91340         |0.-----         |

The "accuracy (half)" column represents the testing accuracy on the temporary leaderboard for the competition, which used approximately 50% of the testing data.

# The code
The Jupyter notebook is available as a file in the repository and [at this link on Google Colab](https://colab.research.google.com/drive/15pORIX2VSS85hrqiU7rdzacePyGbK5nH?usp=sharing).

*The usage of GPUs to accelerate runtime is strongly recommended.*

## Running the Jupyter notebook
To run the code, run each cell in order. A few notes:

- Using GPUs on Colab: GPUs should be automatically allocated when clicking on "Connect". If not, go to Runtime > Change Runtime Type > Hardware accelerator > GPU > Save.
- The `VALIDATION` variable: this variable determines whether or not a train/validation split is done. If set to true, 20% of the training data will be used as validation data. The results mentioned above were gotten with `VALIDATION = False`.

All other cells should run without any problem.
