Install the R ArcGIS Tools
==========================

Install and update the R ArcGIS Bridge with this Python toolbox.


Prerequisites
-------------

 - [ArcGIS 10.3.1](http://desktop.arcgis.com/en/desktop/) or [ArcGIS Pro 1.1](http://pro.arcgis.com/en/pro-app/) ([don't have it? try a 60 day trial](http://www.esri.com/software/arcgis/arcgis-for-desktop/free-trial))
 - [R Statistical Computing Software, 3.1.0 or later](http://cran.cnr.berkeley.edu/bin/windows/base/)
  + 32-bit version required for ArcMap, 64-bit version required for ArcGIS Pro (Note: the installer installs both by default).
  + 64-bit version can be used with ArcMap by installing [Background Geoprocessing](http://desktop.arcgis.com/en/desktop/latest/analyze/executing-tools/64bit-background.htm) and configuring scripts to [run in the background](http://desktop.arcgis.com/en/desktop/latest/analyze/executing-tools/foreground-and-background-processing.htm).

How to Run
----------

First, make sure you've installed an appropriate version of R, 3.1 or later. 

###ArcGIS 10.3.1
 - In the [Catalog window](http://desktop.arcgis.com/en/desktop/latest/map/working-with-arcmap/what-is-the-catalog-window-.htm), nagivate to the folder containing the Python Toolbox, `R Integration.pyt`. _Note_: You may have to first add a folder connection to the location that you extracted the files or downloaded via Git.
 - Open the toolbox, which should look like this:

![](https://github.com/R-ArcGIS/r-bridge-install/blob/master/img/r-bridge-install-arcmap.png)

 - Run the `Install R bindings` script. You can then test that the bridge is able to see your R installation by running the `Print R Version` and `R Installation Details` tools, and running the included [sample tools](https://github.com/R-ArcGIS/r-bridge/tree/master/package/arc/inst/examples).

###ArcGIS Pro 1.1
 - In the [Project pane](https://pro.arcgis.com/en/pro-app/help/projects/the-project-pane.htm), either navigate to a folder connection containing the Python toolbox, or right click on *Toolboxes* > *Add Toolbox* and navigate to the location of the Python toolbox.
 - Open the toolbox, which should look like this:

![](https://github.com/R-ArcGIS/r-bridge-install/blob/master/img/r-bridge-install-pro.png)

  - Run the `Install R bindings` script. You can then test that the bridge is able to see your R installation by running the `Print R Version` and `R Installation Details` tools, and running the included [sample tools](https://github.com/R-ArcGIS/r-bridge/tree/master/package/arc/inst/examples).

###Problems Installing?
 - A few things to check:
    + All [prerequisites](#prerequisites]) have been met, such as the right version of R for your platform, and the latest releases of ArcGIS (ArcMap 10.3.1 / Pro 1.1).
    + Make sure that your user has administrator access, and try running ArcGIS as an Administrator:
     - Start ArcGIS as an administrator, by right clicking the icon, selecting 'Run as Administrator', then trying the script
     - If that doesn't work, the package directory, "arcgisbinding", that gets installed into the R folder (usually, C:\Users\<username>\Documents\R\win-library\) into the requested place, C:\Program Files (x86)\ArcGIS\Desktop\Rintegration
 (this step is only required for the initial install).
    + On Windows 7, [KB2533623](https://support.microsoft.com/en-us/kb/2533623) must be installed.
 - Still stuck? [Add an issue and we'll take a look](https://github.com/R-ArcGIS/r-bridge-install/issues). ([More about GitHub Issues](https://help.github.com/articles/about-issues/).)


Next Steps
----------

Want to use tools others have developed?
 - See how complex problems can be solved with R and ArcGIS in the [Sample Tools](https://github.com/R-ArcGIS/r-sample-tools), such as model-based clustering and combining parametric and non-parametric models with semiparametric regression.
 - Check out the community page for more tools _Coming Soon_

Want to develop new tools using R?
 - Develop new R-based tools using the R package `arcgisbinding`, which is described in the [bridge repository](https://github.com/R-ArcGIS/r-bridge) and the [package documentation](https://r-arcgis.github.io/assets/arcgisbinding.pdf)

Credits
-------

This toolbox depends on the R Statistical Computing Software:

> Copyright (C) 2015 The R Foundation for Statistical Computing
> R is free software and comes with ABSOLUTELY NO WARRANTY.
