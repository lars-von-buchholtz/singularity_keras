BootStrap: docker
From: nvidia/cuda:8.0-cudnn6-runtime-ubuntu16.04

################################################################################
%labels
################################################################################
MAINTAINER Wolfgang Resch/Lars von Buchholtz
VERSION v3

################################################################################
%environment
################################################################################
export PATH=/bin:/usr/bin:/usr/local/bin:/usr/local/cuda/bin:

################################################################################
%post
################################################################################

###
### install keras + tensorflow + other useful packages
###

echo "en_US.UTF-8 UTF-8" > /etc/locale.gen
apt-get update 
apt-get install -y software-properties-common python-software-properties
add-apt-repository main
add-apt-repository universe
add-apt-repository multiverse
apt-get install -y --no-install-recommends \
        autoconf \
        automake \
        ca-certificates \
        curl \
        g++ \
        git \
        libtool \
        make \
        python-dev \
        python-setuptools \
        unzip doxygen

apt-get install -y --no-install-recommends \
        ca-certificates \
        cmake \
        curl \
        g++ \
        git \
        libatlas-base-dev \
        libboost-filesystem-dev \
        libboost-python-dev \
        libboost-system-dev \
        libboost-thread-dev \
        libgflags-dev \
        libgoogle-glog-dev \
        libhdf5-serial-dev \
        libleveldb-dev \
        liblmdb-dev \
        libnccl-dev=1.2.3-1+cuda8.0 \
        libopencv-dev \
        libsnappy-dev \
        python-all-dev \
        python-h5py \
        python-matplotlib \
        python-opencv \
        python-pil \
        python-pydot \
        python-scipy \
        python-skimage \
        python-sklearn libhdf5-dev graphviz locales python3-dev python3-pip

locale-gen en_US.UTF-8
apt-get clean

pip3 install --upgrade setuptools
pip3 install tensorflow-gpu==1.3.0
pip3 install keras==2.0.8
pip3 install -U Pillow scikit-learn pandas matplotlib notebook ipython numpy nibabel scipy Cython six
pip3 install git+https://github.com/aleju/imgaug

###
### destination for NIH HPC bind mounts
###

mkdir /gpfs /spin1 /gs2 /gs3 /gs4 /gs5 /gs6 /gs7 /gs8 /data /scratch /fdb /lscratch




