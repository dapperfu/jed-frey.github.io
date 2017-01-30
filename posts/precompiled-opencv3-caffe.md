<!-- 
.. title: Precompiled OpenCV3 & Caffe for Python3
.. slug: precompiled-opencv3-caffe
.. date: 2017-01-29 11:35:57 UTC-05:00
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text
-->


Binaries:

- [opencv3_3.2.0-1_amd64.deb](/files/opencv3_3.2.0-1_amd64.deb)
- [caffe-distribute.tar.bz2](/files/caffe-distribute.tar.bz2)

Install opencv3 with:

    dpkg -i opencv3_3.2.0-1_amd64.deb
    apt-get install --fix-broken --no-install-recommends --yes
    
Extract caffe:

    tar -xzjf caffe-distribute.tar.bz2
    
Add caffe-distribute/bin to $PATH
Add caffe-distribute/lib to $LD_LIBRARY_PATH
Add caffe-distribute/python to $PYTHONPATH

To make the changes persist across sessions you can add them to ~/.bashrc (if using bash)

Example, assuming the archive was extracted to your home directory:

    export PATH="$HOME/caffe-distribute/bin:$PATH"
    export PYTHONPATH="$HOME/caffe-distribute/python:$PYTHONPATH"
    export LD_LIBRARY_PATH="$HOME/caffe-distribute/lib:$LD_LIBRARY_PATH"


Install required libraries for caffe:

    apt-get install --no-install-recommends --yes libgoogle-glog0v5 libboost-python1.58.0 libleveldb1v5 liblmdb0
     
There are multiple instructions online 


- [opencv3 for python3](https://www.google.com/search?q=compile+opencv3+ubuntu+16.04+python3)
- [caffe for python3 & opencv3](https://www.google.com/search?q=caffe+python3+opencv)

Build:



- Ubuntu 16.04
- x86_64
- CUDA 8.0
- cudnn 5.1 for CUDA 8.0
- Python 3.5.1
- Numpy 1.11.0

Build Scripts:


- [opencv3 w/python3](https://gist.github.com/jed-frey/d01e2d5b39ef33207efda6e170b8788c)
- [opencv3 w/python3](https://gist.github.com/jed-frey/f14399fc7500f03d4c43448c318b3245)


- [opencv3_3.2.0-1_amd64.deb](/files/opencv3_3.2.0-1_amd64.deb)


# Build Scripts

GithubGists of the build scripts for OpenCV3 and Caffe. Both of these should work in a new [Ubuntu 16.04 debootstrap](https://wiki.ubuntu.com/DebootstrapChroot) environment.

## OpenCV3 Build Script

<script src="https://gist.github.com/jed-frey/d01e2d5b39ef33207efda6e170b8788c.js"></script>

## Caffe Build Script

<script src="https://gist.github.com/jed-frey/f14399fc7500f03d4c43448c318b3245.js"></script>
