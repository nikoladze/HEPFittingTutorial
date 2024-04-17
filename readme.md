# HEP Fitting Tutorial

Originally by [Kilian Lieret](https://github.com/klieret)

Jupyter notebooks preview is available [here](https://nbviewer.jupyter.org/github/nikoladze/HEPFittingTutorial/tree/bachelor-tutorial-2023/examples/jupyter_notebooks/).

## Contents

* Fitting basics: Minmize a cost function using ``scipy.optimize.minimize``
* Fitting polynomials to points using ``np.polyfit``
* Fitting arbitrary functions to points using ``scipy.optimize.curve_fit``
* Fitting with `ROOT`
* Template fits using ``RooFit``
* *Histogram template fits using ``pyhf``* (not covered in the course)
* *Hypothesis tests with ``pyhf``* (not covered in the course)


## Setup instructions

Here are some examples how you can setup the nescessary software:

### On LMU jupyterhub (for Bachelor course 2024)

Most tutorials should run when you start jupyterhub with the latest python environment.

To get a copy of the code, run the following in a terminal

```
git clone -b bachelor-tutorial-2024 https://github.com/nikoladze/HEPFittingTutorial.git
```

For running the ROOT 6.26 RooFit example you can add `module load root/6.26.00` to `~/jupyterhub_environment.sh`:

```
echo "module load root/6.26.00" > ~/jupyterhub_environment.sh
```

Then restart the jupyter server and select the `python/3.9-2021.11` environment. Keep in mind `~/jupyterhub_environment.sh` will be always loaded when you start a jupyterhub server, so you may want to delete/move the file when you don't need it anymore.

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
