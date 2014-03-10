Internship-Environmental_Modelling
==================================

Hydrological modelling using the method of cellular automata (Rstudio-TerraMe-Lua) 

In this project a spatial dynamic hydrological model of cellular automata is developed. The model simulates the montly rain water flow into the river segment from it's extended watershed area. TerraMe, a programming environment for spatial dynamical modelling, is used for developing the cellular automata model. 
TerraME provides an interface to TerraLib geographical database which supports the MySQL DB. Data are visualised in TerraView,a GIS application based on TerraLib. A direct runtime link with the R programming language using the aRT package provided the statistical implementation.

Order of script running and short description.
1. R&TerraLib: Connect R with TerraLib using aRT package. Visualise shape files in TerraView creating layers. (These shape files data are not included in the uploaded project files because of no permission).  
2. SciDB: Data as raster formats retrieved from the site "http://eca.knmi.nl/download/ensembles/download.php" and stored in SciDB. This is an R script for retrieving part of daily data of SciDB, create monthly data, save in a csv file, plot data and create raster giving the coordinate reference system.  
3. Correlation coefficient: Find the correlation coefficient of elevation-precipitation. Based on P. Goovaert's paper "Geostatistical approaches for incorporating elevation into the
spatial interpolation of rainfall" for correlation < 0.75, the method of ordinary kriging is selected for precipitation data interpolation.
4. Interpolation_precipitation: Ordinary kriging for precipitation data.
