Download Link: https://assignmentchef.com/product/solved-cse575-project1-density-estimation-and-classification
<br>
: Density Estimation and Classification

In this part, you need to first perform parameter estimation for a given dataset (which is a subset from the MNIST dataset). The MNIST dataset contains 70,000 images of handwritten digits, divided into 60,000 training images and 10,000 testing images. We use only images for digit “7” and digit “8” in this question.

Therefore, we have the following statistics for the given dataset:

Number of samples in the training set:  “7”: 6265 ;”8″: 5851.

Number of samples in the testing set: “7”: 1028;   “8”: 974

You are required to extract the following two features for each image:

<ol>

 <li>The average of all pixel values in the image</li>

 <li>The standard deviation of all pixel values in the image</li>

</ol>

We assume that these two features are independent, and that each image (represented by a 2-D features vector) is drawn from a 2-D normal distribution.

<a href="http://yann.lecun.com/exdb/mnist/">You may go to the original MNIST dataset (available here</a><a href="http://yann.lecun.com/exdb/mnist/"> http://</a><a href="http://yann.lecun.com/exdb/mnist/">y</a><a href="http://yann.lecun.com/exdb/mnist/">ann.lecun.com/exdb/mnist/ </a><a href="http://yann.lecun.com/exdb/mnist/">(</a><a href="http://yann.lecun.com/exdb/mnist/">Links to an external site.)</a><a href="http://yann.lecun.com/exdb/mnist/"><strong> (http://</strong></a><a href="http://yann.lecun.com/exdb/mnist/"><strong>y</strong></a><a href="http://yann.lecun.com/exdb/mnist/"><strong>ann.lecun.com/exdb/mnist/) </strong></a><a href="http://yann.lecun.com/exdb/mnist/">) to extract the images for digit 7 and digit 8, to form t</a>he dataset for this project. To ease your effort, we have also extracted the necessary images, and store them in “mnist_data.mat” files. The file can be downloaded <a href="https://asu.instructure.com/courses/31489/files/7881772/download?wrap=1"><strong>here.</strong></a> A description of the file can be downloaded <a href="https://asu.instructure.com/courses/31489/files/7882575/download?wrap=1"><strong>here</strong></a>

<a href="https://asu.instructure.com/courses/31489/files/7882575/download?wrap=1">.</a>

You may use the following piece of code to read the dataset: import scipy.io

Numpyfile= scipy.io.loadmat(‘mnist_data.mat’)

The specific algorithmic tasks you need to perform for this part of the project include:

<ol>

 <li>Extracting the features and then estimating the parameters for the 2-D normal distribution for each digit, using the training data. Note: You will have two distributions, one for each digit.</li>

 <li>Use the estimated distributions for doing Naïve Bayes classification on the testing data. Report the classification accuracy for both “7” and “8” in the testing set.</li>

 <li>Use the training data to train a Logistic Regression model using gradient ascent. Report the classification accuracy for both “7” and “8” in the testing set.<strong> Note that you are not allowed to use package like sklearn to compute the boundary. You need to implement your own version for using gradient ascent to find the solution.</strong></li>

</ol>

<strong>Algorithms:</strong>

MLE Density Estimation, Naïve Bayes classification, Logistic regression

<strong>Resources:  </strong>

<a href="http://yann.lecun.com/exdb/mnist/">A subset of MNIST dataset, download either from</a><a href="http://yann.lecun.com/exdb/mnist/"> http://</a><a href="http://yann.lecun.com/exdb/mnist/">y</a><a href="http://yann.lecun.com/exdb/mnist/">ann.lecun.com/exdb/mnist/ </a><a href="http://yann.lecun.com/exdb/mnist/">(</a><a href="http://yann.lecun.com/exdb/mnist/">Links to an external site.)</a><u>    </u><a href="http://yann.lecun.com/exdb/mnist/"><strong> (http://</strong></a><a href="http://yann.lecun.com/exdb/mnist/"><strong>y</strong></a><a href="http://yann.lecun.com/exdb/mnist/"><strong>ann.lecun.com/exdb/mnist/) </strong></a><a href="http://yann.lecun.com/exdb/mnist/">(requiring you to extract data corresponding to digit 7 and digit </a>8 only),  or from the .mat files provided.

<strong>Workspace: </strong>

Any Python programming environment.

<strong>Software: </strong>

Python environment.

<strong>Language(s): </strong>

Python. (MATLAB is equally fine, if you have access to it.)

<strong>Required Tasks:</strong>

<ol>

 <li>Write code to extract features for both training set and testing set.</li>

 <li>Write code to implement the Naive Bayes Classifier and use it produce a predicted label for eachtesting sample.</li>

 <li>Write code to implement the Logistic Regression and use it produce a predicted label for each testingsample.</li>

 <li>Write code to compute the classification accuracy, for both the Naive Bayes Classifier and LogisticRegression.</li>

 <li>Write a short report summarizing the results, including the final classification accuracy.</li>

</ol>

<strong>Note that you are not allowed to use package like sklearn to compute the boundary.</strong>

<strong>Optional Tasks:</strong>

<ol>

 <li>Repeat the experiments for different pairs of digits.</li>

 <li>Consider doing multi-class classification.</li>

</ol>

Optional tasks are to be explored on your own if you are interested and have extra time for them. No submission is required on the optional tasks. No grading will be done even if you submit any work on the optional tasks. No credit will be assigned to them even if you submit them. (So, please do not submit any work on optional tasks.)