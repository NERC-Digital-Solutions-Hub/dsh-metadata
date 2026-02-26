# ReadMe file for SpringSoilsData.csv

## Overview
- Describes ancillary soil measurements associated with a field trial on greenhouse gas emissions from sheep urine patches in semi-improved upland grassland.
- Data collected alongside greenhouse gas flux measurements; derived from soil samples and standard soil chemical analyses.

## Study and sampling design
- Location: orthic podzol at Henfaes Research Station, Abergwyngregyn, North Wales (270 m a.s.l.; 53°13'N, 4°0'W).
- Establishment: spring 2016; time-series data over one year after treatment.
- Plot design: randomized block design with n = 4 plots per treatment.
- Treatments: Control (no urine), ArtUrine (artificial urine), RealUrine (real sheep urine).
- Urine application rates: artificial 1066 kg N ha-1; real urine 756 kg N ha-1.
- Soil sampling: 0–10 cm depth; 3 bulked samples per replicate plot (n = 4 plots per treatment).
- Sampling cadence: dates provided in the data file; measurements span one year post-treatment.

## Measurements and laboratory methods
- Soil properties measured: gravimetric moisture (gravmoist, % dry weight), pH, EC (µS cm-1).
- Chemical extractions: 0.5 M K2SO4 (1:5 soil-to-solution) for extractable nitrate, ammonium, total dissolved nitrogen (TDN), and dissolved organic carbon (DOC).
- Analytical methods:
  - Nitrate: Miranda et al., 2001; spectrophotometric analysis with calibration curves from certified standards.
  - Ammonium: Mulvaney, 1996; spectrophotometric analysis with calibration curves.
  - TDN and DOC: analyzed with Multi N/C 2100S (AnalytikJena) using matrix-matched calibration curves.
- Quality assurance: analysis of procedural blanks, visual inspection of calibration curves, re-analysis and corrections as needed; calibration curves checked for precision.

## Data structure and headers
- Plot: plot and chamber identifier.
- Date: sampling date.
- Days_after: days before/after treatment.
- Tmnt: treatment category (Control, ArtUrine, RealUrine).
- Gravmoist: gravimetric soil moisture (%, dry weight basis) at sampling.
- pH: soil pH at sampling.
- EC: soil EC (µS cm-1) at sampling.
- Nitrate: extractable nitrate (mg NO3-N kg-1 soil dry weight).
- Ammon: extractable ammonium (mg NH4+-N kg-1 soil dry weight).
- TDN: total dissolved nitrogen (mg N kg-1 soil dry weight).
- DOC: dissolved organic carbon (mg C kg-1 soil dry weight).

## Data quality, processing, and interpretation
- Data were refrigerated post-collection and processed within 24 hours.
- QA procedures included blanks, calibration curve checks, and re-analysis if necessary; results were visually checked and corrected for errors.
- Data are linked to greenhouse gas flux measurements from the same trial, enabling integrated analysis of soil chemistry and emissions.

## Attribution, usage, and metadata
- Authors must be acknowledged when data are reused or reproduced.
- References for methods:
  - Miranda et al. (2001) for nitrate/nitrite detection.
  - Mulvaney (1996) for inorganic nitrogen forms (soil analysis methods).
- Important for data leaders: assess data discoverability, provenance, and alignment with other datasets; plan for attribution and potential data gaps (e.g., limited depth, time points).