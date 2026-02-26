# Details of Cleaned UK Rainfall Chemistry Data (1986 - 2011)

## Overview
- Rainfall chemistry data from the UK-AIR database (Defra) for 1986–2011.
- Subset comprises 20 sites with the longest continuous records.
- Samples collected weekly or biweekly; analyzed centrally.
- Data cleaned for quality; concentrations in microequivalents per litre (µeq L-1); deposition can be computed by multiplying by rainfall depth (mm).
- Final datasets include accepted data and estimated values, flagged to indicate processing.

## Data Content and Format
- Each site has a separate dataset named Sitename.csv; site metadata included (latitude, longitude, UK-AIR id).
- Columns (per site dataset):
  1. sample start date
  2. sample end date
  3. Ca2+ (µeq L-1)
  4. Cl− (µeq L-1)
  5. H+ (µeq L-1)
  6. K+ (µeq L-1)
  7. Mg2+ (µeq L-1)
  8. NH4+ (µeq L-1)
  9. NO3− (µeq L-1)
  10. Na+ (µeq L-1)
  11. PO4 3− (µeq L-1)
  12. SO4 2− (µeq L-1)
  13. non-sea SO4 2− (µeq L-1, calculated from Na+ based on average sea-salt composition)
  14. conductance (µS cm−1)
  15. precipitation depth (mm)
  16. flag (data quality status)
- Data quality flags:
  - 0: no sample; 1: contaminated and omitted (no correction); 2: sample volume but not analysed; 3: missing data replaced by estimates; 4: contaminated data replaced by estimates; -1: raw data OK
- Special notes:
  - Concentrations are in µeq L−1; deposition in µeq m−2 is obtained by multiplying by precipitation depth.
  - “NA” indicates no analysis for chemical species/conductance; “NA” in precipitation_depth indicates no sample due to no rain.

## Quality Assurance and Cleaning
- Contamination and data quality rules:
  - Ion balance: (Σcations − Σanions) / (Σcations + Σanions) used to assess data quality; acceptable ranges: −10% to +20%, extended to −10% to +30% when total ion concentration < 200 µeq L−1.
  - Evidence of contamination: remove samples with phosphate > 10 µeq L−1; ammonium > 100 µeq L−1; potassium > 8 µeq L−1; calcium > 50 µeq L−1 with Ca > Na (wind-blown dust indicator). Some dust-contaminated samples may remain if they have very low volume.
- After cleaning, missing data are estimated using time- and space-based interpolation with GENSTAT MULTMISSING.
- Final datasets contain both accepted (raw/adjusted) and estimated values, with appropriate flags.
- Data files correspond to site datasets listed in the UK-AIR directory, with site-specific data and metadata.

## Data Details and Units
- All chemical species concentrations are in µeq L−1; deposition is calculated by multiplying by the site’s rainfall depth (mm).
- Non-sea sulfate is derived from Na+ using average sea-salt composition.
- Equivalents concept: 1 mole of a species multiplied by its ionic charge (e.g., SO4 2− = 1 mole yields 2 equivalents).

## Site Metadata and Access
- 20 sites included, with each site file named as Sitename.csv.
- Examples of site metadata provided:
  - Allt a’Mharcaidh, Bannisdale, Barcombe Mills, Bottesford, Eskdalemuir, Flatford Mill, Goonhilly, High Muffles, Hillsborough, Loch Dee, Lough Navar, Preston Montfort, Pumlumon, Stoke Ferry, Strathvaich, Thorganby, Tycanol Wood, Wardlow Hay Cop, Whiteadder, Yarner Wood.
- Each site record includes:
  - Latitude and longitude
  - UK-AIR id (e.g., UKA00086)
  - Data file name (e.g., AlltaMharcaidh.csv)

## Usage Notes and Considerations
- Data are best used with the flag column to filter for quality-controlled samples.
- Some samples are replaced by estimates; interpret accordingly.
- Potential remaining limitations from contamination in low-volume samples.
- Useful for long-term analysis of wet chemical deposition and cross-site comparisons when combined with precipitation data.

## Data Support Implications
- Example use cases for data support:
  - Build self-serve dashboards showing temporal deposition trends by site and ion.
  - Create comparative visuals across sites (spatial and temporal patterns).
  - Integrate with other UK-AIR datasets to analyze atmospheric deposition contexts.
  - Document and share data cleaning steps (ion balance checks, contamination rule filters, imputation) to improve reproducibility.