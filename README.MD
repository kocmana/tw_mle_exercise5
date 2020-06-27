# Exercise 5 - Deep Learning

## Description
The main goal of this exercise is to work with Deep Learning approaches, either for image or for sequential data, depending on your preference / experience / interest to learn.
Thus. you shall use approaches such as convolutional neural networks (for images) or recurrent neural networks (for text)
For images, you can base your DL implementation on the tutorial provided by colleagues at TU Wien, available at https://github.com/tuwien-musicir/DL_Tutorial/blob/master/Car_recognition.ipynb (you can also check the rest of the repository for interesting code; credit to Thomas Lidy (http://www.ifs.tuwien.ac.at/~lidy/)).
For the dataset you shall work with, pick one of the text/image datasets from the list of suggestions below. If you have proposals for other datasets, please inform me (rmayer@technikum-wien.at), and we can see if the dataset is fit.

### For Images:
* The German Traffic Sign Recognition Benchmark (GTSRB), http://benchmark.ini.rub.de/
* AT&T (Olivetti) Faces: https://www.cl.cam.ac.uk/research/dtg/attarchive/facedatabase.html, https://scikit-learn.org/0.19/datasets/olivetti_faces.html
* Yale Face Database: http://vision.ucsd.edu/content/yale-face-database
* CIFAR-10: https://www.cs.toronto.edu/~kriz/cifar.html
* Tiny ImageNet: https://tiny-imagenet.herokuapp.com/
* Labeled Faces in the Wild, http://vis-www.cs.umass.edu/lfw/, using the task for face recognition. See also https://scikit-learn.org/0.19/datasets/#the-labeled-faces-in-the-wild-face-recognition-dataset

### For Text Data:
* 20 newsgroups: http://qwone.com/~jason/20Newsgroups/
* Reuters: http://www.daviddlewis.com/resources/testcollections/reuters21578/

### Recommendations for CNNs specifically:
* Use architectures of your choice – you can work with something simple like a LeNet, or a bit more advanced architectures (where maybe transfer learning is required for efficiency reasons, see below).
* Use as well data augmentation (you can reuse the code from the tutorial), and compare it to the non-augmented results
* Also consider using transfer learning of pre-trained models


If you do want to work in a group of up to three students, this is also possible, then the task would be slightly extended, to either
* Choosing three datasets (you shall chose only one of the AT&T and Yale Face datasets, but not both of them, as they are both relatively small)
* Or a comparison to non-DL based approaches for image / text classification (for image, some of you already did this in exercise 4). Specifically, in this case, follow the instructions below.

### Comparison to feature-extraction based approaches (group work, 3 students):
The main goal of this exercise is to get a feeling and understanding on the importance of representation of complex media content, in this case images or text. You will thus get some datasets that have an image classification target.
(1) In the first step, you shall try to find a good classifier with „traditional“ feature extraction methods. Thus, pick
* For Images
  * One simple feature representation (such as a colour histogram, see also the example provided in Moodle for the previous exercise) and
  * A feature extractor based on SIFT (https://en.wikipedia.org/wiki/Scale-invariant_feature_transform) and subsequent visual bag of words (e.g. https://kushalvyas.github.io/BOV.html for python), or a similar powerful approach (such as SURF, HOG, ..).

* For Text
  * One feature extractor based on e.g. Bag Of Words, or n-grams, or similar
You shall evaluate these features on a couple of non-DL algorithms (for image, also specifically including a simple MLP), and parameter settings to see what performance you can achieve, to have a baseline for the subsequent steps.

Compare not just the overall measures, but perform a detailed comparison and analysis per class (confusion matrix), to identify if the two approaches lead to different types of errors in the different classes, and also try to identify other patterns. Also perform a detailed comparison of runtime, considering both time for training and testing, including also the feature extraction components.