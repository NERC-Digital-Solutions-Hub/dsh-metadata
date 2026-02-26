# Supporting information

- This file describes the BLEL_nutrient_profiles.csv dataset collected for the NEC05744 project.
- Collected by Emma Gray; focuses on nutrient concentrations in Blelham Tarn.

## Data scope and collection

- Location: Blelham Tarn, Lake District, with monitoring buoy at the deepest point (14.5 m).
- Depths sampled: SRP at every metre from 1 m to 13 m; Nitrate, Silica, Total Nitrogen, and Total Phosphorus at 1 m, 4 m, 7 m, 10 m, and 13 m.
- Time period: Monthly sampling from June to October 2016.
- Analytes: Soluble Reactive Phosphorus (SRP), Nitrate, Silica, Total Nitrogen (TN), Total Phosphorus (TP).
- Data file: BLEL_nutrient_profiles.csv.

## Variables and data structure

- Columns: Date (dd/mm/yyyy), Depth (m), SRP (mg/L), Silica (mg/L), Total Nitrogen (mg/L), Total Phosphorus (mg/L).
- Depth range: 1–13 m (1 m is near-surface; 13 m is deepest in the dataset).

## Sampling and laboratory procedures

- SRP:
  - Field filtration through a 47 mm GF/C filter.
  - Colourimetric determination using ammonium molybdate and antimony potassium tartrate in acid; blue complex read at 880 nm.
  - Calibration with standards (50 µg/L), prepared and diluted to 10–100 µg/L; QC solution (AQC) at 50 µg/L diluted to 10 µg/L for quality control.
- Total Phosphorus (TP):
  - Potassium persulphate digestion with colourimetric molybdenum blue method.
  - Unfiltered water digested; measurement with SEAL AQ2 analyser; calibration against a curve with blanks subtracted.
- Total Nitrogen (TN):
  - Acidification with HCl, purge to remove inorganic carbon, measurement with Shalar Formacs CA16 (ND25 attachment).
- Nitrate:
  - Filtration through Whatman 0.45 µm cellulose acetate filters; ion chromatography (Dionex ICS2100).
- Silica:
  - Colourimetric method with ammonium molybdate; reduced with ascorbic acid to form silicomolybenum blue.
  - Measured at 880 nm; blanks used to correct background colour.
- Quality control:
  - Calibration curves and QC procedures described for SRP; use of blanks for background corrections; periodic QC samples for precision and reproducibility.

## Provenance and metadata

- Data provenance: Analytical procedures and instrument details provided; SRP analyses performed by Emma Gray; other nutrients analysed by the UK Centre for Ecology & Hydrology chemistry department (Lancaster).
- Metadata emphasis: Sampling depths, date format, units (mg/L), and depth integration (1–13 m for SRP; discrete depths for other nutrients).

## Location context

- Figure 1: Location map of Blelham Tarn with buoy at the deepest point (14.5 m); bathymetry source Ramsbottom (1976).

## Reference

- Ramsbottom, A. (1976) Depth charts of the Cumbrian lakes, Freshwater Biological Association, Kendal.

## Implications for data leadership and reuse

- Strengths for data strategy:
  - Clear data structure with explicit depth sampling scheme and measurement depths.
  - Comprehensive documentation of analytical methods and QC procedures per nutrient parameter.
  - Provenance traceability: named collectors and collaborating lab (CEH Lancaster).
  - Metadata includes date, depth, units, and site-specific context (lake, buoy depth).
- Considerations for data integration and scale:
  - Temporal coverage limited to June–October 2016; may affect long-term trend analyses.
  - Spatial coverage is single-site (one buoy) at one lake; consider combining with other sites for broader comparisons.
  - Data quality relies on calibration, QC, and blanks; ensure reproducibility when integrating with other datasets.
- Potential data gaps or limitations:
  - Granularity varies by parameter (SRP at every metre vs. other nutrients at select depths).
  - Availability of full metadata beyond what’s in this file (e.g., exact QC results, instrument maintenance logs) could enhance reliability for cross-study comparisons.