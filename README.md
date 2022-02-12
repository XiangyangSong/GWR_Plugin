# Geographically Weighted Regression(GWR) Plugin for QGIS
A QGIS plugin for Geographically Weighted Regression(GWR).

___
### Installation - Windows

**1)** Install dependencies:

If you are using **QGIS 3.16**:

Open `OSGeo4W Shell` installed with QGIS as `Administrator` and type:
```sh
 $ py3_env
 $ python -m pip install --upgrade pip
 $ python -m pip install pandas
```

If you are using ***QGIS 3.22.3***
Open `OSGeo4W Shell` installed with QGIS as `Administrator` and type:
```sh 
 $ cd C:\Program Files\QGIS 3.16\apps\Python37
```
 
```sh 
$ python -m ensurepip
$ python -m pip install --upgrade pip
```
  
- ModuleNotFoundError: No module named 'spglm'
```sh 
$ python -m pip install spglm
```

 - ModuleNotFoundError: No module named 'scipy'
```sh 
$ python -m pip install scipy
```
___
### Changeset

##### Changeset 01/2022
- Fixed the export feature type error issue

##### Changeset 02/2022
- Fixed the name of Spatial kernel in the Geographically Weighted Regression (GWR) Results in the SUMMARY TXT did not change issue
