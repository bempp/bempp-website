---
title: Installing Bempp
---

The page contains information about how to install the latest version of Bempp ({{ site.bemppversion }}).
You can find information about installing the previous version (Bempp 3.3.4) [here](bempp334/installation.md).

## Running Bempp with Docker
If you want to use Bempp without installing it directly on your computer, you can run a
Jupyter notebook lab containing Bempp using Docker. To do this, run the following commands:

```bash
docker pull bempp/cl-notebook:latest
docker run -p 8888:8888 bempp/cl-notebook
```

Instructions for opening your Jupyter lab in a web browser will then be output to your terminal.

In order to share a directory with the docker image, replace the second command with:
```bash
docker run -v /path/to/folder:/root/shared -p 8888:8888 bempp/cl-notebook
```
The folder `/path/to/folder` on your computer will then be visible as `shared` in the
root directory of the Jupyter lab.

### Running Numba-only Docker image
On some systems, running OpenCL inside a Docker image can cause issues with drivers. Typically,
this will cause errors to be thrown when trying to import Bempp. If you experience this, you can
run the Numba-only Bempp Docker image using the following commands:

```bash
docker pull bempp/cl-notebook-numba:latest
docker run -p 8888:8888 bempp/cl-notebook-numba
```

A folder can be shared with the image in the same way as above.

## Quick install
The latest release of Bempp can be installed using `pip`:

```bash
pip install bempp-cl
```

Alternatively, the latest development version of Bempp can be installed using `pip`:

```bash
pip install numpy scipy numba meshio>=4.0.16 gmsh==4.6.0
pip install git+https://github.com/bempp/bempp-cl.git
```

Alternatively, you can install Bempp using `conda`.
First, if not already done, enable the conda-forge channel:

```bash
conda config --add channels conda-forge
conda config --set channel_priority strict
```

You can then install Bempp with:

```bash
conda install bempp-cl
```

## Installing from Source
You can find the source code of bempp-cl on [GitHub](https://github.com/bempp/bempp-cl).

### Requirements
Bempp can be installed on any Windows, Mac or Linux system with Python 3.7+.
The following dependencies are required:

+ NumPy
+ SciPy
+ Numba
+ meshio

These can be installed with:

```bash
pip install numpy scipy numba meshio>=4.0.16
```

Some features will not work without the following dependencies:

+ plotly
+ pyopencl
+ [gmsh](https://gmsh.info) (tested with version 4.6.0)
+ [exafmm](https://github.com/exafmm/exafmm-t)

These can be installed with:

```bash
pip install plotly pyopencl gmsh==4.6.0

git clone https://github.com/exafmm/exafmm-t.git
cd exafmm-t
./configure 
make
make install
python setup.py install
```

### Installing Bempp
Once you have installed all the requirements, you can install Bempp with the following commands:

```bash
git clone https://github.com/bempp/bempp-cl
cd bempp-cl
python setup.py install
```

### OpenCL
Bempp-cl uses OpenCL kernels to launch computations.
[OpenCL](https://www.khronos.org/opencl/) is a standard for accessing
various types of compute devices, including CPUs and GPUs. Bempp-cl uses
OpenCL to compile C99 kernels during runtime for the underlying compute device.
This requires a runtime environment to be installed. Runtime environments are
available from Apple (CPU, GPU), Nvidia (GPU),
[AMD (GPU)](https://rocm.github.io/install.html),
[Intel (CPU/GPU)](https://software.intel.com/en-us/articles/opencl-drivers) and
through the open-source [Pocl Project (CPU)](http://portablecl.org/). In the
following a few important remarks about OpenCL runtime environments.

+ Most GPU devices are much faster in single precision and we do not
  advise using Bempp in double precision on such devices.
+ If Pocl is used we require at least version 1.3. The package in the
  current Ubuntu 18.04 LTS release is older and does not yet support Bempp-cl.
+ The Apple CPU runtime environment is not compatible with Bempp-cl.

We provide quick installation instructions with Pocl, but also test regularly
with AMD and Nvidia runtime environments. This quick installation creates a
working installation based on the Pocl ICD (Installable Client Driver). For the
activation of other ICDs (e.g. from AMD or Nvidia) see further below.

#### Using other compute devices
Any compute device that provides a valid ICD can
in principle be used with Bempp. However, if Bempp is installed within a conda
environment these may not be seen by the installation. The reason is that conda
expects files in different locations than may be provided by the system. The
following two solutions have been tested on Linux based systems.

##### Set the ICD location via environment variable

Typically, GPU vendors install ICDs in `/etc/OpenCL/vendors`. You can
set this as default search path for ICD files with the command
::

    export OPENCL_VENDOR_PATH=/etc/OpenCL/vendors

The drawback is that as long as this variable is set the Pocl driver
provided through conda is not visible any more.

##### Copy ICD files into the correct location

An alternative to setting an environment variable is to copy the system
ICD files into a location that conda knows.

First, find out where your conda environment is installed,
using e.g. the command `which python` when the environment is active.
The output of the command may be something like

```/home/user/miniconda3/envs/bempp/bin/python```

But this depends on whether Anaconda Python or Miniconda is installed and
where the base installation resides. The directory in which conda installs
ICDs is

```/home/user/miniconda3/envs/bempp/etc/OpenCL/vendors```

This directory already contains a file called `pocl.icd` which has been
installed through the `pocl` conda package. To use other ICD drivers
copy them over from the system directory `/etc/OpenCL/vendors`
into the above directory of your conda environment.
