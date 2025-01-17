GAN models in the browser with tensorflow.js

* Demo: https://josephrocca.github.io/tfjs-gans/index.html
* See also: https://github.com/josephrocca/tfjs-acgan-browser-training

## Setup

Download this repo and serve the contents of the folder with a static webserver of your choice. For example:

```sh
git clone https://github.com/josephrocca/tfjs-gans
cd tfjs-gans
# install deno if you don't have it: https://deno.land/
deno run --allow-net --allow-read=. https://raw.githubusercontent.com/josephrocca/denoSimpleStatic/master/main.ts
```

The server will say something like "Start listening on 127.0.0.1:8000", and so you'd open up `127.0.0.1:8000` in your browser.

## Training a model

You can use [this colab notebook](https://colab.research.google.com/drive/1WmZRWG1L1_SuBwDVyiexcLkGSn8gqYap) to train your own DCGAN, or you can convert a ProGAN/PGGAN, or BigGAN model (among others) from [tfhub.dev](https://tfhub.dev/) to tfjs format by opening a new Google Colab notebook and running the following code:
```
!pip install tensorflowjs[wizard].
!tensorflowjs_wizard
```
Enter a tfhub URL like `https://tfhub.dev/google/progan-128/1` when prompted, and use all the default options. Then download the model files. More detailed instructions are in the [tfjs-converter repo](https://github.com/tensorflow/tfjs/tree/master/tfjs-converter).
