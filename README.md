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

See [the anaconda
documentation](http://conda.pydata.org/docs/using/envs.html#share-an-environment)
for more information on sharing environments.
