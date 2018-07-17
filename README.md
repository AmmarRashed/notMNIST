# notMNIST
Letter recognition Logistic Regression classifier trained on notMNIST (alphabet A-J)

- <a href="https://www.udacity.com/">Udacity</a>
  - <a href="https://classroom.udacity.com/courses/ud730"> Intro to Deep Learning</a>
    - <a href="https://github.com/tensorflow/tensorflow/blob/master/tensorflow/examples/udacity/1_notmnist.ipynb">Assignment 1</a>
    - <a href="https://github.com/tensorflow/tensorflow/blob/master/tensorflow/examples/udacity/2_fullyconnected.ipynb">Assignment 2</a>

## Data
- <a href="http://yaroslavvb.com/upload/notMNIST/"> notMNIST </a>
<img src="https://lh4.googleusercontent.com/proxy/b94FV3AHSfDPdqNvd0PXCXnQLzSZquHEoQqziiMTHOvbuVP3xIjVH92yYzpOCCqqnUOS0PjjFDjMawC905m19Rs=w1200-h630-p-k-no-nu">
529119 28 x 28 grayscale images of letters A - J, sorted into directories by letter. There are 52920 images for letters A - I, and 52919 images for letter J. This dataset is more challenging version of the image classification problem than <a href="http://yann.lecun.com/exdb/mnist/">MNIST</a>: classifying letters from images. It is a multiclass classification dataset of glyphs of English letters A - J.

## Training

Trained using <a href="https://www.zotac.com/sg/product/graphics_card/zotac-geforce-gtx-1070-amp-edition">  Zotac GTX 1070 AMP edition 8GB </a>

- <a href="http://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html"> Sklearn Logistic Regression </a>

  - 84% accuracy

<img src="https://github.com/AmmarRashed/notMNIST/blob/master/misc/sklearn_perf.png?raw=true">

- Full batch: (linear) Logistic Regression with TensorFLow
  - 88% accuracy

<img src="https://github.com/AmmarRashed/notMNIST/blob/master/misc/tf_perf_fullbatch.png?raw=true">

- Mini batch (linear)
  - 90% accuracy
  - batch_size=1000, took: 155 seconds
  
<img src="https://github.com/AmmarRashed/notMNIST/blob/master/misc/single_layer_lr.png?raw=true">

- Mini batch (ReLU)
  - 95% accuracy
  - took: 188 seconds
  <img src="https://github.com/AmmarRashed/notMNIST/blob/master/misc/tf_relu_l2_reg.png?raw=true">

- ReLU with L2-regularization
  - 95.9% accuracy
  - took: 192 seconds
<img src="https://github.com/AmmarRashed/notMNIST/blob/master/misc/tf_relu_dropout.png?raw=true">


- ReLU with dropout+L2-regularization
  - 95.7% accuracy
  - took: 208 seconds
<img src="https://github.com/AmmarRashed/notMNIST/blob/master/misc/tf_relu_dropout.png?raw=true">


- CNN with dropout+L2-regularization (similar to <a href="http://yann.lecun.com/exdb/lenet/">LeNet</a>)
  - 95.5% accuracy
  - took: 391.5 seconds
<img src="https://github.com/AmmarRashed/notMNIST/blob/master/misc/CNN.png?raw=true">


- CNN inception module (concatenation)
  - 95.1% accuracy
  - took: 554 seconds
<img src="https://github.com/AmmarRashed/notMNIST/blob/master/misc/inception_concat.png?raw=true">

- CNN inception module (reduce mean)
  - 93.6% accuracy
  - took: 528.5 seconds
<img src="https://github.com/AmmarRashed/notMNIST/blob/master/misc/inception_avg.png?raw=true">



## Dependancies

**Tested on Python 3.5**
- <a href="http://scikit-learn.org/"> scikit-learn </a>
- <a href="http://www.numpy.org/"> NumPy </a>
- <a href="https://ipython.org/"> IPython</a>
- <a href="https://matplotlib.org/"> Matplotlib</a>
- <a href="https://pythonhosted.org/joblib/"> Joblib (optional)</a>
