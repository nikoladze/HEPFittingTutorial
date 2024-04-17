# HEP Fitting Tutorial

Originally by [Kilian Lieret](https://github.com/klieret)

Jupyter notebooks preview is available [here](https://nbviewer.jupyter.org/github/nikoladze/HEPFittingTutorial/tree/bachelor-tutorial-2023/examples/jupyter_notebooks/).

To run the tutorial, just click on:

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/nikoladze/HEPFittingTutorial/bachelor-tutorial-2023?filepath=examples%2Fjupyter_notebooks)


## Contents

* Fitting basics: Minmize a cost function using ``scipy.optimize.minimize``
* Fitting polynomials to points using ``np.polyfit``
* Fitting arbitrary functions to points using ``scipy.optimize.curve_fit``
* Fitting with `ROOT`
* Template fits using ``RooFit``
* *Histogram template fits using ``pyhf``* (not covered in the course)
* *Hypothesis tests with ``pyhf``* (not covered in the course)


## Setup instructions

If you want to use what you learned in the tutorial on your projects later, here are some examples how you can setup the nescessary software:

### On LMU jupyterhub (for Bachelor course 2024)

Most tutorials should run when you start jupyterhub with the latest python environment.

For running the ROOT 6.26 RooFit example you can add `module load root/6.26.00` to `~/jupyterhub_environment.sh`:

```
echo "module load root/6.26.00" > ~/jupyterhub_environment.sh
```

Then restart the jupyter server and select the `python/3.9-2021.11` environment.

For the pyhf tutorials (not covered in the course) you can install the additional dependencies via
```
pip install pyhf iminuit mplhep # only needed for the pyhf tutorials
```

### Generic

If you don't have anything setup and need both ROOT and the python packages, the easiest way is through [Anaconda](https://www.anaconda.com/products/individual#Downloads) or [Miniconda](https://docs.conda.io/en/latest/miniconda.html). After installing, create your environment using

```
conda env create -f environment.yml
```

and activate it via

```
conda activate HEPFittingTutorial
```
