# Authors must be acknowledged if data are re-used or reproduced. The data is derived from a field trial investigating greenhouse gas emissions from sheep urine patches deposited to a semi-improved upland grassland, and represents the ancillary soil measurements made alongside the greenhouse gas flux measurements.

## Study context and location
- Field trial on an orthic podzol at Henfaes Research Station, Abergwyngregyn, North Wales (270 m a.s.l.; 53°13'N, 4°0'W).
- Established in autumn 2016.
- Aimed to collect ancillary soil measurements alongside greenhouse gas flux data from sheep urine patches.

## Experimental design
- Randomised block design with 4 plots per treatment.
- Treatments: Control (no urine), ArtUrine (artificial urine), RealUrine (real sheep urine).
- Urine application rates: artificial urine 1004 kg N ha^-1; real urine 1112 kg N ha^-1.
- Replicates: 4 plots per treatment; patches located near gas flux chambers.
- Timeframe: one-year time series after treatment.

## Sampling and sample processing
- Soil depth: 0–10 cm.
- Sampling: 3 bulked samples per replicate plot (n = 4) using a 1.3 cm diameter auger.
- Sample handling: refrigerated after collection; processed within 24 h.
- Gravimetric soil moisture (Gravmoist) measured as % dry weight.
- pH and EC measured on 1:2.5 soil-to-distilled water slurries; electrodes calibrated with certified buffers.

## Laboratory analyses
- Extraction: 0.5 M K2SO4, 1:5 soil-to-solution.
- Analytes:
  - Nitrate (NO3^--N) and ammonium (NH4^+-N) via spectrophotometry.
  - Total dissolved nitrogen (TDN) and dissolved organic carbon (DOC) via Multi N/C 2100S.
- Calibration: matrix-matched 6-point curves using certified stock solutions.
- Data QA: procedural blanks, calibration curve checks, dilution/reanalysis as needed, calibration curves checked for precision.
- Notes: zero values indicate concentrations below detection limits.

## Data structure and variables
- Data headers and meaning:
  - Plot: plot and chamber identifier.
  - Date: sampling date (dd/mm/yy).
  - Days_after: days relative to treatment application.
  - Tmnt: treatment code (Control, ArtUrine, RealUrine).
  - Gravmoist: gravimetric soil moisture (%, dry weight basis).
  - pH: soil pH at sampling time.
  - EC: soil electrical conductivity (µS cm^-1).
  - Nitrate: 0.5M-K2SO4 extractable nitrate (mg NO3--N kg^-1 soil dry weight).
  - Ammon: 0.5M-K2SO4 extractable ammonium (mg NH4+-N kg^-1 soil dry weight).
  - TDN: 0.5M-K2SO4 extractable total dissolved nitrogen (mg N kg^-1 soil dry weight).
  - DOC: 0.5M-K2SO4 extractable dissolved organic carbon (mg C kg^-1 soil dry weight).

## Data provenance and usage notes
- Data are derived from a field trial; attribution is required: authors must be acknowledged if data are reused or reproduced.
- One-year time-series sampling; exact dates and sampling frequency are provided in the data file.
- The dataset enables linkage of soil chemical properties with greenhouse gas flux measurements for understanding urine patch effects on soil microbiology and nutrient dynamics.

## References
- Miranda, K.M., Epsey, M.G., and Wink, D.A. (2001). A rapid, simple, spectrophotometric method for simultaneous detection of nitrate and nitrite. Nitric Oxide 5, 62-71.
- Mulvaney, R.L. (1996). Nitrogen - inorganic forms. In Sparks, D.L. (Ed.), Methods of Soil Analysis. Part 3. Madison, WI, USA: SSSA Inc., pp. 1123-1184.