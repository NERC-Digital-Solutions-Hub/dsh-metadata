# Authors must be acknowledged if data are re-used or reproduced. The data is derived from a field trial investigating greenhouse gas emissions from sheep urine patches deposited to a semi-improved upland grassland, and represents the ancillary soil measurements made alongside the greenhouse gas flux measurements.

- Context and origin
  - Field trial at Henfaes Research Station, Abergwyngregyn, North Wales (270 m a.s.l.; 53°13'N, 4°0'W).
  - Established autumn 2016 on an orthic podzol soil in semi-improved upland grassland.
  - Data represent ancillary soil measurements alongside greenhouse gas flux measurements.
  - Timeframe: one-year time-series after treatment application.

- Experimental design and treatments
  - Treatments: Control (no urine), ArtUrine (artificial urine), RealUrine (real sheep urine).
  - Urine application rates: artificial 1004 kg N ha^-1; real 1112 kg N ha^-1.
  - Design: randomised block with plots replicated (n = 4 per treatment; total n = 4 per treatment group).
  - Sample scope: soil samples collected near chambers used for gas flux measurements.

- Sampling, processing, and storage
  - Soil depth: 0–10 cm.
  - Sampling unit: 3 bulked samples per replicate plot (n = 4 per treatment).
  - Sampling method: 1.3 cm diameter auger.
  - Handling: samples refrigerated after collection; processed within 24 h.
  - Gravimetric soil moisture: determined by oven-drying at 105°C for 24 h.
  - pH and EC: measured in 1:2.5 soil-to-distilled water slurries; calibrated with certified buffers.
  - Chemical extractions: 0.5 M K2SO4 (1:5 soil-to-solution) for nitrate, ammonium, total dissolved nitrogen (TDN), and dissolved organic carbon (DOC).

- Analytical methods and QA
  - Nitrate: spectrophotometric method (Miranda et al., 2001).
  - Ammonium: spectrophotometric method (Mulvaney, 1996).
  - TD-N and DOC: analyzed with Multi N/C 2100S analyzer; calibration with matrix-matched 6-point curves.
  - QA procedures: procedural blanks, calibration curve checks, dilution and re-analysis as needed, data visually checked and corrected for errors.
  - Data limitations: zero values denote concentrations below detection limits.

- Data structure and variable definitions
  - Data headers and meanings:
    - Plot: plot and chamber identifier.
    - Date: sampling date (dd/mm/yy).
    - Days_after: days before/after treatment application.
    - Tmnt: treatment label (Control, ArtUrine, RealUrine).
    - Gravmoist: gravimetric soil moisture content (% dry weight).
    - pH: soil pH at sampling.
    - EC: electrical conductivity (µS cm^-1) at sampling.
    - Nitrate: extractable nitrate (mg NO3--N kg^-1 soil dry weight).
    - Ammon: extractable ammonium (mg NH4+-N kg^-1 soil dry weight).
    - TDN: total dissolved nitrogen (mg N kg^-1).
    - DOC: total dissolved organic carbon (mg C kg^-1).

- Data provenance and references
  - Method references for nitrate and ammonium analyses:
    - Miranda, K.M., Epsey, M.G. and Wink, D.A. (2001).
    - Mulvaney, R.L. (1996).
  - Data quality assurance and processing steps described to ensure traceability.

- Notes for reuse and accessibility
  - Data come with explicit metadata on sampling design, treatments, measurement methods, and QA.
  - Clear units, value coding (e.g., zero values for below-detection results) to aid interoperability.
  - Includes date-formatted sampling timeline and treatment mapping to support time-series analysis.