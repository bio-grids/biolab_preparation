# Installing Gromacs with GPU

`cd gromacs-2021.4` [or in desired version]

`mkdir build`

`cd build`

`cmake .. -DGMX_BUILD_OWN_FFTW=ON -DREGRESSIONTEST_DOWNLOAD=ON -DGMX_GPU=CUDA -DGMX_MPI=ON`

`make`

`make check`

`sudo make install`

`source /usr/local/gromacs/bin/GMXRC`
