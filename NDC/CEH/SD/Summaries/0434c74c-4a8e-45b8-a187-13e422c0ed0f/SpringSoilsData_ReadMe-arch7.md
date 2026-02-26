# ReadMe file for SpringSoilsData.csv

## Overview
- ReadMe for ancillary soil measurements accompanying greenhouse gas flux data from a field trial.
- Field trial investigates soils under control or sheep urine patches (artificial or real) in relation to GHG flux measurements.
- Data represent soil properties collected alongside GHG measurements.

## Study Site and Timeline
- Location: orthic podzol at Henfaes Research Station, Abergwyngregyn, North Wales.
- Elevation: 270 m above sea level; coordinates: 53°13'N, 4°0'W.
- Established in spring 2016.
- Time-series dataset spanning one year after treatment application (sampling dates provided in the data file).

## Treatments and Experimental Design
- Treatments: Control (no urine), ArtUrine (artificial urine), RealUrine (real sheep urine).
- Urine application rates: artificial urine 1066 kg N ha-1; real sheep urine 756 kg N ha-1.
- Experimental design: randomised block design with n = 4 per treatment.
- Sampling plots included urine patches near chambers used for GHG flux measurements.

## Sampling and Sample Handling
- Soil samples: n = 3 bulked samples per replicate plot (total replicates per treatment = 4).
- Depth: 0–10 cm.
- Sampling method: auger (1.3 cm diameter).
- Processing: samples refrigerated after collection and processed within 24 hours.
- Sampling frequency: time-series over the course of one year; specific dates included in the data file.

## Measurements and Analytical Methods
- Gravimetric soil moisture (Gravmoist): determined by oven-drying soil at 105 °C for 24 h.
- pH and EC: measured in 1:2.5 soil-to-distilled water slurries; electrodes calibrated with certified buffers.
- Extraction: 0.5 M K2SO4, 1:5 soil-to-solution ratio.
- Analytes (mg kg-1 soil dry weight or µS cm-1 as appropriate):
  - Nitrate (NO3--N)
  - Ammonium (NH4+-N)
  - Total dissolved nitrogen (TDN)
  - Dissolved organic carbon (DOC)
- Analytical methods:
  - Nitrate and ammonium: spectrophotometric methods (Miranda et al., 2001; Mulvaney, 1996) with matrix-matched 6-point calibration.
  - TDN and DOC: measured with Multi N/C 2100S analyser, using matrix-matched calibrations.

## Data Quality Assurance
- Procedures included analysis of procedural blanks, inspection of calibration curves, and re-analysis when necessary.
- Calibration curves checked for high precision; calculations visually checked and corrected for errors.

## Data Headers and Variable Definitions
- Plot: plot number and chamber number.
- Date: sampling date.
- Days_after: days before/after treatment application.
- Tmnt: treatment category (Control, ArtUrine, RealUrine).
- Gravmoist: gravimetric soil moisture (%) at sampling time (dry weight basis).
- pH: soil pH at sampling.
- EC: soil electrical conductivity (µS cm-1) at sampling.
- Nitrate: extractable nitrate (mg NO3--N kg-1 soil dw).
- Ammon: extractable ammonium (mg NH4+-N kg-1 soil dw).
- TDN: extractable total dissolved nitrogen (mg N kg-1 soil dw).
- DOC: extractable total dissolved organic carbon (mg C kg-1 soil dw).

## Provenance and Use
- Data derived from a field trial examining GHG emissions; supplementary soil measurements accompany flux data.
- Authors should be acknowledged if data are reused or reproduced.
- References for methods:
  - Miranda, K.M., Epsey, M.G., and Wink, D.A. (2001). Nitric Oxide, 5, 62-71.
  - Mulvaney, R.L. (1996). Methods of Soil Analysis, Part 3.