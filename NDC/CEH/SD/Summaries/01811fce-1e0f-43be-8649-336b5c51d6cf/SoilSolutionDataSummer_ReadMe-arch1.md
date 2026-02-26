# ReadMe file for SoilSolutionDataSummer.csv

## Overview
- Dataset contains soil solution chemistry data from three treatments: control (no urine), artificial sheep urine patches, and real sheep urine patches.
- Study site: dystric histosol in unimproved grazing land, Carneddau mountains, Snowdonia National Park, Wales, UK (556 m a.s.l.; 53°22'N, 3°95'W).
- Sheep excluded from plots from 15/05/2017 to avoid recent excretal confounding effects.
- Sampling method: Rhizon soil solution samplers (2.5 mm diameter, 5 cm porous section, 12 cm tubing) inserted at 45° to soil surface within urine patches and controls in chambers.
- Sample collection aimed for a minimum of three samples per treatment across four replicates (n ≥ 3).

## Experimental Design
- Treatments applied on 24/07/2017:
  - Control: no urine.
  - Artificial sheep urine: patches with N application rate of 920 kg N ha^-1; 200 ml artificial urine over 100 cm^2 per patch.
  - Real sheep urine: patches with N application rate of 930 kg N ha^-1; 200 ml real urine over 100 cm^2 per patch.
- Samples collected at multiple dates after treatment; data include days after treatment (Days) and the date of collection (Date).
- Each sample linked to a specific chamber (plot and chamber number).

## Analytes and Measurements
- Nitrate (NO3^--N) in mg NO3^- -N L^-1 (measured by Miranda et al., 2001).
- Ammonium (NH4^+-N) in mg NH4^+-N L^-1 (measured by Mulvaney, 1996).
- Dissolved Organic Carbon (DOC) in mg C L^-1.
- Total Dissolved Nitrogen (TN) in mg N L^-1.
- All solutions stored at -20 °C until analysis; analyses performed against certified standards.

## Data File and Headers
- Data header fields in SoilSolutionDataSummer.csv:
  - Date: date of soil sample collection (dd/mm/yyyy)
  - Days: days after treatment when sampling occurred
  - Treatment: Control, ArtUrine (Artificial urine), RealUrine (Real urine)
  - Chamber: plot and chamber identifier
  - Nitrate: mg NO3^- -N L^-1
  - Ammonium: mg NH4^+-N L^-1
  - DOC: mg C L^-1
  - TN: mg N L^-1

## Data Quality and Replication
- Successful sampling achieved in at least three of the four replicate treatments (n ≥ 3).

## Usage Notes and References
- Data intended to analyze differences between urine types and their impact on soil solution chemistry, with potential for correlation analysis and predictive modelling.
- Acknowledgement required if data are reused or reproduced.
- Analytical methods references:
  - Miranda, K.M., Epsey, M.G. and Wink, D.A. (2001). A rapid, simple, spectrophotometric method for simultaneous detection of nitrate and nitrite. Nitric Oxide 5, 62-71.
  - Mulvaney, R.L. (1996). Nitrogen - inorganic forms. In: Sparks, D.L. (Eds.), Methods of Soil Analysis. Part 3. Madison, WI: SSSA, pp. 1123-1184.