TensorFlow is an open source software library for machine intelliegence.

Per Google: TensorFlow is an open source software library for numerical computation using data flow graphs. Nodes in the graph represent mathematical operations, while the graph edges represent the multidimensional data arrays (tensors) communicated between them.

This article assumes that you have a basic knowledge of the terminal, node, homebrew, and the command line -- and that you are working on a Mac (directions could be adjusted for a PC, but that's not what they're written for).
This article also assumes that you do not have a working knowledge of python or anaconda.

***Check your version of python:***

`$ python --version`

If it is not 3.5, download and install it from [here](https://www.python.org/downloads/)

***Install Dependencies:***

`$ brew install bazel swig`

`$ sudo easy_install -U six`

`$ sudo easy_install -U numpy`

`$ sudo easy_install wheel`

`$ sudo easy_install ipython`

***Installing Anaconda***
* Go to [continuum](https://www.continuum.io/) to download the Anaconda CLI installer
Download Command-Line Installer for Python 3.5

`$ cd [downloaded file location -- most likely Downloads]`

`$ bash FILENAME`

`$ cd`

`$ vim .zshrc (or .bash_profile)`

From vim add `export PATH="$HOME/anaconda3/bin:$PATH"` to your .zshrc or .bash_profile file, then exit vim.

`$ conda install -c conda-forge tensorflow`

(where NAME = the name you give your environment)

`$ conda create —n NAME python=3.5`

`$ source activate NAME` (at the end `$ source deactivate` to exit)

Other helpful Anaconda Commands:
* List your environments: `$ conda info —-envs`
* What Anaconda Version? `$ conda info —-version`
* Help: `$ conda info —h`
* Remove an environment: `conda-env remove -n NAME`

Then to test it…

`$ source activate NAME`

`$ ipython`

`[1]: import tensorflow as tf`

`[2]: <blank> the fact that nothing shows up here is good`

then...

`[2]: exit`

After exiting OR instead of using ipython:

`$ jupyter notebook`

(pick a folder or create one then create a notebook)

In the first text line of the notebook:
import tensorflow as tf

In the top menu bar go to cell > run all. You should see no errors -- that's good!

Next you can test whatever you want, for example — the [small python code segment from the tensorflow site](https://www.tensorflow.org/versions/r0.11/get_started/index.html):

***Copy and Paste this entire script into your jupyter notebook file***

```sh

import tensorflow as tf
import numpy as np

# Create 100 phony x, y data points in NumPy, y = x * 0.1 + 0.3
x_data = np.random.rand(100).astype(np.float32)
y_data = x_data * 0.1 + 0.3

# Try to find values for W and b that compute y_data = W * x_data + b
# (We know that W should be 0.1 and b 0.3, but TensorFlow will
# figure that out for us.)
W = tf.Variable(tf.random_uniform([1], -1.0, 1.0))
b = tf.Variable(tf.zeros([1]))
y = W * x_data + b

# Minimize the mean squared errors.
loss = tf.reduce_mean(tf.square(y - y_data))
optimizer = tf.train.GradientDescentOptimizer(0.5)
train = optimizer.minimize(loss)

# Before starting, initialize the variables.  We will 'run' this first.
init = tf.initialize_all_variables()

# Launch the graph.
sess = tf.Session()
sess.run(init)

# Fit the line.
for step in range(201):
    sess.run(train)
    if step % 20 == 0:
        print(step, sess.run(W), sess.run(b))

# Learns best fit is W: [0.1], b: [0.3]

```

In the top menu bar go to cell > run all — and your result will be calculated in the bottom of the notebook.

Special thanks to a data scientist friend and some willing test subjects to work out the kinks in this process.
