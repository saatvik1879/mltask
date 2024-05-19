# mltask

## step 1: finding data
after a few tries,

I was able to acquire the required data by searching lung tidal volume vs age height weight at https://www.kaggle.com/datasets/sulaimanahmed/lung-capacity-data?resource=download

(the data has been sampled from 747 people)

## step 2: preprocessing data
### Data preprocessing and visualisation
I have converted the available data from CSV format to Numpy and PyTorch tensors
### feature selection
I have chosen not to apply feature selection as there are very few available features
###test train split
I have split the dataset with a test_size of 0.25
## step 3: building model
To solve the above problem I chose random forest because it prevents overfitting, thus more accurate than decision trees. My first choice was to build my model using pytorch but that didn't turn out well. I tried various things to improve the performance of my model like adding more hidden layers, increasing nodes in hidden layers, and adding dropout and normalisation layers but nothing seemed to increase the performance.

So, I went for one of the best options to perform regression i.e. random forest using scikit learn. I did consider using XGboost regressor but as random forest provided satisfactory results I didn't bother implementing XGboost.
### Performing regression using random forest regressor
By using random forest regressor from Scikit Learn I was able to build a regressor which was able to predict the lung capacity with a mean absolute error of 0.89

(predictions - true values)
![Alt text](/img1.jpg?raw=true "Optional Title")
### trying to build my regressor using Pytorch
The architecture that I used for my regressor is `12(input)->16->1(output)`.

(predictions - true values)
![Alt text](/img2.jpg?raw=true "Optional Title")

the model performed poorly on the dataset with a mean absolute error of 2.33 😅

You can access my model by uploading the model parameters provided by running the first and last cell under the heading `2. using PyTorch`

To access the random forest model,

1. upload the data file

2. run all the cells from the start till the last cell under the subheading `1. using random forests`

P.S. My .ipynp file is not able to preview properly. so please first download the file and open the file using Colab to view it

