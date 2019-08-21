About
==
 F3RBM-SVM is used to realize feature extraction and recognition of images. Relevant programs and data sets are provided:
------- 
1.“F3RBM-SVM.m”is combination of Fuzzy Removing Redundancy Restricted Boltzmann Machine and Support Vector Machine.<br>
2. “RBM-SVM.m”is combination of Restricted Boltzmann Machine and Support Vector Machine.<br>
3. “SVM.m”is support vector machine (SVM) to realize multifunctional classification.<br>
4. “libsvm-3.22.rar” is an effective software package for SVM pattern recognition and regression to solve multi-class pattern recognition problems. <br>
5. “Mnistdisp.m” is used for image reconstruction after feature extraction to verify the effect of feature extraction.<br>
6. “MNIST_Handwritten_data.mat”is MNIST handwritten database including 60000 training samples and 10000 test samples.<br>
7. “Fashion_MNIST_data.mat”is Fashion MNIST database including 60000 training samples and 10000 test samples.<br>
8. “Olivetti_Faces_data.mat”is Olivetti Faces Data Set, which contains image data without noises and with four different noises. Each type of images contains 240 training samples and 160 test samples.<br>
  Preparation before running 
  1. Download and install LIBSVM software package (libsvm-3.22.rar) 
  2. Download and properly divide the data set into small sample sets of average batches. The MNIST_Handwritten_data.mat, Fashion_MNIST_data.mat and Olivetti_Faces_data.mat have been divided into several small sample sets.
Image reconstruction and classification 
  F3RBM-SVM.m can realize the process of image feature extraction and classification, and the specific steps are as follows:
  1. Parameter initialization
  2. positive phase
  3. negtive phase
  4. Parameter optimization
  5. SVM classification
Taking MNIST_Handwritten_data.mat data set as an example, run F3RBM-SVM.m to get the comparison between the original image and the reconstructed image (odd behavior original image, even behavior reconstructed image) as follows:
 
The classification accuracy is 98.30%±0.05%.
 
How to verify the effectiveness of feature extraction
  Reconstruction errors are used to reflect the effectiveness of feature extraction. During the training iteration, reconstruction errors in each iteration are displayed in the workspace. It can not only reflect the convergence performance of training, but also verify the effectiveness of feature extraction.
 
How to test the classification effect 
  The training samples and test samples are data sets after F3RBM feature extraction. That is to say, the sample data after feature extraction can be obtained by the optimized parameters and the corresponding conditional probability function.
How to improve the classification accuracy of F3RBM-SVM 
  1. Set more iterations until the reconstruction error converges. 
  2. Set more hidden units until the number of hidden units approaches the number of visible units.
  3. When the number of original data samples is relatively small and the dimension of samples is relatively low, improving the threshold of removing redundancy can improve the accuracy of classification.
How to improve the learning speed
  1. Increase the learning rate appropriately, Increase learning rate appropriately, but it is easy to cause non-convergence.
  2. When the sample size of the original data is large and the sample size is large, the learning speed can be improved by appropriately reducing the threshold of eliminating redundancy.

