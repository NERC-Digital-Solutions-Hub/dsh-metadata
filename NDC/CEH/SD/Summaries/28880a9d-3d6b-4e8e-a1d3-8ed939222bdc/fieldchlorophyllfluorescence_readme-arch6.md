# Data collected on Mt Etna during the field transplant in 2017

## Overview
- Field transplant experiment on Mt Etna in 2017.
- Five genotypes randomly chosen for each of two Senecio species.
- For each genotype, four cuttings per transplant elevation and four leaves per plant were measured.
- Measurements were repeated on a second day to account for weather and timing.
- Light-response measurements were recorded after 30 minutes of darkness using an IMAGING-PAM M-series chlorophyll fluorometer.

## Experimental design and scope
- Species: S. aethnensis (AE) and S. chrysanthemifolius (CH).
- Genotype: identifier from glasshouse source plants.
- TGSite: transplant site elevation.
- TGBlock: replicate field blocks.
- Grid: plant grid location within each block; genotype randomized to grid locations.
- Day: day of measurement.

## Measurements and data structure
- Fluorometer outputs: Columns 7–22 (full set of fluorometer signals); primary analysis uses PI(total), representing total photosynthetic capacity.
- Primary variable for analysis: PI(total).
- Data captured per plant/measurement across multiple days, elevations, blocks, and grid locations, with four cuttings per genotype and four leaves per plant.

## Data quality and preparation notes
- Repeated measurements on a second day to mitigate weather/time effects.
- Data structure supports aggregation by species, genotype, elevation, block, and day.
- While multiple fluorometer outputs exist (columns 7–22), analyses focus on PI(total) for photosynthetic capacity.