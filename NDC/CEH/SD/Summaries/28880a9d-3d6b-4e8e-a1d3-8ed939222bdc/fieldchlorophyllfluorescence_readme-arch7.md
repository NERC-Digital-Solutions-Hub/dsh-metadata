# Data collected on Mt Etna during the field transplant in 2017

## Overview
- Field transplant experiment on Mount Etna in 2017
- Five genotypes randomly chosen for each of two Senecio species
- Measurements:
  - Four cuttings per genotype at each transplant elevation
  - Four leaves per plant
  - Repeated measurements on a second day to account for weather and measurement timing
  - After 30 minutes of dark adaptation, light response measured with an IMAGING-PAM M-series chlorophyll fluorometer

## Variables
- Species: AE = S. aethnensis; CH = S. chrysanthemifolius
- Genotype: genotype ID from individuals grown in the glasshouse
- TGSite: elevation of transplant sites
- TGBlock: replicate field blocks
- Grid: grid location of plants within each block (genotype randomized to different grid locations)
- Day: day measurements were taken
- PI(total): total photosynthetic capacity output from the fluorometer (used for analysis)
- Columns 7-22: fluorometer outputs in the dataset, with PI(total) being the primary variable used

## Spatial/Geographic context
- Location: Mount Etna with multiple transplant elevations
- Experimental layout includes blocks and grid positions within blocks, indicating a structured spatial design

## Data structure for GIS
- Multidimensional dataset including:
  - Species, Genotype, TGSite (elevation), TGBlock (block), Grid (within-block location), Day (temporal dimension), and PI(total)
- Enables map-based visualization of PI(total) across elevations, sites, blocks, grids, and days
- Suitable for layered GIS analyses: spatial patterns by species/genotype, elevation effects, and temporal trends

## Processing and usage notes
- Data collection occurred on two days to capture variability
- Standardized protocol: dark adaptation followed by fluorometer measurement
- Primary analysis focal point: PI(total); other fluorometer outputs are available but not used in the specified analysis

## Practical considerations for GIS specialists
- Spatial alignment is crucial: blocks and grid locations must be accurately georeferenced
- Data may require harmonization across blocks and grid positions for consistent analysis
- Temporal dimension (Day) allows exploration of changes over time, in addition to spatial variation by elevation and location
- Potential challenges include managing varying resolutions across measurements and ensuring consistency in genotype and species labeling across the dataset