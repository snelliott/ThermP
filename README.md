# ThermP

This program reads in canonical partition functions and converts them into a table of thermochemical parameters: Cp, S, and H.

### Requirements

While not strictly required, ThermP makes use of output from the MESS program by default.

The user may format partition function data from some other program to match those in the examples directory. Of course, we encourage the use of MESS to calculate the input partition function data. 

The source code and installation instructions for MESS can be found at <https://github.com/Auto-Mech/MESS>. 

See below for alternative means of obtaining MESS alongside ThermP.

### Direct Installation using Conda

The most direct way to install the code is through the conda package manager.
If you have conda installed,  
(1) activate an environment in you wish to use to install ThermP, and  
(2) run the install command:
```
conda install -c auto-mech thermp
```

If you do not have a preferred Conda environment set up, an empty environment with no packages can be created and activated with the following commands
```
conda create --name myenv
conda activate myenv
```
where `myenv` should be replaced with your preferred name for the environment.

Alternatively, we also recommend building our own pre-set Auto-Mech environment, which includes ThermP, MESS and all their dependencies. This environment can be created and activated with the commands:
```
conda env create auto-mech/amech-env
conda activate amech-env
```

If your Conda commands are not functioning, you may need to iniliatize Conda via the command
```
. /path/to/conda.sh
```
which places Conda executables in your PATH. The specific location of conda.sh depends on the Conda install.

If you do not have Conda, it can be installed using the shell script
`debug/install-conda.sh`.


### Building from source using Conda environment for dependencies

To build the code from source for development or debugging purposes, first
create a conda environment with the necessary dependencies as follows:
```
conda env create -f environment.yml
```
wich will create the `thermp-env` environment.
You can then activate the environment and build the code as follows:
```
conda activate thermp-env
bash debug/build.sh
```
To put the ThermP executables in your PATH, you can then run
```
. debug/fake-install.sh
```
Note that the above command does not **permanently** alter your PATH, it only affects PATH for the current login session.


### Building from source without Conda

Run build.sh, which uses cmake to compile ThermP:
```
bash build.sh
```

Note that the results of the `make install` in build.sh will depend on your system setup.
