
# Human Activity Recognition using Smartphones



## Description :
Human Activity Recognition is a Supervised learning problem in which our task is to predict Human
activity from the six Activities : three static activities (standing, laying, and sitting) and three
dynamic activities (walking, walking upstairs, and walking downstairs). We will proceed first with
data cleaning and pre-processing. Then we will perform Feature Selection to select prominent features
from the feature space. After that, we will employ several classification models and select the best
among them to predict class levels of the given test data.

## Dataset :
The Human Activity Recognition dataset was built from the recordings of 30  participants performing activities of daily living while carrying a waist-mounted smartphone with embedded inertial sensors.

There are 563 columns and 8239 data points in the training dataset. Two of these columns contain
activity labels and the subject who performed the experiment. The dataset contains 3-axial linear
acceleration data from the accelerometer, axial angular velocity data from the Gyroscope and estimated
values of mean, std, max, etc derived from the time series data.

## Code description :
The [gourav_sen_code.ipynb](https://github.com/sengourav/Human_Activity_Recognition/blob/main/gourav_sen_code.ipynb) file contains the code for our project. This includes following sections:

#### Data preprocessing :
We start by checking null values or duplicate values in the dataset. We found that there were no null values and duplicate values in the dataset. Also all values lies in between -1 and 1 which ensures that there are no outliers in the data. Then we check whether dataset is balanced or not by looking at the count plot. We found that the dataset is well balanced.

#### EDA :
To get insights into the data , we start 
by creating scatter plots and density plots for various features. Box plots are another tool we use to distinguish between classes and determine the
range of classes for a certain attribute.

Finally, we mapped the 563 dimension feature vector to a 2D
space using the tSNE plot displayed below, and we noticed standing and sitting class are
most hard to classify.

#### Feture Selection :
For feature selection we first start by encoding the class labels.The encoded labels are as follows 2- STANDING,
3- WALKING, 0- LAYING, 4- WALKING DOWNSTAIRS, 1- SITTING, 5-WALKING UPSTAIRS.

We used F1-test, Mutual Information Gain, Extra tree classifier and Correlation Coefficient for feature selection. The feature selection results are listed in the [FEATURE_SELECTION_RESULTS.pdf](https://github.com/sengourav/Human_Activity_Recognition/blob/main/FEATURE_SELECTION_RESULTS.pdf) file.


#### Models :
To find the best-performing algorithm for our HAR task, we experimented with various machine learning models, including:

 - KNN 
 - Logistic Regression 
 - Decision tree 
 - Random Forest
 - Linear
 - SVM 
 To optimize the performance of each model, we conducted hyperparameter tuning using Grid Search Cross-Validation (Grid Search CV). 

 ## Results :
- We found that features selected by Extra tree classifier gave highest performance when tested with several classifiers.
- Among the various machine learning models we explored, the Random Forest classifier delivered the highest performance in terms of macro- F1-score and accuracy.
## Future Enhancements : 
One of the ongoing challenges in our Human Activity Recognition (HAR) project is accurately classifying activities such as sitting and standing. These activities can be particularly tricky to differentiate based solely on smartphone sensor data. The future work will focus on addressing this challenge and improve the overall performance of our HAR model.

## Other Information :
#### Prerequisites:
Before running this project, please ensure you have the following Prerequisites:
- You should have Python 3.x installed on your machine. You can download Python from the. [official website](https://www.python.org/downloads/).
- Install Jupyter notebook.

#### Installation :
The following libraries are required for this project:

- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org/)
- [matplotlib](http://matplotlib.org/)
- [scikit-learn](http://scikit-learn.org/stable/)

You can install jupyter notebook from here - [Jupyter Notebook](http://jupyter.org/install.html) or install the [Anaconda](https://www.anaconda.com/download/) distribution of Python, which already has the above packages and more included. 




