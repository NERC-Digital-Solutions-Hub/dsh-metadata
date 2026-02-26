# ReadMe file for SpringSoilsData.csv

## Overview
- Field trial dataset on greenhouse gas emissions from sheep urine patches applied to semi-improved upland grassland.
- Ancillary soil measurements accompanying the GHG flux data.
- Established spring 2016 at Henfaes Research Station, North Wales (orthic podzol; 270 m a.s.l.; 53°13'N, 4°0'W).
- Sampling depth: 0–10 cm; soil samples from control and replicated urine patches (artificial or real) near GHG chambers.
- Timeframe: one-year time-series following treatment.

## Experimental design
- Plot design: randomised block with 4 replicates per treatment.
- Treatments: Control (no urine), ArtUrine (artificial urine), RealUrine (real sheep urine).
- Urine application rates: artificial urine at 1066 kg N ha-1; real sheep urine at 756 kg N ha-1.
- Samples collected per plot: 3 bulked samples (n = 3 per replicate plot; total n = 4 per treatment).

## Measurements and methods
- Soil properties measured:
  - Gravimetric soil moisture (Gravmoist; % dry weight)
  - pH (1:2.5 soil-to-water slurry)
  - Electrical conductivity (EC; µS cm-1)
  - Nitrate (NO3--N; mg NO3--N kg-1 soil dry weight)
  - Ammonium (NH4+-N; mg NH4+-N kg-1 soil dry weight)
  - Total dissolved nitrogen (TDN; mg N kg-1 soil dry weight)
  - Dissolved organic carbon (DOC; mg C kg-1 soil dry weight)
- Extraction and analysis:
  - 0.5 M K2SO4 extractant (1:5 soil-to-solution) for NO3--N, NH4+-N, TDN, DOC.
  - NO3--N and NH4+-N analyzed by spectrophotometry; calibration with matrix-matched 6-point curves.
  - TDN and DOC analyzed with Multi N/C 2100S (matrix-matched 6-point curves).
  - pH and EC measured on standard electrodes with calibrated buffers.
- QA and QA/QC:
  - Procedural blanks analyzed; calibration curves visually inspected.
  - Re-analysis of samples where necessary; corrections for detected errors.
  - High-precision calibration curves ensured before analyses.
  - Data checked for errors and corrected as needed.

## Data structure and headers
- Data headers included:
  - Plot: plot and chamber identifier
  - Date: sampling date
  - Days_after: days since treatment
  - Tmnt: treatment (Control, ArtUrine, RealUrine)
  - Gravmoist: gravimetric soil moisture content (% dry weight)
  - pH: soil pH at sampling
  - EC: soil EC (µS cm-1)
  - Nitrate: 0.5M K2SO4 extractable NO3--N (mg NO3--N kg-1 soil dry weight)
  - Ammon: 0.5M K2SO4 extractable NH4+-N (mg NH4+-N kg-1 soil dry weight)
  - TDN: 0.5M K2SO4 extractable total dissolved nitrogen (mg N kg-1 soil dry weight)
  - DOC: 0.5M K2SO4 extractable total dissolved organic carbon (mg C kg-1 soil dry weight)

## Data provenance and usage notes
- Data derived from field measurements linked to a greenhouse gas flux study; the included soil measurements provide context for soil chemical status over time after urine treatments.
- Attribution: Authors must be acknowledged if data are reused or reproduced.
- Location and sampling details are provided to support replication and meta-analysis.

## Timeline and data scope
- Sampling conducted over a one-year period following treatment application.
- Data include a time-series dimension via the Days_after variable and multiple sampling dates.

## References for methods
- Miranda, K.M., Epsey, M.G., and Wink, D.A. (2001). A rapid, simple, spectrophotometric method for simultaneous detection of nitrate and nitrite. Nitric Oxide 5, 62-71.
- Mulvaney, R.L. (1996). Nitrogen - inorganic forms. In Sparks, D.L. (Ed.), Methods of Soil Analysis. Part 3. SSSA Inc., pp. 1123-1184.