# Data from a field trial investigating greenhouse gas emissions from sheep urine patches deposited to a semi-improved upland grassland

- Overview
  - Dataset derives from a field trial examining greenhouse gas emissions from sheep urine patches deposited on semi-improved upland grassland.
  - Represents ancillary soil measurements collected alongside greenhouse gas flux measurements.
  - Location: orthic podzol at Henfaes Research Station, Abergwyngregyn, North Wales (270 m a.s.l.; 53°13'N, 4°0'W).
  - Timeframe: one-year time-series following treatment application (sampling dates provided within the data file).

- Experimental design and treatments
  - Plot design: randomised block design with replicate plots.
  - Treatments (per plot): Control (no urine), ArtUrine (artificial urine), RealUrine (real sheep urine).
  - Urine application rates: artificial urine at 1004 kg N ha-1; real sheep urine at 1112 kg N ha-1.
  - Replication: n = 4 plots per treatment; soil samples collected from 4 replicate plots per treatment.
  - Soil depth sampled: 0–10 cm.

- Sampling and measurements
  - Soil sampling details: n = 3 bulked samples per replicate plot.
  - Sample processing: soil moisture determined by oven drying (24 h, 105 °C); samples refrigerated after collection and processed within 24 h.
  - Measured parameters:
    - Gravmoist: gravimetric soil moisture (% dry weight)
    - pH: soil pH in 1:2.5 soil-to-distilled water slurry
    - EC: soil electrical conductivity (µS cm-1)
    - Nitrate: extractable nitrate (0.5 M K2SO4, mg NO3--N kg-1 soil dry weight)
    - Ammonium: extractable ammonium (0.5 M K2SO4, mg NH4+-N kg-1 soil dry weight)
    - TDN: total dissolved nitrogen (0.5 M K2SO4 extract, mg N kg-1 soil dry weight)
    - DOC: dissolved organic carbon (0.5 M K2SO4 extract, mg C kg-1 soil dry weight)

- Analytical methods and QA
  - Extraction: 0.5 M K2SO4 (1:5 soil-to-solution) for nitrate, ammonium, TDN, and DOC.
  - Nitrate method: Miranda et al. (2001) spectrophotometric method; results tied to matrix-matched calibration curves.
  - Ammonium method: Mulvaney (1996); spectrophotometric analysis with matrix-matched curves.
  - TDN and DOC: analyzed on a Multi N/C 2100S (AnalytikJena) with matrix-matched 6-point calibration curves.
  - Calibration and QA: procedural blanks analyzed; calibration curves visually inspected; samples re-analyzed if necessary; data visually checked and corrected for errors.
  - Data notes: zeros indicate concentrations below detection limits.

- Data structure and headers
  - Plot: plot and chamber identifier (within the plot)
  - Date: sampling date (dd/mm/yy)
  - Days_after: days relative to treatment application
  - Tmnt: treatment type (Control, ArtUrine, RealUrine)
  - Gravmoist: gravimetric soil moisture (%)
  - pH: soil pH
  - EC: soil EC (µS cm-1)
  - Nitrate: 0.5 M K2SO4 extractable nitrate (mg NO3--N kg-1 soil dw)
  - Ammon: 0.5 M K2SO4 extractable ammonium (mg NH4+-N kg-1 soil dw)
  - TDN: 0.5 M K2SO4 extractable total dissolved nitrogen (mg N kg-1 soil dw)
  - DOC: 0.5 M K2SO4 extractable total dissolved organic carbon (mg C kg-1 soil dw)

- Data usage and governance
  - Acknowledgement: Authors must be acknowledged if data are reused or reproduced.
  - Relevance for monitoring frameworks: Provides a structured, QA‑backed example of environmental soil measurements linked to a field trial on nutrient deposition and potential GHG dynamics; includes clear metadata, sampling design, and measurement protocols suitable for integration into monitoring dashboards and decision-support tools.

- References (methodologies)
  - Miranda, K.M., Epsey, M.G. and Wink, D.A. (2001). A rapid, simple, spectrophotometric method for simultaneous detection of nitrate and nitrite. Nitric Oxide 5, 62-71.
  - Mulvaney, R.L. (1996). Nitrogen - inorganic forms. In: Sparks, D.L. (Eds.), Methods of Soil Analysis. Part 3. Madison, WI, USA: Soil Science Society of America Inc., pp. 1123-1184.