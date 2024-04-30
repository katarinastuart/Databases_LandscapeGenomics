# Databases for landscape genomics and more

Includes example code for extracting data.

## Environmental variables databases

**Worldclim: https://www.worldclim.org/** <br>
Example publication here: https://www.pnas.org/doi/10.1073/pnas.2216789120 <br>
Includes: temperature and rainfall (averages, variation, minimums, maximums)<br>

```
library(raster)
library(geodist)
climdata <- getData('worldclim',download=TRUE,var='bio',res=5)
sample.coord <-read.table("metadata_au.txt", header=T, stringsAsFactors=F)
points_D3 <- SpatialPoints(sample.coord[,2:3], proj4string=climdata@crs) #coordinated provided are Long, then Lat
values_D3 <- extract(climdata,points_D3)
```

<p>

**Light at night global radiance (NOAA Global Radiance Calibrated Nighttime Lights): https://ngdc.noaa.gov/eog/dmsp/download_radcal.html <br>**
Example publication here: https://www.pnas.org/doi/10.1073/pnas.2216789120 <br>
Includes: Night time illumination levels across the globe

## Other databases

**Human Phenotype Ontology: https://hpo.jax.org/app/ <br>**
Example publication here: https://www.pnas.org/doi/10.1073/pnas.2216789120
