# Details of Cleaned UK Rainfall Chemistry Data (1986 - 2011)

## Overview
- Source: UK-AIR database operated on behalf of Defra.
- Scope: Subset of 20 sites with the longest continuous data record from 1986 to 2011.
- Sampling: Weekly or biweekly rainfall samples across the UK, analyzed at a central laboratory.
- Issues addressed: Contamination (bird droppings, wind-blown dust) and missing samples; raw data cleaned and quality-assessed.
- Data products: Final datasets containing accepted and estimated values, flagged for quality.
- Units and use: Ion concentrations are in microequivalents per litre (µeq L⁻¹). Deposition can be derived by multiplying concentration by rainfall depth (mm) to yield deposition in microequivalents per square metre (µeq m⁻²). Conversions to mass require multiplying equivalents by the substance’s mass per equivalent.

## Data structure and contents
- Data per site: Each site has a separate dataset named Sitename.csv.
- Columns (1–16):
  1. sample start date (dd/mm/yyyy)
  2. sample end date
  3. Ca²⁺ (µeq L⁻¹)
  4. Cl⁻ (µeq L⁻¹)
  5. H⁺ (µeq L⁻¹)
  6. K⁺ (µeq L⁻¹)
  7. Mg²⁺ (µeq L⁻¹)
  8. NH₄⁺ (µeq L⁻¹)
  9. NO₃⁻ (µeq L⁻¹)
  10. Na⁺ (µeq L⁻¹)
  11. PO₄³⁻ (µeq L⁻¹)
  12. SO₄²⁻ (µeq L⁻¹)
  13. non-sea SO₄²⁻ (µeq L⁻¹) – calculated from Na⁺ using average sea-salt composition
  14. conductance (µS cm⁻¹)
  15. precipitation depth (mm)
  16. flag (data quality indicator)
- Data characteristics:
  - All ion concentration data are in µeq L⁻¹.
  - A sample’s deposition can be calculated by multiplying each ion concentration by the associated precipitation depth (mm).

## Data cleaning and quality control
- Ion balance: Calculated as (Σcations − Σanions) / (Σcations + Σanions).
  - Acceptable when ion balance is between −10% and +20%; if total ion concentration < 200 µeq L⁻¹, the range extends to −10% to +30%.
- Evidence of contamination:
  - Exclude samples with phosphate > 10 µeq L⁻¹.
  - Examine samples with NH₄⁺ > 100 µeq L⁻¹; exclude if flagged.
  - Exclude samples with K⁺ > 8 µeq L⁻¹.
  - Exclude samples with Ca²⁺ > 50 µeq L⁻¹ and Ca²⁺ > Na⁺ (wind-blown dust indicator). Some dust-contaminated samples may remain if they had very low rain volumes.
- Missing data:
  - After cleaning, missing values are estimated using spatial and temporal statistical interpolation with GENSTAT MULTMISSING.
- Output:
  - Final datasets include both accepted and estimated values, with appropriate flags to indicate estimated values.

## Geospatial and site metadata
- Site list includes 20 UK sites with:
  - Site name
  - Latitude and longitude
  - UK-AIR ID (e.g., UKA00086)
  - Data file name (e.g., AlltaMharcaidh.csv)
- Spatial identifiers allow mapping and integration with GIS workflows.

## Using the data in GIS (map-based data products)
- Data can be joined to GIS layers using site identifiers or coordinates.
- Deposition mapping:
  - Convert ion concentrations to deposition by multiplying by corresponding rainfall depth per sample.
  - Resulting deposition units: µeq m⁻² per sampling period.
- Data quality and interpretation:
  - Use the flag column to filter samples (0 = raw OK; 1 = contaminated and omitted; 2 = volume but not analysed; 3/4 = missing or contaminated data replaced by estimates; -1 = raw data OK).
  - Non-sea sulfate is provided as a calculated value to account for sea-salt contributions.

## Access and data files
- Data are stored as separate CSV files per site (Sitename.csv) within the UK-AIR dataset.
- The full site list (20 sites) includes site names, coordinates, UK-AIR IDs, and corresponding data file names for GIS-ready referencing.