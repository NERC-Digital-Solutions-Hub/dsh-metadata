# Details of Cleaned UK Rainfall Chemistry Data (1986 - 2011)

## Overview
- Subset of 20 UK sites with the longest continuous data record from 1986 to 2011, sourced from the UK-AIR database (Defra).
- Rainfall samples collected weekly or biweekly at each site and analyzed centrally.
- Raw data contained contamination issues and missing values; cleaning, gap-filling, and quality assurance were performed to produce usable datasets.

## Quality control and data processing
- Contamination and data quality rules applied:
  - Bird droppings and wind-blown dust samples removed; some samples may still remain if contamination is conservative.
  - Ion balance assessed; acceptable range: -10% to +20% (or -10% to +30% when total ion concentration < 200 µeq L^-1).
  - Contamination checks: phosphate > 10 µeq L^-1 (remove); ammonium > 100 µeq L^-1 (review); potassium > 8 µeq L^-1 (remove); calcium > 50 µeq L^-1 with Ca > Na (conservative removal).
- Missing data estimation:
  - Remaining gaps filled where possible using statistical interpolation across time and space with GENSTAT MULTMISSING.
  - Final datasets include both accepted measurements and estimated values, flagged accordingly.
- Data flags explain data status (see below).

## Data content and format
- Each site has a corresponding data file (Sitename.csv); rows represent rainfall samples defined by start and end dates.
- Columns include:
  - Ca2+, Cl-, H+, K+, Mg2+, NH4+, NO3-, Na+, PO4 3-, SO4 2-, non-sea SO4 2- (calculated from Na+ based on average sea-salt composition)
  - Conductance (µS cm^-1)
  - Precipitation depth (mm)
  - Flag (data status)
- Unit details:
  - Concentrations in microequivalents per litre (µeq L^-1)
  - Deposition (per sample) = concentration × rainfall depth → microequivalents per square metre (µeq m^-2)
  - Mass conversion requires multiplying deposition by the appropriate mass per equivalent (e.g., 16 for sulfur)
- Flag meanings:
  - 0 = no sample
  - 1 = contaminated and omitted (no correction possible)
  - 2 = rain sample volume but not analysed
  - 3 = missing data replaced by estimates
  - 4 = contaminated data replaced by estimates
  - -1 = raw data OK
- NA denotes no analysis; NA in precipitation_depth indicates no sample; separate rules for samples with no recorded rainfall volume.

## Site details and data access
- 20 UK sites with coordinates and UK-AIR IDs; site names include Allt a’Mharcaidh, Bannisdale, Barcombe Mills, Bottesford, Eskdalemuir, Flatford Mill, Goonhilly, High Muffles, Hillsborough, Loch Dee, Lough Navar, Preston Montfort, Pumlumon, Stoke Ferry, Strathvaich, Thorganby, Tycanol Wood, Wardlow Hay Cop, Whiteadder, Yarner Wood.
- Site data are stored in individual CSV files named after the site (e.g., Sitename.csv).

## Implications for monitoring frameworks
- Demonstrates rigorous QA/QC, transparent data provenance, and explicit handling of data gaps and contamination—key for long-term environmental monitoring analyses.
- Flags and imputation metadata facilitate traceability of data quality and decisions in framework assessments.
- Acknowledges practical barriers in data sharing and metadata completeness that can affect governance and openness.