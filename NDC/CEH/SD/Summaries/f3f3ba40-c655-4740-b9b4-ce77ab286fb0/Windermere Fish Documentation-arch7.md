# Windermere Fish Abundance 1940-2012

## Overview
- Long-term dataset documenting fish abundance in Windermere, focusing on Arctic Charr (Salvelinus alpinus), Pike (Esox lucius), Perch (Perca fluviatilis), and Roach (Rutilus rutilus), plus total fish abundance from hydroacoustics.
- Data span from 1940 to 2012, with yearly averages.
- Initial data collection by the Freshwater Biological Association (FBA) until 1989; CEH and predecessor IFE have collected since 1989. Hydroacoustics data collected by CEH/IFE since 1990.
- Available downloads pertain to Windermere North and South Basins.

## Data Content and Format
- File: Windermere_fish_1940_2012.csv
- Format: comma separated values (CSV); size ~24 KB
- Primary columns:
  - YEAR: Year of measurement
  - SITE: Sampling basin/site (Windermere North basin / Windermere South basin)
  - DETERMINAND: Fish species or total detectable fish (as listed below)
  - ANNUAL_AVERAGE: Yearly mean value
  - UNITOFMEASUREMENT: Measurement unit (see specifics below)
- Key determinands (DETERMINAND) include:
  - Esox lucius (Pike)
  - Perca fluviatilis (Perch)
  - Rutilus rutilus (Roach)
  - Salvelinus alpinus (Arctic charr)
  - Total fish (hydroacoustics)
  - All detectable fish species (hydroacoustics)
- Unit of measurement (UNITOFMEASUREMENT):
  - CPUE = Catch per unit effort (fish species data)
  - fish ha-1 for hydroacoustics data
  - For some hydroacoustics entries, CPUE may be reported as fish per hectare

## Spatial and Temporal Coverage
- Spatial: Windermere Lake, Cumbria, Great Britain
  - Basin-level data for Windermere North and Windermere South
  - Approximate lake center coordinates provided: OS Grid SD393960; WGS84 54.360193, -2.935836
- Temporal: 1940–2012
  - Arctic charr monitored 1940–2012 (north basin)
  - Pike monitored 1944–present (north and south basins)
  - Perch monitored 1943–present (north and south basins)
  - Roach sampled in 1995, 2000, 2005, 2012
  - Hydroacoustics surveys conducted monthly from 1990 onward (night-time full-water-column abundance and daylight large-fish abundance in upper 20 m)

## Sampling and Collection Methods
- Pike
  - Sampling by gill nets; standardized since 1982 (64 mm bar mesh, 40 m x 3 m nets)
  - Sampling in both basins at ~10 sites per basin (October–December)
  - Weekly rotation with two-week site coverage; total annual effort ~240 net days (since 1990)
  - Laboratory processing includes measurement, weighing, sexing, aging; CPUE calculated per year per basin
- Perch
  - Standardized trapping technique (1943–present), primarily April–June
  - Early traps evolved to black tar-varnish-coated designs for improved catches
  - Data used to compute CPUE per year per basin
- Roach
  - Bottom-set gill nets; surveys at 15 inshore sites (north and south basins)
  - Varied designs across years (1995, 2000, 2005, 2012) with different net lengths, depths, and mesh sizes
  - Catches frozen and later identified/enumerated; CPUE calculated per year per basin
- Arctic charr
  - Gill nets on spawning grounds (low water depths) in October–December
  - Spawning-ground CPUE calculated for November
- Hydroacoustics
  - Night- and day-time surveys from 1990 onward
  - Initial zig-zag single-beam system (1990s); since 2002, split-beam echo sounders
  - Calibration performed periodically
  - Abundance estimates:
    - Night-time abundance of all detectable fish (entire water column)
    - Day-time abundance of large fish (>~200 mm) in upper 20 m (exploited by Arctic charr fishery)
  - Means and 95% confidence limits computed annually

## Data Quality Control and Provenance
- Quality control: measurements cross-checked by permutations of three individuals
- Hydroacoustic calibrations and methodological references cited
- Species-specific QA noted (e.g., separate QA for Arctic charr, perch, pike, roach)
- Key references for methods and datasets include:
  - Le Cren (1959, 2001) on age/growth and Windermere fish projects
  - Kipling (1984) and Elliott & Fletcher (2001) on Arctic charr assessment
  - Baroudy & Elliott (1993); Winfield et al. (2006) on hydroacoustics and sampling
  - Additional papers linked to pike, perch, roach population studies

## GIS and Data Integration Considerations
- Temporal series data suitable for time-series GIS analysis and basinal trend mapping
- Basin-level aggregation; no explicit site-point geometries for every year provided in the CSV (site-level delineation implied by NORTH/SOUTH basins)
- Spatial context includes precise OS grid and latitude/longitude for lake center for georeferencing
- Units and sampling designs vary by species and method; careful harmonization needed when combining across years or comparing CPUE across species
- Data suitable for layering with environmental covariates (eutrophication, climate change, prey abundance) to assess drivers of fish abundance

## Usage Notes and Limitations
- Roach data have limited years and variable sampling designs; interpret CPUE cautiously
- Per-year comparison requires attention to differing sampling methods and net designs across years
- Hydroacoustic data provide total and exploitable-fish abundance but are influenced by calibration and method switches over time
- Data are provided as yearly averages, which may smooth seasonal or intra-annual variability

## References and Additional Information
- Kipling, 1984; Le Cren, 1959; Le Cren, 2001
- Le Cren, E. D. (2001). The Windermere perch and pike project. Freshwater Forum
- Baroudy, E. & Elliott, J. M. (1993). The effect of large-scale spatial variation on hydroacoustics estimates
- Elliott, J. M. & Fletcher, J. M. (2001). Assessing abundance of Arctic charr
- Winfield, I. J., Fletcher, J. M. & James, J. B. (2006). Monitoring Arctic charr population in Windermere
- Winfield, I. J., James, J. B. & Fletcher, J. M. (2008). Northern pike in a warming lake
- Le Cren, E. D., (2001). Windermere perch and pike project (Freshwater Forum)