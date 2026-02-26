# ReadMe file for SpringSoilsData.csv

- Purpose and scope
  - Documents ancillary soil measurements collected alongside greenhouse gas flux measurements from a field trial examining sheep urine patches on semi-improved upland grassland.
  - Data represent 0–10 cm soil samples taken from control plots and replicated artificial or real sheep urine patches.

- Experimental design and location
  - Location: orthic podzol at Henfaes Research Station, Abergwyngregyn, North Wales (270 m a.s.l.; 53°13'N, 4°0'W).
  - Treatments: Control (no urine), ArtUrine (artificial urine), RealUrine (real sheep urine).
  - Application rates: artificial urine = 1066 kg N ha^-1; real sheep urine = 756 kg N ha^-1.
  - Design: randomised block with 4 plots per treatment (n = 4 per treatment; total 12 plots).
  - Sampling: soil samples collected over a one-year time series following treatment.

- Sample collection and processing
  - Soil depth: 0–10 cm; samples from each plot are bulked from 3 subsamples.
  - Timeframe: samples collected over a year, with sampling dates provided in the data file.
  - Handling: soils refrigerated after collection and processed within 24 h.
  - Soil moisture: gravimetric moisture determined by drying at 105 °C for 24 h.

- Measurements and analytical methods
  - pH and EC: measured in 1:2.5 soil-to-distilled water slurries; electrodes calibrated with certified buffers before each measurement.
  - Extractable nutrients: 0.5 M K2SO4 extraction (1:5 soil-to-solution) for:
    - Nitrate (NO3--N) by spectrophotometry (Miranda et al. 2001).
    - Ammonium (NH4+-N) by spectrophotometry (Mulvaney 1996).
  - Total dissolved nitrogen (TDN) and dissolved organic carbon (DOC): analyzed on a Multi N/C 2100S (AnalytikJena) with matrix-matched 6-point calibration.
  - Calibration and QA: matrix-matched calibration curves, procedural blanks, calibration curve checks, re-analysis as needed, and visual data checks for errors.

- Data structure and headers
  - Plot: plot and chamber identifier.
  - Date: sampling date.
  - Days_after: days before/after treatment.
  - Tmnt: treatment category (Control, ArtUrine, RealUrine).
  - Gravmoist: gravimetric soil moisture content (% dry weight).
  - pH: soil pH at sampling.
  - EC: soil electrical conductivity (µS cm^-1).
  - Nitrate: 0.5 M K2SO4 extractable nitrate (mg NO3--N kg^-1 soil dw).
  - Ammon: 0.5 M K2SO4 extractable ammonium (mg NH4+-N kg^-1 soil dw).
  - TDN: 0.5 M K2SO4 extractable total dissolved nitrogen (mg N kg^-1 soil dw).
  - DOC: 0.5 M K2SO4 extractable total dissolved organic carbon (mg C kg^-1 soil dw).

- Data quality assurance and processing
  - Use of procedural blanks and calibration checks.
  - Visual inspection and correction of data; re-analysis when necessary.
  - Documentation of data sources and measurement procedures to support reproducibility.

- References for methods
  - Miranda, K.M., Epsey, M.G., and Wink, D.A. (2001). A rapid, simple, spectrophotometric method for simultaneous detection of nitrate and nitrite. Nitric Oxide, 5, 62-71.
  - Mulvaney, R.L. (1996). Nitrogen - inorganic forms. In Sparks, D.L. (Ed.), Methods of Soil Analysis. Part 3. SSSA Inc., pp. 1123-1184.