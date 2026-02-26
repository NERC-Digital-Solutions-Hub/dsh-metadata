# Ecosystem productivity data from wetland sites in the Pastaza-Marañón Basin, Amazonian Peru, 2018-2020

## Overview
- Datasets come from two forest census plots in the Pastaza-Marañón Basin, Peru: NYO-03 (peatland pole forest) and VEN-02 (palm swamp).
- Aim: estimate and compare litter and root production and decay over a complete annual cycle to understand carbon accumulation dynamics in peat; some data extend to additional sites for context; includes downcore palaeoecological information from peat cores.
- The collection comprises ten CSV files covering decomposition, coarse woody debris, litter traps, root ingrowth cores, dendrometer bands, palm heights, radiocarbon dating, Pb-210 dating, carbon and nitrogen concentrations, and pollen data.

## Datasets included
- CSAP_3.1_Decomposition_bags.csv: litter decomposition rates for different materials; installation depths, replication, and mass loss.
- CSAP_3.2_CWD.csv: coarse woody debris measurements along transects; palm frond material; mass and size classifications.
- CSAP_3.3_Littertraps.csv: 1x1 m traps raised above ground; monthly collections; mass components.
- CSAP_3.4_Root_ingrowth_cores.csv: eight replicates per plot; three-monthly root production estimates.
- CSAP_3.5_Dendrometer_bands.csv: dendrometer growth measurements on selected trees; quarterly censuses.
- CSAP_3.6_Palm_heights.csv: palm height measurements from two census dates using climbing protocol.
- CSAP_3.7_14C.csv: radiocarbon dates from peat cores for age-depth modeling.
- CSAP_3.8_210Pb.csv: lead-210/214Pb and Cs-137 activities for near-surface peat; age-depth modeling.
- CSAP_3.9_C_N.csv: total carbon and nitrogen concentrations in peat cores.
- CSAP_3.10_Pollen.csv: subfossil pollen counts from peat cores for vegetation history.

## Data collection and methods
- Plots: NYO-03 (peatland pole forest) and VEN-02 (palm swamp) in the Pastaza-Marañón Basin.
- Methods follow established protocols (e.g., RAINFOR) for litter, CWD, and tree growth measurements.
- Litterbags installed at various depths; mesh and materials varied by treatment; repeated retrievals planned.
- CWD transects sampled for newly fallen debris; palm fronds included.
- Littertraps deployed in ten subplots per plot; monthly collections for a year.
- Root ingrowth cores installed and sampled at three-month intervals; roots dried and weighed.
- Dendrometers installed on selected trees; growth tracked by notch separation; some data lost to disturbances.
- Palm heights measured on two occasions by climbing; canopy-height metrics recorded.
- Radiocarbon dating processed at NEIF/SUERC; Pb-210/214Pb and Cs-137 measured for peat dating.
- Carbon and nitrogen analyses conducted on dried peat samples; pollen analyses followed standard vegetation reconstruction protocols.

## Quality control
- Litter materials homogenized; eight replicates typical for decomposition bags.
- CWD data collected by experienced fieldworkers with standardized sheets; check for consistency.
- Littertraps: ten replicates per plot; mass components cross-checked.
- Root cores: eight replicates per plot.
- Dendrometer data cleaned to exclude disturbed/destroyed bands; standardized field sheets used.
- Palm height data quality: one VEN-02 census (2019) deemed unreliable and excluded; repeated in 2020.
- Laboratory QA/QC protocols applied for radiocarbon, Pb-210, and C/N analyses; blanks and standards used for calibration.

## Data structure and variables
- Files are UTF-8 encoded, comma-separated; variables in columns, samples in rows; NA indicates missing data.
- Common structure elements across datasets include site codes (NYO_03, VEN_02), dates, and coordinates where applicable.
- Example data fields include:
  - 3.1 Decomposition: site_code, litter_type, depth_cm, time_period, replicate, initial/end masses, percentage remaining, installation/collection dates, latitude/longitude.
  - 3.2 CWD: site_code, transect, collection_date, category/diameter class, mass measurements, subsample masses/volumes.
  - 3.3 Littertraps: site_code, subplot, collection_month, start/date, total leaves/woody/reproductive/misc masses.
  - 3.4 Root_ingrowth_cores: site_code, core_number, collection_month, dates, root_mass_g.
  - 3.5 Dendrometer_bands: site_code, tag_no, installation/notch date, initial_diameter_mm, growth_mm, census_date/no.
  - 3.6 Palm_heights: site_code, tag_no, census_no/date, height metrics.
  - 3.7 14C: project, allocation, sample_name, site, core_code, sample_top/base/mid cm, radiocarbon age, C content, d13C, etc.
  - 3.8 Pb-210: core_code, depth, density, Pb210/214Pb/Cs137 activities and uncertainties.
  - 3.9 C/N: site_name, core_code, depth, C_pct, N_pct.
  - 3.10 Pollen: core_code, depth, counts for pollen taxa; geographic location data in metadata.
- Units follow standard lab reporting (g, mm, cm, May be counts or concentrations); depth is in cm; dates in dd/mm/yyyy formats.

## Geographical coverage and context
- Geographic focus: Pastaza-Marañón Basin, Amazonian Peru.
- Core and pollen data include coordinates; pollen dataset notes lat/long range: approximately -4.07 to -5.88 degrees latitude and -73.27 to -74.83 degrees longitude.
- Data suitable for GIS layering of productivity, carbon stocks, and paleoecological context across peatland and palm swamp habitats.

## Provenance and usage notes
- Project funding: UKRI-NERC, grant NE/R000751/1; Principal Investigator: Ian Lawson.
- Data tailored for integration into map-based data products to compare productivity and carbon dynamics between peatland and palm swamp sites, with potential extension to other sites for comparative context.
- Suitable for GIS analyses of spatial patterns, time-series plotting, age-depth modeling, and paleoecological reconstructions in peatland ecosystems.