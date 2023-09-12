---
layout: page
title: Getting Started
weight: 3
---


## Introduction 

The Gaussian Process Summer School will include some hands-on tutorials in which we will build some simple Gaussian process models. The tutorials will be in Python, featuring the open source GPy package that has been developed by the Machine Learning group at the University of Sheffield.

We'll hold the labs in the same room as the talks and lunch.

Prior Python programming skills are not required, however you should ensure that you have followed the appropriate intrustrctions for running the labs in Google Colab or Locally below.

## Running Labs in Google Colab

This year, we are hosting the labs on Google Colab, a cloud-based environment that you can use to run labs in. You can run the labs in Colab from your browser, without the need to setup a python environment locally on your machine.

To access the labs on Google Colab, follow the appropriate links on the [Labs](./labs) page. To save any progress you make within a notebook you will need to click on the "Copy to Drive" button.

## Running Labs on your Local Machine

You may wish to run the labs on your local machine. You can do this by setting up a Python environment using the following instructions. We highly recommend that you install via [Anaconda](https://www.anaconda.com/download), an integrated Python environment.

The following instructions will tell you how to install and setup the Python library for the tutorials, and some information on installing and running Jupyter. All labs are in a format called "_notebooks_", which can be run using [Jupyter](https://jupyter.org). These are worksheets that can execute Python code in blocks in your web browser.

To download a notebook, click on the _Download_ link listed on [Labs](./labs). This will display the raw code for the notebook, copy and paste all of this code into a new file with the extension `.ipynb` on your computer, e.g. `lab1.ipynb`.

In a terminal window, navigate to the file's path (using the `cd` command) and run the command `jupyter notebook`. This will open a browser window connecting to the (locally hosted) notebook server. The notebook should be visible in the file list.

Typically, Jupyter will launch the server at [http://localhost:8888/tree](http://localhost:8888/tree), and you can navigate to it this way, should you accidentally close the window.

### Installing Python with Anaconda

Anaconda is a distribution of the Python prorgamming language that comes integrated with a number of precompiled libraries, and its own package and environment manager, called `conda`. It freely allows use of installation of packages and libraries via `conda` or `pip`. We recommend using Anaconda to manage your Python language environment, _particularly if you are new to Python_, and the following instructions will assume you are using Anaconda. If you are using a different Python distribution, you may have to tailor to following instructions, but you should ensure that you are using Python 3.6+.

### Installing Packages

The easiest way to get a working Python environment is to install Anaconda. It is straightforward to install, but can take some time so you must make sure this is done before the lab.

1. Download and install the free version of Anaconda from its webpage: [https://www.anaconda.com/download](https://www.anaconda.com/download)
2. Update Anaconda: open a command prompt or terminal and execute the following command: `conda update --name base conda`
3. Create an environment for this workshop: `conda create -n gpss python=3.10`, and activate it `conda activate gpss`
4. Install common python packages: `pip install "numpy>=1.20,<1.25" scipy matplotlib jupyter requests`
5. Install GP specific python packages used for this workshop: `pip install git+https://github.com/connorfuhrman/paramz@connorfuhrman/np_type_alias_dep git+https://github.com/m-lyon/GPy git+https://github.com/SheffieldML/pyDeepGP git+https://github.com/m-lyon/climin emukit`
  - **N.B.** It is crucial to install the versions listed here to ensure dependency compatibility.
  - See below for a description of these packages.


#### GPy

GPy is a Gaussian Process (GP) framework written in python, from the Sheffield machine learning group.

You can test that the installation of `GPy` is working by running the following in a Python shell:
```
>>> import GPy
```
If you want to check your installation, you need to `$ pip install nose` and run `>>> GPy.tests()` in the Python shell. This will run through the testing sequence.

#### paramz

paramz is a parameterization framework for parameterized model creation and handling. It is a lightweight framework for using parameterized models, and is a dependency of GPy.

#### pyDeepGP

This is the library used for creating deep Gaussian Processes with GPy.

#### climin

This is the library used for stochastic optimisation, and is required for the final section of Lab 2.

#### Emukit

This library is useful for solving, among other things, global optimization problems. It is used in Lab 3.
