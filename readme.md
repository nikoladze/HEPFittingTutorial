# HEP Fitting Tutorial

Originally by [Kilian Lieret](https://github.com/klieret)

Jupyter notebooks preview is available [here](https://nbviewer.jupyter.org/github/nikoladze/HEPFittingTutorial/tree/master/examples/jupyter_notebooks/).

To run the tutorial, just click on:

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/nikoladze/HEPFittingTutorial/master?filepath=examples%2Fjupyter_notebooks)



## Contents

* Fitting basics: Minmize a cost function using ``scipy.optimize.minimize``
* Fitting polynomials to points using ``np.polyfit``
* Fitting arbitrary functions to points using ``scipy.optimize.curve_fit``
* Template fits using ``pyroofit``
* Histogram template fits using ``pyhf``
* Hypothesis tests with ``pyhf``


## Setup instructions

If you want to use what you learned in the tutorial on your projects later, here are some examples how you can setup the nescessary software:

### Generic

If you don't have anything setup and need both ROOT and the python packages, the easiest way is through [Anaconda](https://www.anaconda.com/products/individual#Downloads) or [Miniconda](https://docs.conda.io/en/latest/miniconda.html). After installing, create your environment using

```
conda env create -f environment.yml
```

and activate it via

```
conda activate HEPFittingTutorial
```

### On LMU jupyterhub (for Bachelor course 2022)

Most tutorials should run when you start jupyterhub with the `root/6.24.02` environment.

Then you can install additional dependencies with
```
pip3 install --user pyroofit pyhf iminuit mplhep
```

For running the ROOT 6.26 RooFit example (optional) you can add the following line to `~/jupyterhub_environment.sh`:

```
module load root/6.26.00
```

and then restart the jupyterhub server using the `python/3.9-2021.11` environment
