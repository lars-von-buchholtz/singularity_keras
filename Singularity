BootStrap: docker
From: tensorflow/tensorflow:1.2.1-gpu

########################################################################
%labels
########################################################################
TENSORFLOW_VERSION 1.2.1
MAINTAINER Wolfgang Resch

########################################################################
%post
########################################################################

# create bind points for NIH HPC environment
mkdir /gpfs /spin1 /gs2 /gs3 /gs4 /gs5 /gs6
mkdir /gs7 /gs8 /data /scratch /fdb /lscratch

########################################################################
%environment
########################################################################
export LC_ALL=C

########################################################################
%runscript
########################################################################
exec ipython "$@"
