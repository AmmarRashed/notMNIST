# notMNIST
Letter recognition Logistic Regression classifier trained on notMNIST (alphabet A-J)
</br>
<img src="https://camo.githubusercontent.com/a71107803d3190eb032499318ac19f0140a87070/687474703a2f2f7363696b69742d6c6561726e2e6f72672f737461626c652f5f696d616765732f7363696b69742d6c6561726e2d6c6f676f2d6e6f746578742e706e67">
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/11/TensorFlowLogo.svg/2000px-TensorFlowLogo.svg.png" width=200>
- <a href="https://www.udacity.com/">Udacity</a>
  - <a href="https://classroom.udacity.com/courses/ud730"> Intro to Deep Learning</a>
    - <a href="https://github.com/tensorflow/tensorflow/blob/master/tensorflow/examples/udacity/1_notmnist.ipynb">Assignment 1: notMNIST</a>
    - <a href="https://github.com/tensorflow/tensorflow/blob/master/tensorflow/examples/udacity/2_fullyconnected.ipynb">Assignment 2: Fully Connected</a>
    
    - <a href="https://github.com/tensorflow/tensorflow/blob/master/tensorflow/examples/udacity/3_regularization.ipynb">Assignment 3: Regularization</a>
    
    - <a href="https://github.com/tensorflow/tensorflow/blob/master/tensorflow/examples/udacity/4_convolutions.ipynb">Assignment 4: Convulotions</a>
    

## Data
- <a href="http://yaroslavvb.com/upload/notMNIST/"> notMNIST </a>
<img src="https://lh4.googleusercontent.com/proxy/b94FV3AHSfDPdqNvd0PXCXnQLzSZquHEoQqziiMTHOvbuVP3xIjVH92yYzpOCCqqnUOS0PjjFDjMawC905m19Rs=w1200-h630-p-k-no-nu">
529119 28 x 28 grayscale images of letters A - J, sorted into directories by letter. There are 52920 images for letters A - I, and 52919 images for letter J. This dataset is more challenging version of the image classification problem than <a href="http://yann.lecun.com/exdb/mnist/">MNIST</a>: classifying letters from images. It is a multiclass classification dataset of glyphs of English letters A - J.

## Training

Trained using <a href="https://www.zotac.com/sg/product/graphics_card/zotac-geforce-gtx-1070-amp-edition">  Zotac GTX 1070 AMP edition 8GB </a>

- <a href="https://github.com/AmmarRashed/notMNIST/blob/master/sklearn_lr.ipynb"> Sklearn Logistic Regression </a>

  - 84% accuracy
  - <a href="http://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html"> reference</a>

<img src="https://github.com/AmmarRashed/notMNIST/blob/master/misc/sklearn_perf.png?raw=true">

- Full batch: (linear) Logistic Regression with TensorFLow
  - 88% accuracy

<img src="https://github.com/AmmarRashed/notMNIST/blob/master/misc/tf_perf_fullbatch.png?raw=true">

- <a href="https://github.com/AmmarRashed/notMNIST/blob/master/TF_Logistic_Regression.ipynb">Mini batch</a> (linear)
  - 90% accuracy
  - batch_size=1000, took: 155 seconds
  
<img src="https://github.com/AmmarRashed/notMNIST/blob/master/misc/single_layer_lr.png?raw=true">

- <a href="https://github.com/AmmarRashed/notMNIST/blob/master/TF_MLP_relu.ipynb">Mini batch (ReLU) </a>
  - 95% accuracy
  - took: 188 seconds
  <img src="https://github.com/AmmarRashed/notMNIST/blob/master/misc/tf_relu_l2_reg.png?raw=true">

- <a href="https://github.com/AmmarRashed/notMNIST/blob/master/TF_MLP_relu_L2_regularization.ipynb">ReLU with L2-regularization</a>
  - 95.9% accuracy
  - took: 192 seconds
<img src="https://github.com/AmmarRashed/notMNIST/blob/master/misc/tf_relu_dropout.png?raw=true">


- <a href="https://github.com/AmmarRashed/notMNIST/blob/master/TF_MLP_relu_L2_regularization.ipynb">ReLU with dropout+L2-regularization</a>
  - 95.7% accuracy
  - took: 208 seconds
<img src="https://github.com/AmmarRashed/notMNIST/blob/master/misc/tf_relu_dropout.png?raw=true">


- <a href="https://github.com/AmmarRashed/notMNIST/blob/master/ConvNet.ipynb">CNN with dropout+L2-regularization </a> (similar to <a href="http://yann.lecun.com/exdb/lenet/">LeNet</a>)
  - 95.5% accuracy
  - took: 391.5 seconds
<img src="https://github.com/AmmarRashed/notMNIST/blob/master/misc/CNN.png?raw=true">


- <a href="https://github.com/AmmarRashed/notMNIST/blob/master/CNN_Inception.ipynb">CNN inception module </a>
  - concatenation
    - 95.1% accuracy
    - took: 554 seconds
    <img src="https://github.com/AmmarRashed/notMNIST/blob/master/misc/inception_concat.png?raw=true">
  - reduce mean
    - 93.6% accuracy
    - took: 528.5 seconds
<img src="https://github.com/AmmarRashed/notMNIST/blob/master/misc/inception_avg.png?raw=true">

- <a href="https://github.com/AmmarRashed/notMNIST/blob/master/TF_RNN.ipynb">RNN (CPU) </a>
  - 86.5% accuracy
  - took: 589.3 seconds
<img src="https://github.com/AmmarRashed/notMNIST/blob/master/misc/rnn.png?raw=true">


## Libraries

**Tested on Python 3.5**
- <a href="https://www.tensorflow.org/"> TensorFlow </a>
- <a href="http://scikit-learn.org/"> scikit-learn </a>
- <a href="http://www.numpy.org/"> NumPy </a>
- <a href="https://ipython.org/"> IPython</a>
- <a href="https://matplotlib.org/"> Matplotlib</a>
- <a href="https://pythonhosted.org/joblib/"> Joblib (optional)</a>
