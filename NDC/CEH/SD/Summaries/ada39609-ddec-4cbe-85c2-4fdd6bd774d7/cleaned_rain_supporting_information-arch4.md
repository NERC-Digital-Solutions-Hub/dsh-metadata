# Details of Cleaned UK Rainfall Chemistry Data (1986 - 2011)

## Overview
- Source: UK rainfall chemistry data from the UK-AIR database, Defra-backed.
- Scope: Subset of 20 sites with the longest continuous records from 1986 to 2011.
- Sampling: Weekly or biweekly rainfall samples collected by bulk collectors and analyzed centrally.
- Quality concerns: Raw data include contaminated samples and missing values; data cleaned and quality-checked prior to release.

## Data quality rules and cleaning
- Ion balance rule:
  - Acceptable ion balance: -10% to +20%; if total ion concentration (Σcations + Σanions) < 200 µeq/L, the range extends to -10% to +30%.
- Contamination criteria:
  - Phosphate > 10 µeq/L: eliminated.
  - Ammonium > 100 µeq/L: examined; some removed.
  - Potassium > 8 µeq/L: eliminated.
  - Calcium > 50 µeq/L with Ca > Na: excluded as wind-blown dust contamination (conservative; some dust-contaminated samples may remain, typically from small-volume samples).
- Missing data: estimated using statistical interpolation across time and space with GENSTAT MULTMISSING after cleaning.
- Final datasets: contain accepted and estimated values, flagged accordingly.
- Data organization: dataset names correspond to site names in UK-AIR with associated spatial identifiers.

## Data content and format
- Each dataset row: one rainfall sample identified by start and end dates.
- Columns (ions and related data):
  - Calcium Ca2+, Chloride Cl-, Hydronium H+, Potassium K+, Magnesium Mg2+, Ammonium NH4+, Nitrate NO3-, Sodium Na+, Phosphate PO4 3-, Sulphate SO4 2-, non-sea SO4 2- (calculated from Na+ using average seawater composition)
  - Conductance
  - Precipitation depth
  - Flag (data status)
- Units: all ion concentrations in microequivalents per litre (µeq/L).
- Deposition conversion: deposition = ion concentration (µeq/L) × rainfall depth (mm) → deposition in µeq/m2.
- Equivalents concept: one mole × ionic charge; conversion to mass uses the mass per equivalent (e.g., 16 for sulphur).
- Data flags (example meanings):
  - 0 = no sample
  - 1 = contaminated and omitted (no correction possible)
  - 2 = rain sample volume but not analysed
  - 3 = missing data replaced by estimates
  - 4 = contaminated data replaced by estimates
  - -1 = raw data OK
- NA meanings:
  - NA for chemical species and conductance = no analysis
  - NA in precipitation_depth = no sample
  - NA in precipitation_depth = sample where rain volume not recorded

## Site list and data files
- 20 sites with coordinates and UK-AIR IDs, each with a corresponding data file:
  - Allt a’ Mharcaidh, UK-AIR ID UKA00086, AlltaMharcaidh.csv
  - Bannisdale, UK-AIR ID UKA00114, Bannisdale.csv
  - Barcombe Mills, UK-AIR ID UKA00069, BarcombeMills.csv
  - Bottesford, UK-AIR ID UKA00055, Bottesford.csv
  - Eskdalemuir, UK-AIR ID UKA00130, Eskdalemuir.csv
  - Flatford Mill, UK-AIR ID UKA00103, FlatfordMill.csv
  - Goonhilly, UK-AIR ID UKA00056, Goonhilly.csv
  - High Muffles, UK-AIR ID UKA00169, HighMuffles.csv
  - Hillsborough, UK-AIR ID UKA00293, Hillsborough.csv
  - Loch Dee, UK-AIR ID UKA00107, LochDee.csv
  - Lough Navar, UK-AIR ID UKA00166, LoughNavar.csv
  - Preston Montfort, UK-AIR ID UKA00110, PrestonMontfort.csv
  - Pumlumon, UK-AIR ID UKA00173, Pumlumon.csv
  - Stoke Ferry, UK-AIR ID UKA00317, StokeFerry.csv
  - Strathvaich, UK-AIR ID UKA00162, Strathvaich.csv
  - Thorganby, UK-AIR ID UKA00105, Thorganby.csv
  - Tycanol Wood, UK-AIR ID UKA00113, TycanolWood.csv
  - Wardlow Hay Cop, UK-AIR ID UKA00119, WardlowHayCop.csv
  - Whiteadder, UK-AIR ID UKA00123, Whiteadder.csv
  - Yarner Wood, UK-AIR ID UKA00168, YarnerWood.csv

## Implications for data governance and use (Data Leaders perspective)
- The dataset demonstrates rigorous data curation, with explicit quality filters and provenance through flags.
- Cleaned data enable reliable analyses of rainfall chemistry and deposition by conversion to deposition and, if needed, to mass units.
- Comprehensive metadata and site-level files support cross-site comparisons and system-wide data strategy.
- Awareness of residual contamination risk and imputed values is essential when interpreting long-term trends.
- Provides a model for managing dispersed data sources: quality rules, contamination checks, and transparent handling of missing data.