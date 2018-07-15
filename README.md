# notMNIST
Letter recognition Logistic Regression classifier trained on notMNIST (alphabet A-J)

- <a href="https://www.udacity.com/">Udacity</a>
  - <a href="https://classroom.udacity.com/courses/ud730"> Intro to Deep Learning</a>
    - <a href="https://github.com/tensorflow/tensorflow/blob/master/tensorflow/examples/udacity/1_notmnist.ipynb">Assignment 1</a>

## Data
- <a href="http://yaroslavvb.com/upload/notMNIST/"> notMNIST </a>
<img src="https://lh4.googleusercontent.com/proxy/b94FV3AHSfDPdqNvd0PXCXnQLzSZquHEoQqziiMTHOvbuVP3xIjVH92yYzpOCCqqnUOS0PjjFDjMawC905m19Rs=w1200-h630-p-k-no-nu">
529119 28 x 28 grayscale images of letters A - J, sorted into directories by letter. There are 52920 images for letters A - I, and 52919 images for letter J. This dataset is more challenging version of the image classification problem than <a href="http://yann.lecun.com/exdb/mnist/">MNIST</a>: classifying letters from images. It is a multiclass classification dataset of glyphs of English letters A - J.

## Performance
- <a href="http://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html"> Sklearn Logistic Regression </a>
<img src="https://github.com/AmmarRashed/notMNIST/blob/master/misc/sklearn_perf.png?raw=true">
- Full batch: Single Layer Logistic Regression with TensorFlow
<img src="https://github.com/AmmarRashed/notMNIST/blob/master/misc/tf_perf_fullbatch.png?raw=true">
- Mini batch (`batch_size=1000`)
<img src="https://github.com/AmmarRashed/notMNIST/blob/master/misc/single_layer_lr.png?raw=true">

## Dependancies
**Tested on Python 3.5**
- <a href="http://scikit-learn.org/"> scikit-learn </a>
- <a href="http://www.numpy.org/"> NumPy </a>
- <a href="https://ipython.org/"> IPython</a>
- <a href="https://matplotlib.org/"> Matplotlib</a>
- <a href="https://pythonhosted.org/joblib/"> Joblib (optional)</a>
