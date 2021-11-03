# Network-Intrusion-Detection-Using-Deep-Learning

Binary and Multi-Class Classification of NSL-KDD dataset using Multi-Layered Perceptron(MLP).

USER MANUAL:
1.	To run each code, the system must have Anaconda and Jupyter Notebook installed in it.


2.	After installing Anaconda, the packages motioned below must be installed.

               pandas, keras, sklearn, numpy, dill, h5py, matplotlib


List of files:
1.  pre-processing.ipynb // Data Pre-Processing(One hot encoding, label encoding, minmax scaler)

2.  binary_all.ipynb   //Binary Classification of  all features

3.  binary_time.ipynb // Binary Classification for time based feature

4.  binary_host.ipynb // Binary Classification for host-based feature

5.  binary_content.ipynb // Binary Classification for content-based feature

6.  binary_basic.ipynb // Binary Classification for  basic feature

7.  multi_all.ipynb   //Multiclass Classification of  all features

8.  multi_time.ipynb // Multiclass Classification for time-based feature

9.  multi_host.ipynb // Multiclass Classification for host-based feature

10.  multi_content.ipynb // Multiclass Classification for content  based feature

11.  multi_basic.ipynb // Multiclass Classification for  basic feature

12.  classical_binary.ipynb // Binary Classification (using K-nearest neighbor, Decision tree, random forest classifier)

13.  classical_multi.ipynb // Multiclass Classification (using K-nearest neighbor, Decision tree, random forest classifier)


#  Basic modules:

Data Pre-processing:
  The preprocessing of the dataset consists of data Numeralization and Normalization of the original data, which are described below.

Numeralization:
There is a total of 38 numeric features and 3 non-numeric features in the NSL-KDD dataset. As the Deep Neural Network model takes only numeric values, so we have to convert the non-numeric features into the numeric form[5]. In the NSL-KDD dataset, some non-numeric features are ‘protocol type', ‘service’, ‘flag’. These symbolic features include the type of protocol (i.e., TCP, UDP, and ICMP), service type (e.g., HTTP, FTP, Telnet, and so on), and TCP status flag (e.g., SF, REJ, and so on). The method simply replaces the values of the categorical attributes with numeric values as shown in the table below.
  
![](images/Screenshot%202021-01-02%20at%2012.35.50%20AM.png)

Normalization:
The second part is normalization. Since the difference between the maximum and minimum values of some attributes has a very large scope, so these values will be normalized between range [0-1] by using equation-1. Where MAX and MIN are the maximum and minimum values respectively.
  
![](images/3.png)

Training and Testing:
After the pre-processing of the dataset is done, the training dataset will be used to train using MLP, KNN, Decision Tree Classifier, and Random Forest Classifier.

Testing Approaches:
The test datasets were fed to the trained model to predict the attack classes both for ‘Binary Classification’ and ‘Multi-Class Classification’. Using the model’s prediction and the confusion matrix test results were created using ‘train-test’ accuracy graphs and histograms. The role of the confusion matrix[3] for determining the accuracy of binary and multiclass classification results is described below.

Confusion Matrix:
In our model, the most important performance indicator (Accuracy) of intrusion detection is used to measure the performance of the MLP-IDS model. In addition to the accuracy, we introduce the detection rate and false-positive rate. The True Positive (TP) is equivalent to those correctly rejected, and it denotes the number of anomaly records that are identified as an anomaly. 

![](images/4.png)

The False Positive (FP) is the equivalent of incorrectly rejected, and it denotes the number of normal records that are identified as an anomaly. The True Negative (TN) is equivalent to those correctly admitted, and it denotes the number of normal records that are identified as normal. The False Negative (FN) is equivalent to those incorrectly admitted, and it denotes the number of anomaly records that are identified as normal. Table-5.2 shows the definition of the confusion matrix. We have the following notation:

Accuracy: 
The percentage of the number of records classified correctly versus the total number of records is shown in the equation below.

![](images/5.png)

True Positive Rate (TPR): As the equivalent of the Detection Rate (DR), it shows the percentage of the number of records identified correctly over the total number of anomaly records, as shown in the equation below.

![](images/6.png)

False Positive Rate (FPR): The percentage of the number of records rejected incorrectly is divided by the total number of normal records, as shown in the equation below.

![](images/7.png)

Hence, the motivation for the IDS is to obtain a higher accuracy and detection rate with a lower false-positive rate.

Test Reports:

In binary classification, the accuracy table below shows that the basic feature produces the least accuracy for all classifiers. In ‘basic’, ‘host based’, and ‘all’ features, the MLP model shows better accuracy. The accuracy results are non-deterministic in nature because for some features, one classifier works better and for other features, some other classifier produces better results. Although the KNN took a substantial amount of time in both the training and testing process. In binary classification, most of the accuracy results of the classical machine learning classifiers that are used in this project have produced very close results to the MLP classifier.

Histogram comparison of different classifiers in binary classification.

![](images/8.png)

In multi-class classification, the accuracy table shows that content-related feature produces the least accuracy for all classifiers. In ‘all’ and ‘content related’ features the MLP model shows better accuracy. The multi-class classification accuracy shows non-deterministic results similar to the binary classification; because for some features, one classifier works better and for other features some other classifier produces better results. Here also, the KNN took a substantial amount of time in both the training and testing process. In multi class classification, the results of the classical machine learning algorithms and MLP were very close, which is similar to the binary classification results.

Histogram comparison of different classifiers in multiclass classification.
![](images/9.png)

References:

[1] Datasets | Research | Canadian Institute for Cybersecurity | UNB. (n.d.). Canadian Institute for Cybersecurity. Retrieved November 25, 2020, from https://www.unb.ca/cic/datasets/index.html

[2] L.Dhanabal, Dr. S.P. Shantharajah, “A Study on NSL-KDD Dataset for Intrusion Detection System Based on Classification Algorithms”, International Journal of Advanced Research in Computer and Communication Engineering, Vol. 4, Issue 6, June 2015.

[3] Chuanlong yin , Yuefei zhu, Jinlong fei, and Xinzheng he. “A Deep Learning Approach for Intrusion Detection Using Recurrent Neural Networks”, IEEE Access, October 12, 2017.

[4] Schmidhuber, J. (2015). Deep learning in neural networks: An overview. Neural Networks, 61, 85–117. https://doi.org/10.1016/j.neunet.2014.09.003 

[5] Gael Kamdem De Teyou , Junior Ziazet “Convolutional Neural Network for Intrusion Detection System In Cyber Physical Systems”, https://www.researchgate.net/publication/333022621, May 2019.
