# Mini Course in Deep Learning with PyTorch for AIMS
[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/Atcold/PyTorch-Deep-Learning-Minicourse/master)

The African Masters of Machine Intelligence (AMMI) is Africa's flagship program in machine intelligence led by The African Institute for Mathematical Sciences (AIMS).

These lessons, developed during the course of several years while I've been teaching at Purdue and NYU, are here proposed for the AMMI (AIMS).

Prior to this course delivered for AMMI (AIMS), an earlier version of this was delivered for the Computational and Data Science for High Energy Physics ([CoDaS-HEP](http://codas-hep.org/)) summer school at Princeton University. Please refer to this version release [here](https://github.com/Atcold/pytorch-Deep-Learning-Minicourse/releases/tag/v1.0.0). 

## Table of contents
`T`: theory (slides and animations)  
`P`: practice (*Jupyter Notebooks*)

 1. `T` Learning paradigms: supervised-, unsupervised-, and reinforcement-learning
 2. `P` Getting started with the tools: Jupyter notebook, PyTorch tensors and autodifferentiation
 3. `T+P` Neural net's forward and backward propagation for classification and regression
 4. `T+P` Convolutional neural nets improve performance by exploiting data nature
 5. `T+P` Foundations of Salsa
 6. `T+P` Recurrent nets natively support sequential data
 7. `T+P` Unsupervised learning: vanilla and variational autoencoders, generative adversarial nets
 
## Sessions and relative material
 1. Time slot 1 (4h + 4h)
    <br />Topics: 1, 2, 3.
    <br />Slides: [01 - ML and spiral classification](slides/01%20-%20ML%20and%20spiral%20classification.pdf).
    <br />Notebooks: [01](01-tensor_tutorial.ipynb), [02](02-space_stretching.ipynb), [03](03-autograd_tutorial.ipynb), [04](04-spiral_classification.ipynb), [05](05-regression.ipynb).  
 2. Time slot 2 (4h + 2h) 
    <br />Topic: 4.
    <br />Slides: [02 - CNN](slides/02%20-%20CNN.pdf).
    <br />Notebooks: [06](06-convnet.ipynb), [07](07-listening_to_kernels.ipynb).
 3. Time slot 3 (2h)
    <br />Slides: [03 - Salsa](slides/03%20-%20Salsa.pdf).
    <br />Topic: 5.
 4. Time slot 4 (4h + 4h)
    <br />Topic: 6.
    <br />Code Readings: [Word Language Model](https://github.com/pytorch/examples/blob/master/word_language_model/model.py)
    <br />Assignment: [HW1](assignments/hw1.pdf)
    <br />Notebooks: [08](08-seq_classification.ipynb), [09](09-echo_data.ipynb)
 5. Time slot 4 (4h)
    <br />Topic: 7.
    <br />Guides: [TikZ Quick Guide](assignments/tikz_guide.pdf)
    <br />Notebooks: [10](10-autoencoder.ipynb), [11](11-VAE.ipynb)

## Notebooks visualisation
*Jupyter Notebooks* are used throughout these lectures for interactive data exploration and visualisation.

We use dark styles for both *GitHub* and *Jupyter Notebook*.
You should try to do the same, or they will look ugly.
To see the content appropriately install the following:

 - [*Jupyter Notebook* dark theme](https://userstyles.org/styles/153443/jupyter-notebook-dark);
 - [*GitHub* dark theme](https://userstyles.org/styles/37035/github-dark) and comment out the `invert #fff to #181818` code block.

## Keeping in touch
Feel free to follow Afredo at [Twitter](https://twitter.com/alfcnz) and subscribe to his [YouTube channel](https://www.youtube.com/user/Atcold/) to have the latest free educational material.

For more educational materials you also can head to Ritchie's [website](https://www.ritchieng.com/).

# Getting started
To be able to follow the workshop exercises, you are going to need a laptop with Miniconda (a minimal version of Anaconda) and several Python packages installed.
Following instruction would work as is for Mac or Ubuntu linux users, Windows users would need to install and work in the Gitbash terminal.

## Download and install Miniconda
Please go to the [Anaconda website](https://conda.io/miniconda.html).
Download and install *the latest* Miniconda version for *Python* 3.6 for your operating system.

```bash
wget <http:// link to miniconda>
sh <miniconda .sh>
```

After that, type:

```bash
conda --help
```

and read the manual.

## Check-out the git repository with the exercise
Once Miniconda is ready, checkout the course repository and and proceed with setting up the environment:

```bash
git clone https://github.com/Atcold/PyTorch-Deep-Learning-Minicourse
```

If you do not have git and do not wish to install it, just download the repository as zip, and unpack it:

```bash
wget https://github.com/Atcold/PyTorch-Deep-Learning-Minicourse/archive/master.zip
#For Mac users:
#curl -O https://github.com/Atcold/PyTorch-Deep-Learning-Minicourse/archive/master.zip
unzip master.zip
```

## Create isolated Miniconda environment
Change into the course folder, then type:

```bash
#cd PyTorch-Deep-Learning-Minicourse
conda env create -f environment.yml
source activate aims-ml
```

## Enable anaconda kernel in Jupyter
To make newly created miniconda environment visible in the Jupyter, install `ipykernel`:

```bash
python -m ipykernel install --user --name aims-ml --display-name "AIMS DL"
```

## Install Autocomplete by hinterland
You have to run the following commands if you want auto-complete.
```
pip install jupyter_contrib_nbextensions
pip install jupyter_nbextensions_configurator
jupyter contrib nbextension install --user

cd /usr/local/miniconda3/envs/aims-ml/lib/python3.6/site-packages/jupyter_contrib_nbextensions/nbextensions
jupyter nbextension install hinterland
jupyter nbextension enable hinterland/hinterland
```
## Start jupyter notebook
If you are working in a JupyterLab container double click on "Files" tab in the upper right corner.
Locate first notebook, double click to open.
Do not attempt to start `jupyter` from the terminal window.

If working on a laptop, start from terminal as usual:

```bash
jupyter notebook
```
