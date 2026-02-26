# Dung beetle community data from a beforeand-after El Niño experiment in the Brazilian Amazon

## Overview
- Time-series dataset of dung beetle abundance from dung-baited pitfall traps collected in 2010, 2016, and 2017.
- Focuses on the Brazilian Amazon within the NERC HTMF programme.
- Aims to quantify effects of human- and climate-induced stressors on dung beetle communities.

## Data structure and contents
- Four data sheets:
  - Species-all.sites_2010: plot-level beetle abundance for 381 plots.
  - Species-subset.sites_2016: plot-level abundance for 36 re-sampled plots (2016).
  - Species-subset.sites_2017: plot-level abundance for 36 re-sampled plots (2017).
  - Plot-position: geographical coordinates for each plot.
- Column formats:
  - Each species is a row entry; subsequent columns correspond to plot identifiers.
  - Plot-position includes Plot code, Municipality, UTM X, UTM Y, and UTM zone information.

## Experimental design and sampling regime
- Study regions: Paragominas (PGM) and Santarém/Santarém Belterra Mojuí dos Campos (Santarém).
- 18 catchments (32–61 km2) distributed along forest cover gradients.
- Plot distribution:
  - Non-forest plots: pastures and mechanised agricultural lands.
  - Forest plots: primary forests and second-growth after agricultural abandonment.
  - Total plots: 381 (2010) across 234 forest and 147 non-forest plots.
- Sampling years and scope:
  - 2010: all 381 plots sampled (April–June).
  - 2016 and 2017: 36 forest plots within Santarém region, sampled as a before/after comparison relative to El Niño.
- Disturbance gradient for 2016/2017 plots: undisturbed, logged, logged-and-burned, and secondary forests.

## Data collection methods
- Trapping: dung beetles captured with pitfall traps baited with 50 g of dung (80% pig, 20% human) and a killing solution.
- Trap layout: three traps per sampling point arranged at corners of a 3-m equilateral triangle along a 300-m transect; traps left for 48 hours.
- Sampling consistency: methods replicated in 2016 and 2017; permits obtained for private and protected areas.

## Files and variables
- 2010: dung-beetles_ECOFOR_AFIRE_RAS_all.sites_2010.csv
  - 381 plots (columns) by species (rows) with trap counts per plot.
- 2016: dung-beetles_ECOFOR_AFIRE_RAS_subset.sites_2016.csv
  - 36 plots (columns) by species (rows).
- 2017: dung-beetles_ECOFOR_AFIRE_RAS_subset.sites_2017.csv
  - 36 plots (columns) by species (rows).
- Plot-position: dung-beetles_ECOFOR_AFIRE_RAS_all_plot-position.csv
  - Plot, Municipality, UTM_X, UTM_Y, UTM_zone.

## Spatial and temporal coverage
- Temporal: 2010 (pre-El Niño), 2016 & 2017 (post-El Niño period).
- Spatial: two regions in eastern Amazon (Paragominas and Santarém area) with plots across a forest cover and disturbance gradient.
- Coordinates use UTM zones 21M and 22M.

## Licensing, access, and citation
- Data cited: França et al. (2019) Dung beetle community data from a beforeand-after El Niño experiment in the Brazilian Amazon. NERC Environmental Information Data Centre.
- DOI and license details provided for data access and reuse restrictions.
- Proper citation required when using the data.

## Potential analyses and uses for analysts
- Assess pre- vs post-El Niño changes in dung beetle communities.
- Examine responses to forest disturbance gradients (undisturbed, logged, logged-and-burned, secondary).
- Explore species richness, abundance, and community composition across years and land-use types.
- Integrate plot-level spatial data (Plot-position) with environmental covariates for spatial analyses.
- Develop predictive models of dung beetle responses to climate stressors and land-use change.

## Limitations and considerations
- Uneven sampling across years: full 381-plot coverage only in 2010; 2016/2017 limited to 36 plots.
- Methodological consistency maintained, but cross-year comparability should account for subset sampling.
- Data are abundances from pitfall traps; species identifications are as recorded in the dataset.
- Metadata includes permissions and regional context; users should consult licenses for reuse.