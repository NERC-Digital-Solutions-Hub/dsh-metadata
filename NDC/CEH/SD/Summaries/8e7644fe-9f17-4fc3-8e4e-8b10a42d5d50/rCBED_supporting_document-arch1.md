# Concentration-Based Estimation of Deposition (CBED) methodology

## Overview
- Generates 5x5 km resolution gridded estimates of deposition flux for nitrogen, sulfur, and base cations.
- Based on measured concentrations of gases/particulate matter in air and ions in precipitation from the UK Eutrophying and Acidifying Pollutants (UKEAP) network.
- Observations interpolated to map air/precipitation concentrations across the UK; deposition split into dry and wet components.

## Dry deposition methodology
- Deposition to five land-cover categories (forest, moorland, grassland, arable, urban) using land-cover–specific deposition velocities.
- Grid-square mean deposition is a weighted combination according to land-cover fractions within the 5x5 km cell.
- Species included: sulfur dioxide (SO2), nitric acid (HNO3), nitrogen dioxide (NO2), ammonia (NH3), and particulate matter (sulfate, nitrate, ammonium, calcium, magnesium).

## Wet deposition methodology
- Wet deposition includes deposition from precipitation and occult deposition (cloud droplets directly to vegetation).
- Separation of anthropogenic (non-seasalt) and total components for sulfur and calcium using sea-water ion ratios.
- Orographic enhancement factor accounts for increased precipitation in upland areas (seeder–feeder effect) and is applied to precipitation concentrations.
- Wet deposition mapped for sulfate, ammonium, nitrate, calcium, magnesium, and acidity (hydrogen ion).

## Data sources and modelling
- NO2 concentrations: PCM model (Stedman et al., 2007) combining rural measurements with point/line-source modelling.
- NH3 concentrations: FRAME atmospheric transport model plus UKEAP annual measurements; FRAME provides local-scale variability.
- SO2 concentrations: derived from rural measurements with an urban enhancement factor.
- Wet deposition relies on precipitation and orographic factors; dry deposition relies on land-cover velocities.

## Uncertainty and temporal coverage
- Substantial uncertainty in interpolating UK-wide deposition from a relatively sparse network; true inter-annual variability due to weather patterns.
- Estimates averaged over three-year periods (end-year given) to smooth variability.
- Earlier years (pre-1996) have greater uncertainty because aerosols were not always measured; retrospective estimates use long-term mean fractions relative to wet deposition.

## Implementation and reproducibility
- Originally implemented in Genstat; re-implemented in R.
- Small numerical differences from Genstat due to spatial interpolation (kriging) and the use of long-term means/orographic enhancement factors rather than yearly recalculation.

## Quality control
- Methods align with Government analytical model QA practices.
- Peer reviewed; participated in Defra model inter-comparison exercises (Carslaw 2011).
- Documentation, version control, and central storage of code; mass-balance checks for numerical consistency and comparison with previous years.

## Data structure and files
- Data exported from raster format to CSV in xyz format.
- Three files covering 1986–2012 (three-year means ending each year):
  - rCBED_Fdep_gm2y_1986-2012_gridavg.csv: mean deposition weighted by land-cover fractions.
  - rCBED_Fdep_gm2y_1986-2012_forest.csv: deposition to forest (grid cells assumed full forest cover).
  - rCBED_Fdep_gm2y_1986-2012_moor.csv: deposition to moorland (grid cells assumed full moorland cover).
- Common structure includes: year (end-year of 3-year period), easting, northing (OS GB grid in metres), and deposition flux components:
  - H (hydrogen ions)
  - NOx (oxidised nitrogen: HNO3 + NO2 + NO3)
  - NHx (reduced nitrogen: NH3 + NH4)
  - Ntot (total nitrogen: NOx + NHx)
  - SOx (sulfur: SO2 + aerosol SO4 + total SO4 in precipitation)
  - xSOx (non-marine sulfur: SO2 + aerosol SO4 in precipitation)
  - Ca (calcium)
  - Mg (magnesium)
  - CaMg (calcium + magnesium)
  - Cl (chloride)
- Units: g m^-2 year^-1 for deposition fluxes.
- grid cells reflect five land-cover categories; grid-average is a weighted mean.

## Coverage and references
- Coverage: 1986–2012, UK, 5x5 km grid, with annual deposition components and land-cover breakdowns.
- Related references cover model development, uncertainty analyses, and supporting methodologies (e.g., Beswick et al., Dore et al., Fowler et al., Stedman et al., Smith et al., and RoTAP reports).
- Resource links provided for UK Acidifying and Eutrophying Atmospheric Pollutants and related network information.