**********  Scientific Document Classification  **********

In this project, we work with ArXiv scientific abstract dataset in order to
predict the class of a given abstract as a multiclass text classification
problem. We have two datasets, one for training and the other for testing the
model performance on the Kaggle competition.

Training data: 29678 rows with labels
Test data: 7410 rows without labels

*** --- ***
Project Description:

In this project, I performed Natural Language Processing(NLP) over the abstracts
and extract multiple features and train the model of our choice using those
features. Once trained, we predict the class of abstracts on the test dataset.

*** --- ***
Which model?
Here, I am performing a hierarchical classification with Support Vector Machine
Classifier. Firstly we performed preprocessing on the abstracts and then we
extracted TF-IDF as features.

Hierarchical approach:
I split the dataset based on the high-level label class and the sub-label class.

For example, in the label, "q-fin.EC", q-fin, is the main label class and 'EC' is the sub label class.

(a) First level: After splitting the labels into two, I learned that there are 8 main label classes.
    Then I trained the machine on the 8 main label classes at the same time.
(b) Second level: Once the training on 8 main label classes is completed, I trained the
    machine again on the sub level labels, separately for each main label class,
    i.e., each main label has different sub level labels.

Once, the training is done, I ran the code using the labels for test dataset and achieved 56.45% accuracy

*** --- ***
Software/Hardware requirements:

     OS : Windows 7 or above(64-bit)
          Linux Ubuntu 16 or above(64-bit)
 Python : 3.5+
 Memory : 8 GB or more
 Anaconda Jupyter Notebook or Google Colab

*** --- ***
Dependencies/ Packages:
Packages in python you require to run this code:
(i) pandas : For reading and performing multiple operations on the datasets
(ii) re : For collecting data and removing unnecessary things like punctuations from the data
(iii) sklearn : For importing model (SVM) and performing feature extraction(TF-IDF)
(iv) nltk : For natural language related operations like stopword removal, stemming, lemmatisation
(v) string : For string related operations on the abstracts
(vi) pickle : To save the models onto drive

*** --- ***
How to install the dependencies?

You can install Anaconda from :  https://www.anaconda.com/products/individual for free.
It automatically installs Jupyter Notebook. Once installed the required packages can be installed using the below given pip commands in the cells of Jupyter Notebook.
!pip install pandas
!pip install regex
!pip install nltk
!pip install sklearn

*** --- ***
How to run the model?
Load the group26_ass2_impl.ipynb file onto either Google colab or a Jupyter Notebook.
Run the cells in a sequential manner by typing "Shift + Enter"
