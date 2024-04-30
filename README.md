# Databases for landscape genomics and more

Some databases also include example code for extracting data.

## Abiotic (climate) variables databases

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
  
**CHELSA: https://chelsa-climate.org/ <br>**
Example publication here: ?? <br>
Includes: ca. 1km resolution, downscaled future projections (generally better than raw ones),  and also has stuff like growing degree days, growing season length (BIOCLIM+). CHELSA's grid cells are shifted from others by half a grid cell.

</p>

<p>
  
**CRU: https://crudata.uea.ac.uk/cru/data/hrg/ <br>**
Example publication here: ?? <br>
Includes: ca. 1km resolution, downscaled future projections (generally better than raw ones),  and also has stuff like growing degree days, growing season length (BIOCLIM+). CHELSA's grid cells are shifted from others by half a grid cell.

</p>

<p>
  
**CHELSA: https://chelsa-climate.org/ <br>**
Example publication here: ?? <br>
Includes: ca. 1km resolution, downscaled future projections (generally better than raw ones),  and also has stuff like growing degree days, growing season length (BIOCLIM+). CHELSA's grid cells are shifted from others by half a grid cell.

</p>


## Biotic variables databases

<p>
  
**Tree cover percentage: https://globalmaps.github.io/ptc.html <br>**
Example publication here: ?? <br>
Includes: there is probably new MODIS data, but not at 1km (at higher resolution)

</p>

## Human modification variables databases

<p>
  
**Light at night global radiance (NOAA Global Radiance Calibrated Nighttime Lights): https://ngdc.noaa.gov/eog/dmsp/download_radcal.html <br>**
Example publication here: https://www.pnas.org/doi/10.1073/pnas.2216789120 <br>
Includes: Night time illumination levels across the globe

</p>

<p>
  
**SEDAC population density: https://sedac.ciesin.columbia.edu/data/set/popdynamics-1-km-downscaled-pop-base-year-projection-ssp-2000-2100-rev01/data-download <br>**
Example publication here: ?? <br>
Includes: ca. 1km resolution, human population, total, "rural", and "urban", with future projections based on a few different socio-economic scenarios (SSP)

</p>

<p>
  
**SEDAC urban land extent: https://sedac.ciesin.columbia.edu/data/set/ssp-1-km-downscaled-urban-land-extent-projection-base-year-ssp-2000-2100 <br>**
Example publication here: ?? <br>
Includes: ca. 1km resolution, urban land extent

</p>

## Other databases

**Human Phenotype Ontology: https://hpo.jax.org/app/ <br>**
Example publication here: https://www.pnas.org/doi/10.1073/pnas.2216789120
