# mltask

## step 1: finding data
after a few tries,

I was able to acquire the required data by searching lung tidal volume vs age height weight at https://www.kaggle.com/datasets/sulaimanahmed/lung-capacity-data?resource=download

(the data has been sampled from 747 people)

## step 2: building the model 
### Data preprocessing and visualisation
I have converted the available data from CSV format to Numpy and PyTorch tensors
### feature selection
I have chosen not to apply feature selection as there are very few available features
### Performing regression using random forest regressor
By using random forest regressor from Scikit Learn I was able to build a regressor which was able to predict the lung capacity with a mean absolute error of 0.89
### trying to build my regressor using Pytorch
The architecture that I used for my regressor is `12(input)->16->1(output)`.

the model performed poorly on the dataset with a mean absolute error of 2.33 😅

You can access my model by uploading the model parameters provided by running the first and last cell under the heading `2. using PyTorch`

To access the random forest model,

1. upload the data file

2. run all the cells from the start till the last cell under the subheading `1. using random forests`

P.S. My .ipynp file is not able to preview properly. so please first download the file and open the file using Colab to view it

