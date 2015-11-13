# Environments

This repo contains files that define shared environments for working on
projects. Please commit and push any changes.

## `modulefiles`

`modulefiles` contains module files that can be loaded using `module
load GATK` or `module load plink/1.90b3x` etc. 

## `anaconda`

`anaconda` contains Anaconda yml files that define Anaconda environments. You
can export an Anaconda environment by activating that environment and running

	conda env export > environment.yml

You can load an environment using

	conda env create -f environment.yml

When creating an Anaconda environment for a project, you should load that
project's module before creating the Anaconda environment. For instance, if you
want to install the cardips Anaconda environment, you should first do `module
load cardips` and then `conda env create -f cardips.yml`. This is needed
because some Python packages compile against software in your path. For
instance, rpy2 compiles against the R in your path, so if you create the
cardips Anaconda environment with one R in your path and then load the cardips
module and get a different R in your path, rpy2 will not work.  See [the
anaconda
documentation](http://conda.pydata.org/docs/using/envs.html#share-an-environment)
for more information on sharing environments.
