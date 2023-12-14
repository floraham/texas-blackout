
## Title: Texas Blackout: Analyzing affected areas & socioeconomic factors that influenced recovery in 2021
#### 🤠 Author: Flora Hamilton | floraham@github.io 


#### 📦 Repo Link: https://github.com/floraham/xxxx
This Github repository contains a .RMD file conducting an analysis of Texas's blackout impacts and recovery in 2021. We use 4 types of datasets to conduct this analysis. 

## Context 
"In February 2021, Texas faced a significant power crisis resulting from three severe winter storms that swept across the United States on February 10--11, 13--17, and 15--20."[^1]
[^1]: Wikipedia. 2021. "2021 Texas power crisis." Last modified October 2, 2021. <https://en.wikipedia.org/wiki/2021_Texas_power_crisis>.

## Objectives and methods of project:
-    Estimate the number of households in Houston that experienced power loss due to the initial two storms.
    -   To determine the count of homes affected by power outages, we will spatially join these areas with [OpenStreetMap](https://www.openstreetmap.org/#map=4/38.01/-95.84) data on buildings and roads.

-   Investigate whether socioeconomic factors serve as predictors of community recovery from a power outage.
    -   For the exploration of potential socioeconomic factors influencing recovery, the analysis will be linked with data from the US Census Bureau.


## Data 

#### ✨ Nightlights `VNP46A1`
- This analysis will rely on remotely-sensed night lights data acquired from the [Visible Infrared Imaging Radiometer Suite (VIIRS)](https://en.wikipedia.org/wiki/Visible_Infrared_Imaging_Radiometer_Suite) aboard the Suomi satellite. Specifically, we will use the VNP46A1 to identify variations in night lights before and after the storms, pinpointing areas that lost electrical power.

#### 🛣️ Roads  `gis_osm_roads_free_1.gpkg`
- We used [Geofabrik's download sites](https://download.geofabrik.de/) to retrieve a shapefile of all highways in Texas and prepared a Geopackage (`.gpkg` file) containing just the subset of roads that intersect the Houston metropolitan area. 

#### 🏡 Houses  `gis_osm_buildings_a_free_1.gpkg`
- We also obtain building data from OpenStreetMap. We again downloaded from Geofabrick and prepared a GeoPackage containing only houses in the Houston metropolitan area.\

#### 👨‍👩‍👧‍👦 Socioeconomic `ACS_2019_5YR_TRACT_48.gdb`
- We obtained data from the [U.S. Census Bureau's American Community Survey](https://www.census.gov/programs-surveys/acs) for census tracts in 2019. The *folder* `ACS_2019_5YR_TRACT_48.gdb` is an ArcGIS ["file geodatabase"](https://desktop.arcgis.com/en/arcmap/latest/manage-data/administer-file-gdbs/file-geodatabases.htm)


##### 💪 Spatial Skills:
-   load vector/raster data\
-   simple raster operations\
-   simple vector operations\
-   spatial joins

### Repository Structure 
```
Houston-Blackouts
│   README.md
│   Rmd/Proj files
|   .gitignore     
│
└───data
    │───gis_osm_buildings_a_free_1.gpkg
    │───gis_osm_roads_free_1.gpkg
    │
    └───ACS_2019_5YR_TRACT_48_TEXAS.gdb
    |   └  census gdb files
    |
    └───VNP46A1
        └ VIIRS night-light files
``` 

### Data Download Instructions:
### The data associated with this assignment is too large to include in the GitHub repo. Data should be stored locally and added to .gitignore file. Download data from [here](https://drive.google.com/file/d/1bTk62xwOzBqWmmT791SbYbHxnCdjmBtw/view?usp=sharing)
