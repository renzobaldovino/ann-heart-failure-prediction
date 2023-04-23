# Heart Failure Prediction

Using the __[Heart Dataset](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction)__ from kaggle, we wanted to know if we could create an `artificial neural network` that can predict the possibility of heart failure based on the attributes in the dataset.

This was done through the following steps:

1. Exploratory Data Analysis.
2. Data Preprocessing.

    - Handling Outliers
    - Handling Null Values

3. Label Encoding
4. Splitting of data into Train and Test Datasets.
5. Creating the Artificial Neural Network Model using `Tensorflow`.
6. Evaluating the Model.

## Creating the Artificial Neural Network Model

In order to determine the ideal hyperparameters that will produce the most accurate model. We created a function that uses the `keras_tuner` library to produce **6048** models of varying hyperparameters and accuracy. The varying hyperparameters and its values are as follows:

- **Number of Layers**: 1, 2, 3
- **Nodes per Layer**: 30, 40, 50, 60, 70, 80, 90, 100
- **Batch Size**: 16, 32, 64, 128, 256, 512
- **Epoch**: 50, 100, 200, 300, 400, 500
- **Optimizer**: Adadelta, Adagrad, Adam, Adamax, Nadam, RMSprop, SGD

The resulting models are listed in the `ModelData.csv` file and the model with the highest accuracy was saved and evaluated as a .h5 file.
