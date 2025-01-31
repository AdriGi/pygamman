pygamman: Python interface to PreTEOS-10 neutral density fortran code - How Install the Neutral Density Package
================================================================================================

Jackett, David R., Trevor J. McDougall, 1997: A Neutral Density Variable for the World's Oceans. J. Phys. Oceanogr., 27, 237–263. doi: 10.1175/1520-0485(1997)0272.0.CO;2

- Author: 
- License: BSD 3-clause

See:
http://www.teos-10.org/preteos10_software/neutral_density.html


About
-----
Neutral Density surfaces are the most natural layer interfaces stratifying the deep ocean circulation. Neutral Density arises as the continuous analogue of discretely defined locally-referenced potential density surfaces, surfaces which have long been recognised as the most sophisticated for deep ocean density stratification. To account for the compressible nature of sea-water, neutral density is a function of both hydrography and geographical position, and as such is much simpler to use than the cumbersome potential density surface method currently in use.

The Neutral Density code comes as a package of FORTRAN routines which enable the user to fit neutral density surfaces to arbitrary hydrographic data. The FORTRAN implementation consists of a FORTRAN subroutine which labels a cast of hydrographic data with neutral density, and another subroutine which then finds the positions of specified neutral density surfaces within the water column. All code comes with documentation in the form of Readme files, as well as Makefiles and examples to provide check values for the user.



Installation (only tested on Ubuntu 14.04 with gcc 4.8.2 and numpy 1.9.0, Linux Mint 22.1 and numpy 1.9.0, and Ubuntu on Linux)
----------------------------------------------------------------------------------------------
Requires f2py, gfortran (or other fortran compiler)

If you are using Debian: **sudo apt-get install gfortran**

**NOTE**

In case you are using guidov version install in python 2.7, however, my suggestion is to try to install in python 3.7 building a environment using this command:  
**create --name myenv python=3.7**

After you create the new environment, active using **conda activate myenv** and you need to install numpy in this version **conda install -y numpy=1.9.3**. 

Now you will build and setup the pygamman package. However, in case you are using Python 3.7 you will need to use my setup.py version to work well. In case you are using Python 2.7 you can use guidov version.


**********************************************************

You can build the package locally using

    [~]$ python setup.py build

or install the package to the standard Python path using:

    [~]$ python setup.py install

Or, to install to another location, use

    [~]$ python setup.py install --prefix=/path/to/location/

Then make sure your PYTHONPATH environment variable points to this location.

**********************************************************

In case you didn't have configurated the path you can copy the pygamman-master files and paste to a folder called pygamman inside your environment created. Usually the path is /home/username/miniconda3/envs/myenv/lib/python3.7/site-packages/pygamman/.

Do test running using examples made available in the folder and make sure the output results are the same than the output result available in the folder. Don't forget to update your numpy package using **conda install -y numpy**.

After you test you can install in your official environment. In this case you just need to come back your numpy to old version to install the package correctly.



