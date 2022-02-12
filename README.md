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
no module named 'scipy'
Open `OSGeo4W Shell` installed with QGIS as `Administrator` and type:
```sh 
 $ python -m ensurepip --default -pip
 $ python -m pip install --upgrade pip
 $ python -m pip install scipy
 $ python -m pip install spglm
 $ python -m pip install geos=3.7.1
 $ python -m pip install shapely
```

___
### Changeset

##### Changeset 01/2022
- Fixed the export feature type error issue

##### Changeset 02/2022
- Fixed the name of Spatial kernel in the Geographically Weighted Regression (GWR) Results in the SUMMARY TXT did not change issue
