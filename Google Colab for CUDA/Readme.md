# How to Use Google Colab to Run CUDA Codes
In this tutorial, I'm going to provide some tips to run CUDA (C or C++) codes on Google Colab.

For running CUDA codes we need a NVIDIA GPU, but some people don't have access to these GPUs. Fortunately, Google has provided this capability in its Colab, andit is possible to run our CUDA codes on it for free! Follow this tutorial to do so:

## Step1
1. Open your browser and go to https://colab.research.google.com

2. Go to ```File->New Notebook``` (it may ask for type of Notebook, then choose "Python 3 Notebook")

3. Go to ```Runtime->Change runtime type``` and change the Harware accelerator to GPU. Then click on ```Save``` button

![Accelerator](https://github.com/MajidSalimi/Manuals-and-Documents/blob/master/Google%20Colab%20for%20CUDA/Capture.JPG)

## Step2
Write the following code on a seperate block
```
!apt-get --purge remove cuda nvidia* libnvidia-*
!dpkg -l | grep cuda- | awk '{print $2}' | xargs -n1 dpkg --purge
!apt-get remove cuda-*
!apt autoremove
!apt-get update
```

## Step3
Now, it's time to install CUDA 9. For this purpose, open a new block and copy the code below in it:
```
!wget https://developer.nvidia.com/compute/cuda/9.2/Prod/local_installers/cuda-repo-ubuntu1604-9-2-local_9.2.88-1_amd64 -O cuda-repo-ubuntu1604-9-2-local_9.2.88-1_amd64.deb
!dpkg -i cuda-repo-ubuntu1604-9-2-local_9.2.88-1_amd64.deb
!apt-key add /var/cuda-repo-9-2-local/7fa2af80.pub
!apt-get update
!apt-get install cuda-9.2
```

## Step4
After the installation process is finished, you can check your CUDA version by the following command:
```
!nvcc --version
```

If it is correctly installed, you will get its version like the following:
```
nvcc: NVIDIA (R) Cuda compiler driver
Copyright (c) 2005-2018 NVIDIA Corporation
Built on Wed_Apr_11_23:16:29_CDT_2018
Cuda compilation tools, release 9.2, V9.2.88
```

## Step5
Now, you should install a plugin to run your CUDA codes using NVCC. Open a new code block and write:
```
!pip install git+git://github.com/andreinechaev/nvcc4jupyter.git
```
Then, you have to load the plugin. For this purpose, open another new code block and write:
```
%load_ext nvcc_plugin
```

## Step6
It's time to run your CUDA codes on Google Colab
