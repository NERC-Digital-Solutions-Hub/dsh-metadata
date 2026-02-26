# CEH-GEAR1hr.v2

## Overview
- Updated 1-km, hourly rainfall dataset for Great Britain (GB) from 1990 onwards, extending CEH-GEAR1hr with more raingauges (2,606 vs 1,903 previously) and extended temporal coverage to 2016.
- Derived by temporal disaggregation of CEH-GEAR daily data using hourly gauge data; aims to preserve daily totals while reflecting hourly storm shapes.
- Nearest-neighbour interpolation without height correction to maintain real storm shapes; hourly estimates refer to rainfall accumulated in the previous hour.
- Intended for hydrological modelling and related analyses; users should account for statistical disaggregation and interpolation approaches when interpreting results.

## Data access and citation
- Data available from Environmental Information Data Centre (EIDC): https://doi.org/10.5285/fc9423d6-3d54467f-bb2b-fc7357a3941f
- Please cite:
  - Lewis et al. (2020) CEH-GEAR1hr.v2 data record
  - Lewis et al. (2018) A rule based quality control method for hourly rainfall data
  - Additional project and data provenance references listed in the document

## Brief description of the dataset
- CEH-GEAR1hr.v2 provides 1-km gridded hourly rainfall estimates for GB from 1990 to 2016 (with ongoing extension).
- Methodology unchanged from v1: daily CEH-GEAR rainfall disaggregated to hourly values using a nearest-neighbour approach and a larger set of gauges.
- Hourly rainfall values represent the rainfall accumulated in the previous hour.
- Metadata indicate whether a grid cell used statistical disaggregation (Table 1 storm shapes) and the minimum distance to the gauge used for each grid cell.

## Data sources
- 2,606 UK rain gauges from:
  - UK Met Office MIDAS: 382 gauges
  - England Environment Agency (EA) WISKI: 1,622 gauges
  - Natural Resources Wales (NRW) WISKI: 257 gauges
  - Scottish Environmental Protection Agency (SEPA) WISKI: 345 gauges
- CEH-GEAR daily dataset (Keller et al., 2015; Tanguy et al., 2019)
- Quality control procedure applied to hourly gauge data (Lewis et al., 2018)

## Method for deriving the hourly grids
- Daily records selected to ensure completeness for each day; number of gauges used per day ranges 430–1,771.
- For each hour, rainfall is interpolated to a 1-km grid by nearest-neighbour using the hourly gauge value as a fraction of the station’s daily total.
- If the nearest gauge is >50 km away, or if rainfall exists in the daily total but not in the hourly gauge, a statistical disaggregation using average storm shapes is used.
- Statistical disaggregation is documented (Table 1 shows average hourly rainfall for different daily totals and seasons).
- The daily totals are preserved from CEH-GEAR daily data while hourly shapes reflect the observed storm profile.

## Minimum distance grids
- Each grid point has a minimum distance to the closest gauge used for that day (Min_dist).
- Mean distance: ~2.6 km; maximum distance: 100 km (west coast of Scotland).
- A 50 km minimum-distance threshold was used to exclude grids where gauge representativeness would be too low.

## Statistical disaggregation grids
- Disaggregation used when a grid cell is >50 km from a gauge or when there is rainfall in the daily total but not in the hourly data.
- Percentages:
  - Zero rainfall hourly disaggregation: up to 0–26% of grid squares on any day
  - Distance-based disaggregation (>50 km): 0–11% of grid squares over 1990–2016
- Post-2000 reductions in rare disaggregation cases as EA network denseens.
- 97% of zero-rain hourly disaggregations occur for daily totals <1 mm.
- Disaggregation implications: may affect diurnal analysis and extreme-value interpretation; metadata should be consulted.

## Quality control (QC)
- QC process to identify and reject erroneous hourly values (three-step):
  - Step 1: Compare gauge data to CEH-GEAR daily dataset to flag suspect gauges.
  - Step 2: Apply a set of QC tests (Table 2) to all gauges; mark suspect hourly/daily values with QC flags.
  - Step 3: Apply rule-based decisions (Table 3) to determine which flagged values are erroneous and should be removed (replaced with -999).
- QC flags cover a wide range of issues (threshold exceedances, rapid dry/wet spells, monthly/monthly accumulation anomalies, neighborhood checks, etc.).
- Rule-base decisions (R1–R20) describe how combinations of QC flags lead to data removal or treatment (e.g., large hourly values, accumulation issues, suspected large-scale gauge problems, and manual identifications).
- Model performance metrics used: Spearman rs > 0.8 and P00+P11 > 0.8 for gauges/gridded cells to be retained after QC.
- Table 4 indicates total time steps rejected by QC (highly stringent cleaning in v2 vs v1).

## Use and caveats
- Designed for hydrological modelling; appropriate use depends on analysis type.
- Diurnal cycles are affected by statistical disaggregation (and by the fixed hourly storm shapes); trend analyses of hourly rainfall may be biased.
- Nearest-neighbour interpolation can yield “blocky” spatial patterns; spatial analyses should consider this limitation.
- Users should inspect metadata (Stat_disag and Min_dist) when conducting analyses.

## Format and structure
- Data stored in NetCDF4 format following CEH conventions.
- Monthly files (e.g., CEH-GEAR-1hr.v2_199001 for January 1990).
- Variables per file:
  - Rainfall_amount: hourly rainfall in kg/m2 (mm)
  - Stat_disag: 1 if statistical disaggregation used for that day, 0 otherwise
  - Min_dist: minimum distance to the closest hourly gauge used (m)
- Global attributes include time_coverage_resolution (P1H) and time_coverage_duration (e.g., P27Y).

## Acknowledgements and references
- Funded by SINATRA (NERC Flooding from Intense Rainfall) and CONVEX (NERC Changing Water Cycle) among others.
- Data acquisition and publishing supported by Hydro-JULES and partner hydrometric teams (EA, SEPA, NRW, Met Office).
- Key references:
  - Keller et al. 2015; Lewis et al. 2018; Lewis et al. 2020
  - MIDAS Open and related datasets
  - Tanguy et al. 2019; Wilks 2006; Yoo & Ha 2007

## Implications for monitoring frameworks
- Provides a high-resolution, openly cited rainfall data source suitable for policy evaluation and environmental health monitoring with explicit metadata and QC.
- Emphasizes data provenance, quality assurance, and governance needs (metadata completeness, data sharing, reproducibility).
- Highlights practical considerations for data integration, including handling of data gaps, homogenization across agencies, and transparent documentation of disaggregation effects.