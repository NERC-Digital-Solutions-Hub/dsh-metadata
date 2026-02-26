# Ammonia Global Emissions from Seabirds (AGES) version 1

## Overview
- Global NH3 emission estimates from seabird colonies (AGES) version 1.
- Data are gridded at 0.1-degree spatial resolution.
- Emissions are expressed as Mg NH3 per grid cell per year.
- Three emission-factor scenarios are provided; scenario 3 is the best estimate (mean of Scenarios 1 and 2) with limited temperature dependence.

## Data specifications
- Spatial resolution: 0.1 degree (latitude/longitude) grid.
- Units: Mg NH3 per grid cell per year.
- Data rounding: values rounded to 2 significant figures.
- Version: AGES version 1.

## Emission scenarios
- Scenario 1: emission factors based on mid-latitude measurements applied globally; independent of temperature at seabird colonies.
- Scenario 2: emission factors depend on temperature at seabird colonies (thermodynamic temperature dependence), using Henry's Law and dissociation equilibria.
- Scenario 3: best estimate; limited temperature dependence (mean of Scenarios 1 and 2).

## Publication and citation
- Any use of the data must quote the publication: S. N. Riddick, U. Dragosits, T. D. Blackall, F. Daunt, S. Wanless and M. A. Sutton (2012) The global distribution of ammonia emissions from seabird colonies. Atmospheric Environment (in press) DOI:10.1016/j.atmosenv.2012.02.052

## GIS-ready considerations
- Suitable for map-based visualisations and spatial analyses; can be used as raster data.
- Ensure compatible coordinate reference system (CRS) and alignment with other layers; grid is a regular 0.1-degree lattice.
- Emissions are annual per grid cell; can be aggregated or summed to coarser resolutions as needed.
- For analyses, consider using Scenario 3 as the best-estimate dataset, with awareness of differences across scenarios.

## Limitations and notes
- Scenarios reflect different temperature dependencies; Scenario 3 represents the best estimate among them.
- Proper attribution to the cited publication is required when using the data.