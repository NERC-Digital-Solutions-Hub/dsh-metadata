# BLEL_nutrient_profiles.csv

## Overview
- Dataset documenting nutrient concentrations in Blelham Tarn at the main buoy ( deepest point, 14.5 m) in 2016.
- Monthly profiles collected from June to October 2016.
- Analytes: soluble reactive phosphorus (SRP), nitrate, silica, total nitrogen (TN), total phosphorus (TP).
- SRP measured at every metre (1–13 m); Nitrate, Silica, TN, and TP at depths 1, 4, 7, 10, and 13 m.
- Analyses performed by Emma Gray and by the UK Centre for Ecology & Hydrology chemistry department (Lancaster).

## Data structure
- Columns: Date (dd/mm/yyyy), Depth (m), SRP (mg/L), Silica (mg/L), Total Nitrogen (mg/L), Total Phosphorus (mg/L).

## Sampling and provenance
- Collected by Emma Gray for NEC05744.
- Location: Blelham Tarn, Lake District, North West England (see Figure 1; buoy at 14.5 m depth).
- Bathymetry source: Ramsbottom (1976).

## Analytical procedures (key methods)
- Soluble Reactive Phosphorus (SRP):
  - Field filtration through 47 mm GF/C filter.
  - Colorimetric determination using ammonium molybdate and antimony potassium tartrate in acid medium to form antimony-phospho-molybdate complex; reduced to blue with ascorbic acid.
  - Read at 880 nm with spectrophotometer.
  - Calibration curve created from standard SRP concentrations (50 µg/L) plus diluted samples; inclusion of a dedicated quality control solution (AQC) at 50 µg/L diluted to 10 µg/L.
- Total Phosphorus (TP):
  - Digestion with potassium persulphate (K2S2O8) and sulfuric acid, followed by colorimetric molybdenum blue analysis.
  - Unfiltered water digested; measurement via SEAL AQ2 analyser.
  - Calibration prepared and corrected by blank means.
- Total Nitrogen (TN):
  - Acidification with HCl, purging to remove inorganic carbon, then measurement with Shimadzu Shalar Formacs CA16 analyser (ND25 for TN).
- Nitrate:
  - Ion chromatography; samples filtered through Whatman 0.45 µm cellulose acetate filters and run on a Dionex ICS2100 IC system.
  - Precision and reproducibility checked with QC samples at 10 sample intervals.
- Silica:
  - Colorimetric method using ammonium molybdate, reduced with ascorbic acid to form silicomolybdenum blue.
  - Color read at 880 nm; background corrections applied.

## Temporal and depth coverage
- Sampling period: June–October 2016 (monthly).
- Depths:
  - SRP: 1 m through 13 m (every metre).
  - Nitrate, Silica, TN, TP: 1 m, 4 m, 7 m, 10 m, and 13 m.

## Documentation and metadata
- File: BLEL_nutrient_profiles.csv.
- Metadata and methodology documented to support reproducibility and reuse.
- Figure 1 (not included here) shows lake location and buoy position relative to bathymetry.

## Quality assurance and provenance notes
- Calibration curves used with multiple standards; inclusion of QA/QC solutions in SRP protocol.
- Cross-checks and instrument calibration implied through standard curves and QC samples for each measurement type.
- Provenance: data collected by Emma Gray; analyses performed by Emma Gray and UK CEH chemistry department (Lancaster).

## Usage considerations and limitations
- Data limited to 2016 and to the Blelham Tarn site; temporal and spatial scope may affect comparability with other lakes or years.
- Some analytes have limited depth sampling (Nitrate, Silica, TN, TP only at specific depths).
- Units: mg/L for all nutrient measurements; Date format and depth units specified for consistency.

## References
- Ramsbottom, A. (1976) Depth charts of the Cumbrian lakes, Freshwater Biological Association. Kendal.