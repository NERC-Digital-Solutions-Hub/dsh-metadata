# Dung beetle community data from a beforeand-after El Niño experiment in the Brazilian Amazon

## Overview

- Time series dataset of dung beetle abundance from pitfall traps, collected in 2010, 2016, and 2017 (six years before and after the 2015–16 El Niño), part of the NERC Human-Modified Tropical Forest (HTMF) programme.
- Four data files are provided: all sites 2010, subset sites 2016, subset sites 2017, and plot-position coordinates.
- Aims to assess how human- and climate-induced stressors influence tropical forests biodiversity and dung beetle communities.

## Data files and structure

- dung-beetles_ECOFOR_AFIRE_RAS_all.sites_2010.csv
  - Plot-level abundance matrix for 381 plots (rows: species; columns: plots).
  - Columns include Species and Plot identifiers (e.g., 100_1, 100_10).

- dung-beetles_ECOFOR_AFIRE_RAS_subset.sites_2016.csv
  - Plot-level abundance matrix for 36 re-sampled plots in 2016 (same format as 2010).

- dung-beetles_ECOFOR_AFIRE_RAS_subset.sites_2017.csv
  - Plot-level abundance matrix for 36 re-sampled plots in 2017 (same format as 2010).

- dung-beetles_ECOFOR_AFIRE_RAS_all_plot-position.csv
  - Plot-level geographic coordinates for all study plots.
  - Columns: Plot, Municipality, UTM_X, UTM_Y.
  - Note: Paragominas lies in UTM zone 22M; Santarém, Belterra and Mojuí dos Campos lie in 21M.

## Experimental design and sampling regime

- Regions: Paragominas (PGM) and Santarém/Belterra/Mojuí dos Campos (Santarém STM) in eastern Brazilian Amazon.
- Catchments: 18 catchments (32–61 km²) with 381 plots, distributed across gradients of forest cover and disturbance.
- Plot types: mixture of non-forest (pastures, mechanised agriculture) and forest plots (primary and secondary forests).
- 2010: full survey across 381 plots (3429 pitfall traps).
- 2016 and 2017: a subset of 36 forest plots surveyed within Santarém region, sampled to reflect a gradient of previous forest degradation (undisturbed, logged, logged-and-burned, secondary forests).
- Disturbance classification based on canopy disturbance time-series (1988–2010) and prior field assessments.

## Data collection methods

- Dung beetles collected with pitfall traps baited with 50 g dung (80% pig, 20% human) and 5% detergent + 2% salt killing solution.
- Trap setup: corners of a 3-m equilateral triangle along a 300-m transect; sampling at 0, 150, and 300 m; traps left for 48 hours.
- Consistent methodology across 2010, 2016, and 2017; permits secured from landowners and protection authorities.

## GIS-relevant details

- Plot identifiers link across datasets (e.g., 100_1, 100_10), enabling temporal and spatial joins.
- Spatial coordinates provided for all plots in UTM coordinates, with explicit zone information per locality.
- Data suitable for map-based visualization and spatial analyses of abundance across space, time, and disturbance gradients.

## Access, licensing, and citations

- Data citation: França, F.M.; Oliveira, V.H.; Louzada, J.N.C.; Vaz-de-Mello, F.Z.; Ferreira, J.N; Berenguer, E.; Gardner, T.; Lees, A.; Barlow, J. (2019). Dung beetle community data from a beforeand-after El Niño experiment in the Brazilian Amazon. NERC Environmental Information Data Centre. https://doi.org/10.5285/799db965-3ce7-4e9b-8590de6a8624d652
- For data access, reuse limitations and licensing, visit: https://doi.org/10.5285/799db965-3ce7-4e9b-8590-de6a8624d652
- Funders and project context: NERC HTMF programme; supported by NERC, Darwin Initiative, EMBRAPA, CNPq, INCT Biodiversidade e Uso da Terra na Amazônia, and Formas.