# Geographically Weighted Regression(GWR) Plugin for QGIS
A QGIS plugin for Geographically Weighted Regression(GWR).

**THIS PLUGIN VERSION IS BASED ON MGWR: LATEST RELEASED VERSION >= 2.1.2**  [other versions here](https://github.com/pysal/mgwr/)

The Plugin implements Geographically Weighted Regression(GWR) statistics to perform spacial analysis. Users can choose some parameters and perform action. And the results will display with style. The plugin requires MGWR (see the repository for installation instruction).

**Note**: We need use some new functions, they are not included in mgwr-2.1.2 version, but in unrelease version. So the export summary function is unavailable now. If these functions are available, I will update this plugin in time. 
___
### Installation - Windows

**1)** Install dependencies:

Open `OSGeo4W Shell` Shell installed with QGIS as `Administrator` and type:
```sh
 $ python -m pip install --upgrade pip
 $ python -m pip install mgwr -U
```

**2)** Install plugin in QGIS:

Open `QGIS 3` and go to `Plugins` -> `Manage and Install plugins` -> `Settings` -> `Show also experimental plugins` 

In `All plugins` tab, look for `GWR(Processing)` and tick the checkbox.  

A new icon for Geographically Weighted Regression will appear on the QGIS main panel and in the 'Processing Toolbox' panel.

**3)** Also you can install plugin from `zip folder`:

Download the zip folder of the repository at:
https://github.com/XiangyangSong/gwr_processing/archive/refs/heads/qgis3gwr1.zip

Open QGIS 3 and go to `Plugins` -> `Install from ZIP`

Select the downloaded zip folder and press `Install plugin`. The icon for the GWR plugin will appear in the list of the installed plugins. Tick the Checkbox to activate it. The plugin will appear in the 'Processing Toolbox' panel.


**Note**: In case of errors rising from the `Pandas`, `Scipy`, `Spglm`, `Shapely` package, open `OSGeo4W Shell` installed with QGIS3 as `Administrator` and type:
```sh
 $ python -m pip install pandas -U
 $ python -m pip install scipy -U
 $ python -m pip install spglm -U
 $ python -m pip install shapely -U
```

In case of does not find python, open `OSGeo4W Shell` installed with QGIS3 as `Administrator` and type:
(e.g. jump to the python environment directory in QGIS folder where in your computer):
```sh 
 $ cd C:\Program Files\QGIS 3.16\apps\Python37
```
If there is an error of pip, open `OSGeo4W Shell` installed with QGIS3 as `Administrator` and type:
- ModuleNotFoundError: No module named 'pip'
```sh 
$ python -m ensurepip
$ python -m pip install --upgrade pip
```

___
### Installation - Ubuntu

**1)** Install dependencies:

Open `Terminal` and type the commands:
```sh
 $ python3 -m pip install --upgrade pip
 $ python3 -m pip install mgwr -U
```

**2)** Refer to previous steps `Installation - Windows` -> `2) Install plugin in QGIS` and `3) Also you can install plugin from zip folder`

**Note**: In case of errors rising from the `AttributeError: module 'sys' has no attributre 'argv'`, Open `Terminal` and type the commands: 
```sh
 $ python3 --version
 $ pip3 list
```

Then check your python environment. Maybe the environment in which your QGIS is running is not a standard python environment, some caused by the following:

- **May be caused by your Python version and LIBPYSAL version conflict**  [click here](https://pysal.org/libpysal/installation.html)
___
### Changeset

##### Changeset 05/2022
- Publish the new version v0.1.2
- Fix some issues and update the metadata file.

##### Changeset 04/2022
- Add new features. Add styles to the output layer.

##### Changeset 03/2022
- Improve the code. Automatically get the geometry type of the currently selected input layer, and calculate the centroid coordinates

##### Changeset 02/2022
- Fixed an issue of export feature type error. 

##### Changeset 01/2022
- Fixed an issue that the name of spatial kernel in the Geographically Weighted Regression (GWR) remained unchanged in the output summary .txt file. 
- Changed the way of importing geographical coordinates from selecting coordinates attributes inside shapefile layer to opening .csv sheet file. As a result, user is required to proceed one additional step after opening the .csv file: mannually type the names of two fields indicating coordinates x and y in the .csv file opened. 
- Fixed the unit problem of fixed and adaptive kernel type. The unit for fixed kernel type is "meters" instead of kilometers in our plugin. 
- Updated ShortHelpString.html document to provide more information on help page in the plugin, with an improved layout.

___
**Reference Article**

[*"MGWR: A Python Implementation of Multiscale GeographicallyWeighted Regression for Investigating Process Spatial Heterogeneity and Scale"*](https://www.mdpi.com/2220-9964/8/6/269/pdf)
___
##### License

_The Geographically Weighted Regression(GWR) Plugin is free software; you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation_

Copyright © 2022 Jiawei Gao - [Politecnico Di Milano](https://www.polimi.it/) | Xiangyang Song - [Politecnico Di Milano](https://www.polimi.it/) 

E-mail: 

xiangyang.song@mail.polimi.it 

jiawei.gao@mail.polimi.it
