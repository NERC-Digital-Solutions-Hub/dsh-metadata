# Wetland life project, species table for larval and adult mosquitos at various wetland sites, samples from April to October 2017 and 2018

## Overview
- A dataset of mosquito counts by life stage and species across 12 UK wetland sites.
- Samples collected from April 2017 to September/October 2018 (adult and larval data).
- Aims to document mosquito diversity and abundance to support wetland suitability predictions and related research.

## Data collection and methods
- Study design:
  - 12 wetland sites sampled in the UK.
  - Adult mosquitoes: Mosquito Magnet traps deployed at each site, operated continuously for four days and four nights every fortnight from early April to late October.
  - Larval mosquitoes: Surveys conducted once per target water body in May, July, and September.
- Collection specifics:
  - Adults: Traps emit CO2 and heat and are baited with octenol to attract mosquitoes.
  - Larvae: 1 L of surface water sampled per site; approximately 200 mL collected into a white container; larvae collected with a pipette and preserved in 75% ethanol.
- Data scope:
  - Data include total counts by life stage, species, site, and year/month.

## Data structure and units
- File format: CSV.
- Columns:
  - Date year, site, site latitude and longitude (formatted with degrees, minutes, seconds).
  - A subsequent species table with a column for every species observed in the study.
- Units: Total counts by life stage and species, aggregated by site and year/month.

## Quality control
- Species identification performed using published keys, with secondary verification within the team.
- Methods were adjusted to suit site topography.
- Data indicate relative species distribution per site; there is no guarantee of completely uniform sampling effort, so absolute population density estimates are approximate.

## Spatial and temporal coverage
- Spatial: 12 wetland sites across the United Kingdom.
- Temporal: April 2017 to September 2018 (adult traps run through Oct in some years; larval surveys in May, July, September).

## Data interpretation and GIS relevance
- Enables mapping of species presence/absence and abundance per site and time.
- Can be combined with site metadata (locations, habitat features) to analyze spatial patterns and drivers of mosquito distributions.
- Suitable for creating visualization dashboards, trend analyses, and informing wetland suitability tools.

## Related publications and outputs
- Mosquito diversity and abundance in English wetlands → guidance for wetland suitability prediction tools (Parasites & Vectors, 2022, submission noted).
- Mosquito magnet traps for monitoring host-seeking Simulium (2018 abstract).
- Wetland mosquito survey handbook: assessing suitability of British wetlands for mosquitoes (Natural Resources Institute, 2020).
- Interdisciplinary investigations on values of English wetlands (2022).
- Mosquito Magnet traps as a potential means of monitoring blackflies (2021).

## Considerations and limitations for users
- Sampling effort is not guaranteed to be perfectly consistent across sites and times.
- Absolute density estimates are approximate due to variability in sampling effort and method adaptation by site.
- Data should be used with awareness of potential spatial and temporal biases when performing comparative analyses.