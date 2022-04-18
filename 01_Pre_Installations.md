# Pre Installations

## Install nVIDIA CUDA Toolkit

`sudo apt install nvidia-cuda-toolkit`

Checking

`nvcc --help`

`nvcc --version`

## Selecting CUDA version
`sudo nano ~/.bashrc`
#### At last
`export CUDA_HOME="/usr/local/cuda-11.5"`
`export LD_LIBRARY_PATH="/usr/local/cuda-11.5/lib64:$LD_LIBRARY_PATH"`
`export PATH="/usr/local/cuda-11.5/bin:$PATH"`
`source ~/.bashrc`

## Installing nVIDIA Setings

`sudo apt install nvidia-settings`

Checking available cuda core

`nvidia-settings -q CUDACores -t`

## Install OpenMPI

`sudo apt-get install openmpi-bin`

## Installing gcc and g++ 7

Gromacs create issue with updated gcc and g++ when installing with cuda. So gcc 7 and g++ 7 should be installed first.

`sudo apt-get install -y software-properties-common`

`sudo add-apt-repository ppa:ubuntu-toolchain-r/test`

`sudo apt update`

`sudo apt install g++-7 -y`

`sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-7 60 --slave /usr/bin/g++ g++ /usr/bin/g++-7`

`sudo update-alternatives --config gcc`

`gcc --version`
