# Pre Installations

## Install nVIDIA CUDA Toolkit

`sudo apt install nvidia-cuda-toolkit`

Checking

```shell
nvcc --help
nvcc --version
```

## Selecting CUDA version

`sudo nano ~/.bashrc`

#### At last

```shell
export CUDA_HOME="/usr/local/cuda-xx.x"
export LD_LIBRARY_PATH="/usr/local/cuda-xx.x/lib64:$LD_LIBRARY_PATH"
export PATH="/usr/local/cuda-xx.x/bin:$PATH"
source ~/.bashrc
```

## Installing nVIDIA Setings

`sudo apt install nvidia-settings`

Checking available cuda core

`nvidia-settings -q CUDACores -t`

## Install OpenMPI

### Install

`sudo apt-get install openmpi-bin`

### Build

1. Install latest gcc, g++, gfortran
```shell
sudo apt install gcc g++ gfortran -y
```
2. Download current version from http://www.open-mpi.org
3. Extract it
```shell
tar -jxf openmpi-x.x.x.tar.bz2
cd openmpi-x.x.x
```
4. Configure and install
```shell
./configure --prefix=$HOME/opt/openmpi CC=gcc-11 CXX=g++-11 FC=gfortran-11
make -j8 all
make -j8 install
```
5. Adapt PATH and LD_LIBRARY_PATH environment variable:
```shell
echo "export PATH=\$PATH:\$HOME/opt/openmpi/bin" >> $HOME/.bashrc
echo "export LD_LIBRARY_PATH=\$LD_LIBRARY_PATH:\$HOME/opt/openmpi/lib" >> $HOME/.bashrc
source $HOME/.bashrc
```
6. Test installation:
```shell
mpirun -h
```
7. Clean folder and files:
```shell
cd
rm $HOME/local/src/openmpi-x.x.x.tar.bz2
rm -rf $HOME/local/src/openmpi-x.x.x
```

## Installing gcc and g++ 7

Gromacs create issue with updated gcc and g++ when installing with cuda. So gcc 7 and g++ 7 should be installed first.

```shell
sudo apt-get install -y software-properties-common

sudo add-apt-repository ppa:ubuntu-toolchain-r/test

sudo apt update

sudo apt install g++-7 -y

sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-7 60 --slave /usr/bin/g++ g++ /usr/bin/g++-7

sudo update-alternatives --config gcc

gcc --version
```
