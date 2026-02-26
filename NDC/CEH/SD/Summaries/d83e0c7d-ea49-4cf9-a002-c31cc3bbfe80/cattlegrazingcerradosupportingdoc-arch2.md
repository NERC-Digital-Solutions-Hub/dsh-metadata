# Data overview

- Data describe plant community composition collected in 100 plots of 1-m² across ten old-growth Cerrado grasslands in São Félix do Tocantins, Tocantins, Brazil, collected in March–April 2022.
- Experimental design: 50 plots in cattle-grazed and burned old-growth grasslands and 50 plots in ungrazed and unburned old-growth grasslands (ten plots per grassland; ten old-growth grasslands total: five grazed/burned and five ungrazed/unburned).
- Data integration: from two projects—Ecological and economic evaluation of beef cattle on pastures in the Brazilian Cerrado and Optimising the long-term management of invasive species affecting biodiversity and the rural economy using adaptive management; funded by FAPESP (Grant 2020/04713-5) and NERC (Grant NE/S011641/1).
- Study area context: located over ~1,000 hectares in northern Cerrado; average altitude ~500 m; climate with dry winter (May–Sept) and humid summer (Oct–Apr); annual rainfall ~1,400–1,500 mm; average temperatures 26–27°C, with 24–27°C across the year. Predominant soil is arenosol. Historic fire–grazing regime: burned and grazed for ~100 years, fire typically in September; ungrazed/unburned sites protected for 14 years.
- Plot and transect design: in each old-growth grassland, a 50-m transect (North–South) with 10 plots of 1-m² along the transect; plots systematically distributed along the transect. Along each plot, all plant species recorded, growth form noted (graminoids, forbs, shrubs), and their percent cover estimated. If needed, material collected for later identification.
- Biomass sampling and processing: within each plot, a 0.5 m × 0.5 m subplot sampled for aboveground biomass and litter; biomass sorted into graminoid, forb, shrub, and dead biomass; dried at 80°C for 48 hours and weighed (g per 0.5 m², converted to g m⁻²).
- Key derived variables per plot: total richness, graminoid richness, forb richness, shrub richness; graminoid, forb, and shrub cover (%); dead biomass cover (%); bare ground (%); graminoid, forb, shrub, and dead biomass (g m⁻²). The average cover per site is calculated as the mean of the 10 plots (zero if a species is absent at a site).

## Vegetation sampling

- Sampling period: March–April 2022.
- Grassland types: five grazed and burned, five ungrazed and unburned old-growth grasslands.
- Transects and plots: 50-m transects per site; 10 plots per transect (1 m² each); plots distributed systematically along the transect.
- Within-plot measurements: complete species list, growth form classification, and percent cover estimates; dead biomass and bare ground estimated; biomass sampled from a 0.25 m² subplot, sorted into four categories (graminoid, forb, shrub, dead biomass) and weighed after drying.
- Data processing: conversion of biomass to g m⁻²; species covers summed across plots to obtain per-site averages; average cover across 10 plots computed per site.
- Location data: geographic coordinates of transects and grasslands are provided in a separate file.

## Data structure

- File: CattleGrazingCerrado1.txt
  - Tab-delimited; 100 rows (plots) with 16 columns:
    - site: site/old-growth grassland identifier
    - land_use: grazing/burning status (in file, values are 'grazed' for grazed sites; 'ungrazed' for ungrazed sites)
    - plot: plot identifier within site
    - total_richness: total species per 1 m²
    - shrub_richness: shrub species per 1 m²
    - graminoid_richness: graminoid species per 1 m²
    - forb_richness: forb species per 1 m²
    - shrub_cover: shrub cover (%)
    - graminoid_cover: graminoid cover (%)
    - forb_cover: forb cover (%)
    - dead_biomass_cover: dead biomass cover including litter (%)
    - bare_ground: bare soil (%)
    - shrub_biomass: shrub biomass (g m⁻²)
    - graminoid_biomass: graminoid biomass (g m⁻²)
    - forb_biomass: forb biomass (g m⁻²)
    - dead_biomass: dead biomass (g m⁻²)
- File: CattleGrazingCerrado2.txt
  - Tab-delimited; 100 rows (sites) with variable columns representing the average cover of each of the 118 recorded species per site
  - Zeros indicate absence of a species at a site
- File: CattleGrazingCerrado3.txt
  - Latitudes and longitudes for the locations of the old-growth grasslands (site coordinates)