Directions for using TensorFlow with the Fast-Style-Transfer repo.

This aritcle assumes that you followed the setup directions found [here](https://gist.github.com/thacherT1D/0103f69cb409385b80fb717419eb2ffc) OR that you have python correctly setup on your machine with an anaconda environment that has TensorFlow installed.

Clone the Fast-Style-Transfer repo: `$ git clone https://github.com/lengstrom/fast-style-transfer.git`

`$ cd fast-style-transfer`

Download this [Fast Styles Transfer Models](https://drive.google.com/drive/folders/0B9jhaT37ydSyRk9UX0wwX3BpMzQ) from google drive.

Add the downloaded folder to your `fast-style-transfer` directory.

Add the image that you want to style to your `fast-style-transfer` directory. Your image should be smaller than 200 KB to finish in a decent amount of time.

Stil from the fast-style-transfer directory, activate your anaconda environment with TensorFlow, for this example it is called `tensorflow`.

`$ source activate tensorflow`

In the following code my image file is `casey.jpg` and I chose to use the `la_muse.ckpt` transfer model.

`$ python evaluate.py --checkpoint Fast\ Style\ Transfer\ Models/la_muse.ckpt \
--in-path casey.JPG \
--out-path ./examples/results`

Your finished file will be found in fast-style-transfer/examples/results

If you want to try different effects on the same input image, you will need to change the names of the competed files, such as: `./examples/results/casey.jpg` to `./examples/results/casey_la_muse.jpg`
