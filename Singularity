BootStrap: docker
From: nvidia/cuda:8.0-cudnn5-devel

################################################################################
%labels
################################################################################
MAINTAINER Wolfgang Resch
VERSION v2

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
apt-get update
apt-get install -y libhdf5-dev graphviz locales python3-dev python3-pip
locale-gen en_US.UTF-8
apt-get clean

pip install --upgrade pip

pip install tensorflow-gpu
pip install keras
pip install Pillow scikit-learn pandas matplotlib notebook ipython jupyter numpy scipy

pip3 install tensorflow-gpu
pip3 install keras
pip3 install Pillow scikit-learn pandas matplotlib notebook ipython

###
### destination for NIH HPC bind mounts
###

mkdir /gpfs /spin1 /gs2 /gs3 /gs4 /gs5 /gs6 /gs7 /gs8 /data /scratch /fdb /lscratch
