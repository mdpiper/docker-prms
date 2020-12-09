# prms-pymt

A Docker image, built on condaforge/miniforge3,
with all PRMS pymt components installed into the base environment.

Build the image with:
```
docker build --tag prms-pymt .
```

Launch an interactive container with:
```
docker run -it --rm prms-pymt 
```

Work with the components in the container through IPython:
```
(base) root@e509673e5c28:/opt# ipython
Python 3.7.6 | packaged by conda-forge | (default, Jan  7 2020, 22:33:48)
Type "copyright", "credits" or "license" for more information.

IPython 5.8.0 -- An enhanced Interactive Python.
?         -> Introduction and overview of IPython's features.
%quickref -> Quick reference.
help      -> Python's own help system.
object?   -> Details about 'object', use 'object??' for extra details.

In [1]: import pymt

In [2]: pymt.MODELS
Out[2]: {'Subside', 'PRMSSoil', 'PRMSSurface', 'Hydrotrend', 'Cem', 'Waves', 'Plume', 'Sedflux3D', 'PRMSGroundwater', 'FrostNumber', 'Avulsion', 'Ku', 'PRMSStreamflow'}
```
