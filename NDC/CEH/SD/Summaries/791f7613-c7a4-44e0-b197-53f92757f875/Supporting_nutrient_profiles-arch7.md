# Supporting information

## Overview
- Dataset BLEL_nutrient_profiles.csv contains nutrient concentrations (mg/L) measured at the main buoy of Blelham Tarn (deepest point ~14.5 m) during June–October 2016.
- Parameters: Soluble Reactive Phosphorus (SRP), Silica, Total Nitrogen (TN), Total Phosphorus (TP), plus nitrate data referenced but not listed as a separate column in the data structure.
- SRP sampled at every metre from 1 m to 13 m; nitrate, silica, TN, and TP sampled at depths 1 m, 4 m, 7 m, 10 m, and 13 m.

## Data content and structure
- Data file: BLEL_nutrient_profiles.csv
- Columns: Date (dd/mm/yyyy), Depth (m), SRP (mg/L), Silica (mg/L), Total Nitrogen (mg/L), Total Phosphorus (mg/L)

## Spatial context
- Location: Blelham Tarn, Lake District, UK.
- Monitoring buoy positioned at the lake’s deepest point (14.5 m).
- Figure 1 (referenced) shows buoy location and bathymetry from Ramsbottom (1976).

## Temporal scope
- Sampling frequency: Monthly from June to October 2016.

## Analytical procedures and quality assurance
- Soluble Reactive Phosphorus (SRP): Field-filtered samples; colorimetric determination using ammonium molybdate and antimony potassium tartrate in acid, with ascorbic acid reduction; absorbance read at 880 nm. Calibrated with a standard curve (50 µg/L to 100 µg/L) and a quality control solution (AQC) at 50 µg/L diluted to 10 µg/L.
- Total Phosphorus (TP): Potassium persulfate digestion followed by molybdenum blue colorimetric analysis; calibration with standards; blanks corrected.
- Total Nitrogen (TN): Samples acidified with HCl, purged to remove inorganic carbon, measured with Shalar Formacs CA16 (ND25).
- Nitrate: Determined by ion chromatography; samples filtered (Whatman 0.45 µm) prior to analysis; QC included at 10 sample intervals.
- Silica: Colorimetric method using ammonium molybdate and ascorbic acid; blue complex measured at 880 nm; background corrected via blanks.

## Data provenance
- Collected by Emma Gray for project NEC05744.
- Some analyses performed by the UK Centre for Ecology & Hydrology chemistry department (Lancaster).

## Practical notes for GIS use
- Suitable for constructing vertical nutrient profiles and time-series visualizations at a fixed buoy location.
- Data are point-in-time measurements at discrete depths; spatial dimension is the buoy location, with depth as the vertical axis.
- Can support map-based visualizations of nutrient gradients over time, and cross-dataset integration with bathymetry or lake-wide layers.
- Consider aligning to a GIS-ready schema: Date, Depth, SRP, Silica, TN, TP, with buoy geometry and lake frame of reference.

## Limitations and references
- Temporal coverage limited to June–October 2016; does not include other years or seasons.
- Depth sampling patterns differ by parameter (SRP at every metre 1–13 m; others at 1, 4, 7, 10, 13 m).
- Location and bathymetric context drawn from Ramsbottom (1976).