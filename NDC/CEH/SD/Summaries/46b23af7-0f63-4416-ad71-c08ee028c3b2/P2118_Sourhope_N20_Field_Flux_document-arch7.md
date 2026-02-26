# The influence of land-use management practices on species and functional biodiversity of nitrite oxidising bacteria and nitrification and denitrification processes

## Overview
- NERC Soil Biodiversity Thematic Programme (established 1999) focused on soil biodiversity and the functional roles of soil organisms in key ecological processes.
- Field data collected at Sourhope, Scottish Borders, to study how land management affects nitrogen cycling (nitrifiers/denitrifiers) and related gas fluxes (nitrous oxide, N2O).

## Spatial design and sampling
- Site: upland agricultural grassland soil; sampling areas S, T, U, V along the field site.
- Treatments: Control, Lime, Nitrogen, Nitrogen + Lime (randomised within sub-plots).
- Experimental structure: blocks, main plots (A–F), sub-plots; grid coordinates provided (CELL_X, CELL_Y) to map spatial positions.
- Chamber placement considerations: chambers placed only on ridges (not furrows) due to soil moisture differences; randomised block treatment allocations.
- Chamber setup: 40 cm diameter PVC tubes (20 cm long) with gas sampling tubes; lids designed to maintain gas-tight seals; careful, repeatable placement pattern.

## Data collection and laboratory methods
- Static chamber measurements of nitrous oxide (N2O) flux in field from May 2000 to Nov 2001.
- Gas sampling: Tedlar bags or 10 mL syringes; analysis by gas chromatography with electron capture detector (GC-ECD).
- Calibration: standards injected at start/end to account for drift; detection limits ~30–40 ppb for N2O.
- Analysis workflow: sample loop injection, backflush cleanup, separation on Poropak Q column; retention time ~2.87 minutes for N2O; careful handling of interferents (e.g., water).

## Data structure and fields (Dataset 1006)
- Dataset: Soil Nitrous oxide field flux data (P2118_SOIL_N2O_FIELD_FLUX_DATA.csv).
- Key fields:
  - EXP_ID (text): block/main plot/sub-plot identifier.
  - EXP_DATE (date): sampling date or period.
  - BLOCK (numeric): block number (1–5).
  - MAIN_PLOT (text): main plot label (A–F).
  - SUB_PLOT (text): sub-plot identifier.
  - CELL_X, CELL_Y (numeric): cell grid coordinates.
  - TREATMENT (text): soil treatment (Control, Lime, Nitrogen, Nitrogen & Lime, Biocide).
  - NITROUS_OXIDE_FLOW (numeric): net production/flux of N2O (µg N2O-N m^-2 h^-1); positive = emission.
- Units and data types specified; missing values labeled as Null.

## Data quality and provenance
- Quality control: numeric range checks, formatting conformity, and logical integrity checks.
- Note: Data are subject to quality assurance procedures, but no warranty on accuracy or fitness for purpose; liability disclaimer applies.

## Key findings (context for GIS interpretation)
- Lime application increased gross nitrification rates and altered the NO:N2O flux ratio (approx. 1.6 µg N d^-1 increase in nitrification).
- Nitrogen addition increased both nitric and nitrous oxide flux; however, nitrification rates under all nitrogen-related treatments decreased relative to control and lime-only treatments.
- Data are structured to enable spatial analyses of flux across the grid (CELL_X, CELL_Y) and to relate flux patterns to treatments and block design.

## GIS-relevant implications and usage
- Enables map-based visualization of N2O flux across the field site, with spatial alignment to blocks, main plots, sub-plots, and grid cells.
- Facilitates integration with other spatial data (topography, ridge/furrow distinctions, soil properties) to explore drivers of gas flux variability.
- Supports multi-resolution data integration by linking plot- and cell-level measurements to broader treatment zones.

## References and related materials
- Davies, C.A. (2005). Nitric and nitrous oxide production and emission from an upland agricultural grassland soil (Doctoral dissertation, University of Edinburgh).
- Scott et al. (2003). Sourhope Field Data Handbook 2003.
- Usher et al. (2006). Understanding biological diversity in soil: the UK's Soil Biodiversity Research Programme.