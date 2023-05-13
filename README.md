# Pytorch installation

---

# Resources

Youtube Video:

[How to Install PyTorch on Linux for CPU or GPU - No Driver Install Needed](https://www.youtube.com/watch?v=YTvVxYneu7w)

---

# Required Software versions:

+ **miniconda 3.8**
+ **pytorch 1.12.0**
+ **phyton 3.7.16**
+ **cuDNN	8.3.2**
+ **CUDA 11.3.1**

---

# Installation Steps

1.- Download [Miniconda 3.8](https://docs.conda.io/en/latest/miniconda.html)

2.- Open Terminal and change directory: **cd ./Downloads/**

3.- Install miniconda: **chmod -x ./name-of-file.sh**

4.- Install conda navigator: **conda install anaconda-navigator**
 
 + To open anaconda navigator type: **anaconda-navigator

5.- Install Jupiter Notebook: **conda install -y jupyter**

6.- Create *tensorflow environment* inside conda: **conda create --name pytorch python=3.7**

7.- Enter the created *tensorflow environment*: **conda activate pytorch**

8.- Add Jupyter support to the *tensorflow environment*: **conda install -c conda-forge nb_conda**

9.- Install *pytorch*: **conda install pytorch=1.12 cudatoolkit=11.3 -c pytorch**

+ *tensorflow-gpu* installs *pytorch 1.12.1*, CUDA 11.3.1 and cuDNN 8.3.2

10.- Additional required libraries, Download [toolsPytorch.yml](https://raw.githubusercontent.com/brainnlabs/Pytorch-installation/main/toolsPytorch.yml) and paste it inside *home* folder.

11.- Run the following terminal command: **conda env update --file toolsPytorch.yml** 

12.- Register your environment to show inside jupyter notebook: **python -m ipykernel install --user --name pytorch --display-name "Python 3.7 (pytorch)""**

13.- Testing *tensorflow* environment: **jupyter notebook**

```
# What version of Python do you have?
import sys

import tensorflow.keras
import pandas as pd
import sklearn as sk
import tensorflow as tf

print(f"Tensor Flow Version: {tf.__version__}")
print(f"Keras Version: {tensorflow.keras.__version__}")
print()
print(f"Python {sys.version}")
print(f"Pandas {pd.__version__}")
print(f"Scikit-Learn {sk.__version__}")
gpu = len(tf.config.list_physical_devices('GPU'))>0
print("GPU is", "available" if gpu else "NOT AVAILABLE")
```

*Tensor Flow Version: 2.1.0*  
*Keras Version: 2.2.4-tf*

*Python 3.7.7 (default, May  6 2020, 11:45:54) [MSC v.1916 64 bit (AMD64)]* 
*Pandas 1.0.5*  
*Scikit-Learn 0.23.1*  
