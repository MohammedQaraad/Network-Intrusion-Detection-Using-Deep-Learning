# Network-Intrusion-Detection-Using-Deep-Learning
Binary and Multi-Class Classification of NSL-KDD dataset using Multi Layered Perceptron


#  Basic modules:
Data Pre-processing:
  The preprocessing of dataset consists of data Numeralization and Normalization of the original data, which are described below.

Numeralization:
	There are total 38 numeric features and 3 nonnumeric features in the NSL-KDD dataset. As the Deep Neural Network model takes only numeric value, so we have to convert the non-numeric features into numeric form[5]. In NSL-KDD dataset, some non-numeric features are ‘protocol-type’, ‘service’, ‘flag’. These symbolic features include the type of protocol (i.e., TCP, UDP and ICMP), service type (e.g., HTTP, FTP, Telnet and so on) and TCP status flag (e.g., SF, REJ and so on). The method simply replaces the values of the categorical attributes with numeric values as shown in table below.
  
![](images/Screenshot%202021-01-02%20at%2012.35.50%20AM.png)

Normalization :
  The second part is normalization. Since the difference between the maximum and minimum values of some attributes has a very large scope, so these values will be normalized between range [0-1] by using equation-1. Where MAX and MIN are the maximum and minimum values respectively.

Training and Testing: 
  After the pre-processing of dataset is done, the training dataset will be used to train using the Depp Neural Network. The idea of DNN is roughly described below.

Deep Neural Network:
Deep Neural Networks(DNN) are basically multi-layered structured Artificial Neural Network(ANN) within the input and output layers. DNN has feedforward networks in which data moves across from input layer to the output layer without any feedback. The main reason that DNN will be chosen because, DNN produces much accurate results than ANN(artificial neural network) or any other classical machine learning algorithms and it is blazingly fast. DNN in comparison to  ANN has increasing hierarchy of complexity. DNN first creates a map of virtual neurons and assigns random numeric values or weights, to the connection between them; the inputs and weights are then multiplied and return an output which ranges between 0 to 1. If a particular pattern is accurately recognized, an algorithm would adjust the weights. Using this procedure, the algorithm can decide the correct parameters until the accurate mathematical model is created which fully process the data. The term ‘Deep’ in Deep Learning refers to having more than one layer which is hidden. 
![](images/Screenshot%202021-01-02%20at%2012.34.25%20AM.png)
 
FIGURE 2: DEEP NEURAL NETWORK
  The output layer returns output data in every iteration or epochs. The epochs are continued until a required accuracy is achieved. Once the target accuracy is achieved, the training process is terminated. Next, the trained model will be used along with the test dataset where the detection and classification of different types of attacks will be done. Additionally we will try to extract new features from our existing training dataset, which will be reduced and more efficient representation of the existing dataset.


References:
[1] http://nsl.cs.unb.ca/NSL-KDD/, Last accessed October 2019.

[2] L.Dhanabal, Dr. S.P. Shantharajah, “A Study on NSL-KDD Dataset for Intrusion Detection System Based on Classification Algorithms”, International Journal of Advanced Research in Computer and Communication Engineering,Vol. 4, Issue 6, June 2015.

[3] Chuanlong yin , Yuefei zhu, Jinlong fei, and Xinzheng he. “A Deep Learning Approach for Intrusion Detection Using Recurrent Neural Networks”,IEEE Access, date of publication October 12, 2017.

[4] J. Schmidhuber, “Deep learning in neural networks: An overview,”Neural Netw., vol. 61, pp. 85_117, Jan. 2015.

[5] Gael Kamdem De Teyou , Junior Ziazet “Convolutional Neural Network for Intrusion Detection System In Cyber Physical Systems”, https://www.researchgate.net/publication/333022621, May 2019.
