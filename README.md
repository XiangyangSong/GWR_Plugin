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
- Fixed an issue of export feature type error. 

##### Changeset 02/2022
- Fixed an issue that the name of spatial kernel in the Geographically Weighted Regression (GWR) remained unchanged in the output summary .txt file. 
- Changed the way of importing geographical coordinates from selecting coordinates attributes inside shapefile layer to opening .csv sheet file. As a result, user is required to proceed one additional step after opening the .csv file: mannually type the names of two fields indicating coordinates x and y in the .csv file opened. 
- Fixed the unit problem of fixed and adaptive kernel type. The unit for fixed kernel type is "meters" instead of kilometers in our plugin. 
- Updated ShortHelpString.html document to provide more information on help page in the plugin, with an improved layout.
