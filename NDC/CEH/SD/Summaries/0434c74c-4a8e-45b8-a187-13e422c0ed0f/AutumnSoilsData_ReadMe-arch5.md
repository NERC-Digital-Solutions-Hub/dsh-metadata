# Authors must be acknowledged if data are re-used or reproduced. The data is derived from a field trial investigating greenhouse gas emissions from sheep urine patches deposited to a semi-improved upland grassland, and represents the ancillary soil measurements made alongside the greenhouse gas flux measurements.

## Overview and provenance
- Field trial site: orthic podzol at Henfaes Research Station, Abergwyngregyn, North Wales (270 m.a.s.l.; 53°13'N, 4°0'W); established autumn 2016.
- Purpose: ancillary soil measurements accompanying greenhouse gas flux measurements from sheep urine patches (control, artificial urine, real sheep urine).
- Data type: soil chemical and moisture measurements collected alongside gas flux data.

## Experimental design and treatments
- Design: randomised block with four replicate plots (n = 4 per treatment).
- Treatments (n = 3 per patch type): 
  - Control: no urine application
  - ArtUrine: artificial urine (1004 kg N ha-1)
  - RealUrine: real sheep urine (1112 kg N ha-1)
- Sampling context: patches located near gas flux chambers.

## Sampling details and depth
- Soil depth: 0–10 cm.
- Sub-sampling: 3 bulked samples per replicate plot (n = 4).
- Sampling method: 1.3 cm diameter auger.
- Sampling frequency: time-series over one year following treatment.

## Storage, handling, and processing
- Post-collection: soil samples refrigerated; processed within 24 hours.
- QA for storage/processing: standard procedures applied at collection and processing.

## Measurements and analytical methods
- Gravimetric soil moisture: drying in crucibles (105 °C, 24 h), expressed as % dry weight.
- pH and electrical conductivity (EC): measured in 1:2.5 soil-to-distilled water slurries; electrodes calibrated with reference buffers before each measurement.
- Analytes in 0.5 M K2SO4 extract (1:5 soil:solution):
  - Nitrate (NO3–-N) and ammonium (NH4+-N): analyzed spectrophotometrically using Miranda et al. (2001) and Mulvaney (1996) methods, respectively.
  - Total dissolved nitrogen (TDN) and dissolved organic carbon (DOC): quantified with a Multi N/C 2100S analyser.
  - Calibration: matrix-matched 6-point curves with certified reference standards; blanks analyzed.
- Data quality assurance: inclusion of procedural blanks, assessment of calibration curves, data re-analysis if needed, and visual checks/corrections of calculations.

## Data structure and headers
- Key data columns:
  - Plot: plot and chamber identifiers
  - Date: sampling date (dd/mm/yy)
  - Days_after: days before/after treatment
  - Tmnt: treatment category (Control, ArtUrine, RealUrine)
  - Gravmoist: gravimetric soil moisture (% dry weight)
  - pH: soil pH at sampling
  - EC: soil EC (µS cm-1)
  - Nitrate: 0.5 M K2SO4-extractable nitrate (mg NO3–-N kg-1 soil dry weight)
  - Ammon: 0.5 M K2SO4-extractable ammonium (mg NH4+-N kg-1 soil dry weight)
  - TDN: 0.5 M K2SO4-extractable total dissolved nitrogen (mg N kg-1 soil dry weight)
  - DOC: 0.5 M K2SO4-extractable dissolved organic carbon (mg C kg-1 soil dry weight)
- Note: zero values indicate concentrations below detection limits.

## Data quality, limitations, and governance notes
- Data quality assurance steps documented (blanks, calibration curve checks, re-analysis if needed).
- Metadata includes sampling times, treatments, and measurement methods to support reproducibility and reuse.
- Considerations for data users: ensure acknowledgment of data authors when reusing; understand that some values may be below detection limits (zero values).

## References for methods
- Miranda, K.M., Epsey, M.G. and Wink, D.A. (2001). A rapid, simple, spectrophotometric method for simultaneous detection of nitrate and nitrite.
- Mulvaney, R.L. (1996). Nitrogen - inorganic forms. In: Sparks, D.L. (Eds.), Methods of Soil Analysis. Part 3.