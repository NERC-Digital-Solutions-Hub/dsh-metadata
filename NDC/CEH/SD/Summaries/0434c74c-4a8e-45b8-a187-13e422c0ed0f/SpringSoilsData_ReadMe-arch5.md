# ReadMe file for SpringSoilsData.csv

## Overview
- ReadMe for the SpringSoilsData.csv dataset describing ancillary soil measurements linked to a field trial on greenhouse gas emissions from sheep urine patches.
- Field trial location and design: orthic podzol at Henfaes Research Station, North Wales, spring 2016.
- Data cover soil samples (n = 3 bulked per replicate plot, n = 4 replicates) from control or urine-treated patches, depth 0–10 cm, collected alongside GHG flux measurements.
- Time-series data spanning one year after treatment application.

## Experimental design and treatments
- Design: randomised block with four replicates per treatment.
- Treatments:
  - Control (no urine)
  - ArtUrine (artificial urine, 1066 kg N ha-1)
  - RealUrine (real sheep urine, 756 kg N ha-1)
- Sampling: soil samples collected from each plot (n = 3 bulked per replicate plot) across a one-year period post-treatment.
- Depth: 0–10 cm soil layer.
- Sampling cadence and dates are included within the data file.

## Sample handling and storage
- Samples refrigerated after collection and processed within 24 hours.
- Soil moisture determined by drying (105 °C, 24 h).

## Measurements and analytical methods
- pH and EC: measured in 1:2.5 soil-to-distilled water slurries; electrodes calibrated with certified buffers prior to measurements.
- Extractable nutrients: 0.5 M K2SO4 extraction (1:5 soil:solution) for:
  - Nitrate (NO3--N)
  - Ammonium (NH4+-N)
  - Total dissolved nitrogen (TDN)
  - Dissolved organic carbon (DOC)
- Nitrate: determined by Miranda et al. (2001) method; ammonium: Mulvaney (1996) method; both via spectrophotometry with matrix-matched calibration curves.
- TD N and DOC: measured with Multi N/C 2100S analyzer; calibration with 6-point curves from certified standards.
- Quality assurance: procedural blanks, calibration curve inspection, re-analysis if needed, dilution as necessary; data checked and corrected for errors.

## Data structure and headers
- Plot: plot and chamber identifier.
- Date: sampling date.
- Days_after: days relative to treatment application.
- Tmnt: treatment type (Control, ArtUrine, RealUrine).
- Gravmoist: gravimetric soil moisture (%) at sampling (dry weight basis).
- pH: soil pH at sampling.
- EC: soil electrical conductivity (µS cm-1) at sampling.
- Nitrate: extractable nitrate (mg NO3--N kg-1 soil dry weight).
- Ammon: extractable ammonium (mg NH4+-N kg-1 soil dry weight).
- TDN: extractable total dissolved nitrogen (mg N kg-1 soil dry weight).
- DOC: extractable total dissolved organic carbon (mg C kg-1 soil dry weight).

## Data governance, usage and attribution
- Authors must be acknowledged if data are reused or reproduced.
- Data are derived from a single year-long field study; interpret in the context of the experimental design and measurement methods described.
- Method references provided for nitrate and ammonium analyses; general soil analysis methods cited.