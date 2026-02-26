# ReadMe file for SpringSoilsData.csv

## Overview
- Dataset derived from a field trial assessing greenhouse gas emissions from sheep urine patches on semi-improved upland grassland.
- Ancillary soil measurements accompany greenhouse gas flux data.
- Documents authorship acknowledgment requirements for data reuse.

## Study site and design
- Location: orthic podzol at Henfaes Research Station, Abergwyngregyn, North Wales (270 m a.s.l.; 53°13'N, 4°0'W).
- Established: spring 2016.
- Plot setup: randomised block design with four replicate plots per treatment.
- Treatments: Control (no urine), ArtUrine (artificial urine), RealUrine (real sheep urine).
- Urine application rates: artificial urine 1066 kg N ha-1; real sheep urine 756 kg N ha-1.
- Sampling context: soil samples taken from control or urine patches near chambers used for GHG measurements; patches were near flux chambers.

## Data collection and sampling
- Timeframe: data collected over one year following treatment application; sampling dates provided in the data file.
- Soil depth: 0–10 cm.
- Sampling: three bulked samples per replicate plot (n = 4 per treatment).
- Sample handling: soils refrigerated after collection; processed within 24 hours.
- Soil moisture: gravimetric moisture determined by drying in an oven (105 °C, 24 h).
- pH and EC: measured in 1:2.5 soil-to-distilled water slurries with standard electrodes; electrodes calibrated prior to each measurement occasion.

## Analytical methods
- Extraction: 0.5 M K2SO4 (1:5 soil-to-solution) for estimation of extractable nutrients.
- Analytes:
  - Nitrate (NO3--N)
  - Ammonium (NH4+-N)
  - Total dissolved nitrogen (TDN)
  - Dissolved organic carbon (DOC)
- Measurement specifics:
  - Nitrate: spectrophotometric method (Miranda et al., 2001).
  - Ammonium: spectrophotometric method (Mulvaney, 1996).
  - TDN and DOC: measured with Multi N/C 2100S analyzer (AnalytikJena) using matrix-matched calibration curves.
- Calibration: matrix-matched 6-point calibration curves using serial dilutions of certified stock standards.
- Quality assurance: analysis included procedural blanks, calibration curve inspection, re-analysis if needed, and visual data checks.

## Data structure and variables
- Key headers:
  - Plot: plot and chamber identifiers.
  - Date: sampling date.
  - Days_after: days before/after treatment.
  - Tmnt: Treatment (Control, ArtUrine, RealUrine).
  - Gravmoist: gravimetric soil moisture (% dry weight) at sampling.
  - pH: soil pH at sampling.
  - EC: soil EC at sampling (µS cm-1).
  - Nitrate: extractable nitrate (mg NO3--N kg-1 soil dry weight).
  - Ammon: extractable ammonium (mg NH4+-N kg-1 soil dry weight).
  - TDN: extractable total dissolved nitrogen (mg N kg-1 soil dry weight).
  - DOC: extractable total dissolved organic carbon (mg C kg-1 soil dry weight).

## Data quality and usage notes
- Data were subjected to QA procedures including blanks, calibration checks, and possible re-analysis to ensure accuracy.
- Authors must be acknowledged if the data are reused or reproduced.

## References
- Miranda, K.M., Epsey, M.G., and Wink, D.A. (2001). A rapid, simple, spectrophotometric method for simultaneous detection of nitrate and nitrite. Nitric Oxide 5, 62-71.
- Mulvaney, R.L. (1996). Nitrogen - inorganic forms. In Sparks, D.L. (Ed.), Methods of Soil Analysis. Part 3. SSSA Inc. pp. 1123-1184.