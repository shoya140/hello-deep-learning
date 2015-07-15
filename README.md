hello-deep-learning
======================

ILSVRC2012 classification with Caffe reference model and Chainer

[playground.ipynb](http://nbviewer.ipython.org/github/shoya140/hello-deep-learning/blob/master/playground.ipynb)

### Set up

Install requirements.

```
$ brew install gcc python
$ easy_install pip
$ pip install numpy scipy scikit-learn chainer
$ brew install opencv
```

Install options (for iPythonNotebook).

```
$ pip install ipython matplotlib pandas jinja2 tornado pyzmq
```

Download "bvlc_googlenet.caffemodel".

```
$ git clone  https://github.com/pfnet/chainer.git
$ python chainer/examples/modelzoo/download_model.py googlenet
```

Download "synset_words.txt".

```
$ git clone https://github.com/BVLC/caffe.git
$ ./data/ilsvrc12/get_ilsvrc_aux.sh
```

Clone this repository and put resources into ./model directory. 

```
$ git clone https://github.com/shoya140/hello-deep-learning.git
$ mkdir hello-deep-learning/model
$ cp bvlc_googlenet.caffemodel ./hello-deep-learning/model/
$ cp synset_words.txt ./hello-deep-learning/model/
$ cd hello-deep-learning && ipython notebook
```