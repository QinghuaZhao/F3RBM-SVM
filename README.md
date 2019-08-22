About
==
F3RBM-SVM is used to realize feature extraction and recognition of images. 
 ----
 Relevant programs and data sets are provided:
------- 
* [F3RBM-SVM.m](https://github.com/shhdl/F3RBM-SVM/edit/master/F3RBM-SVM.m) is a main program that combines F3RBM and SVM to implement the function of feature extraction and classification of images.<br>
* [RBM-SVM.m](https://github.com/shhdl/F3RBM-SVM/edit/master/RBM-SVM.m) is a code that combines RBM and SVM to implement the function of feature extraction and classification of images.<br>
* [SVM.m](https://github.com/shhdl/F3RBM-SVM/edit/master/SVM.m) is support vector machine to realize multifunctional classification.<br>
* [libsvm-3.22.rar](https://github.com/shhdl/F3RBM-SVM/edit/master/libsvm-3.22.rar) is an effective software package for SVM pattern recognition and regression to solve multi-class pattern recognition problems. <br>
* [mnistdisp.m](https://github.com/shhdl/F3RBM-SVM/edit/master/mnistdisp.m） is used for image reconstruction after feature extraction to verify the effect of feature extraction.<br>
* [MNIST_Handwritten_data.mat](https://github.com/shhdl/F3RBM-SVM/edit/master/MNIST_Handwritten_data.mat)is MNIST handwritten database including 60000 training samples and 10000 test samples.<br>
* [Fashion_MNIST_data.mat](https://github.com/shhdl/F3RBM-SVM/edit/master/MNIST_Handwritten_data.mat) is Fashion MNIST database including 60000 training samples and 10000 test samples.<br>
* [Olivetti_Faces_data.mat](https://github.com/shhdl/F3RBM-SVM/edit/master/MNIST_Handwritten_data.mat) is Olivetti Faces Data Set, which contains image data without noises and with four different noises. Each type of images contains 240 training samples and 160 test samples.<br>

Preparation before running
----
 * Download and install LIBSVM software package ([libsvm-3.22.rar](https://github.com/shhdl/F3RBM-SVM/edit/master/libsvm-3.22.rar)) 
 * Download and properly divide the data set into small sample sets of average batches. The [MNIST_Handwritten_data.mat](https://github.com/shhdl/F3RBM-SVM/edit/master/MNIST_Handwritten_data.mat), [Fashion_MNIST_data.mat](https://github.com/shhdl/F3RBM-SVM/edit/master/MNIST_Handwritten_data.mat) and [Olivetti_Faces_data.mat](https://github.com/shhdl/F3RBM-SVM/edit/master/MNIST_Handwritten_data.mat) have been divided into several small sample sets.<br>

Image reconstruction and classification 
----
 [F3RBM-SVM.m](https://github.com/shhdl/F3RBM-SVM/edit/master/F3RBM-SVM.m) can realize the process of image feature extraction and classification, and the specific steps are as follows:
   `Parameter initialization`<br>
   `positive phase`<br>
   `negtive phase`<br>
   `Parameter optimization`<br>
   `SVM classification`<br>
Taking MNIST_Handwritten_data.mat data set as an example, run F3RBM-SVM.m to get the comparison between the original image and the reconstructed image (odd behavior original image, even behavior reconstructed image) as follows
<div align=center><img src="https://github.com/shhdl/F3RBM-SVM/blob/master/Comparison%20of%20original%20and%20reconstructed%20images.png"/></div><br>
The classification accuracy is 98.30%±0.05%.<br>
<div align=center><img src="https://github.com/shhdl/F3RBM-SVM/blob/master/View%20of%20classification%20accuracy.png"/></div>
How to verify the effectiveness of feature extraction
----
  Reconstruction errors are used to reflect the effectiveness of feature extraction. During the training iteration, reconstruction errors in each iteration are displayed in the workspace. It can not only reflect the convergence performance of training, but also verify the effectiveness of feature extraction.<br>
 
How to test the classification effect
----
The training samples and test samples are data sets after F3RBM feature extraction. That is to say, the sample data after feature extraction can be obtained by the optimized parameters and the corresponding conditional probability function.<br>

How to improve the classification accuracy of F3RBM-SVM 
-----
* Set more iterations until the reconstruction error converges.<br> 
* Set more hidden units until the number of hidden units approaches the number of visible units.<br>
* When the number of original data samples is relatively small and the dimension of samples is relatively low, improving the threshold of removing redundancy can improve the accuracy of classification.<br>

How to improve the learning speed
---
* Increase the learning rate appropriately, Increase learning rate appropriately, but it is easy to cause non-convergence.<br>
* When the sample size of the original data is large and the sample size is large, the learning speed can be improved by appropriately reducing the threshold of eliminating redundancy.<br>

