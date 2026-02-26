# Details of data structure to ' HF_soil_minN.csv '

## Overview
- Dataset comprises 11 columns and 608 rows.
- Contains soil NH4-N and NO3-N + NO2-N concentrations, soil moisture contents, soil pH, and electrical conductivity (EC).
- Data originate from a grassland fertiliser trial conducted in 2016 at Henfaes Research Station (Bangor University).

## Dataset structure (columns and units)
- Date: Date of sampling.
- N_app: Fertiliser application identifier; values 1, 2, or 3 denote applications.
  - 1st & 2nd applications: 90 kg ha-1
  - 3rd application: 60 kg ha-1
- Block: Blocking factor of the randomized block design (values 1–4).
- Plot: Plot number (values 1–16).
- Treatment: Fertiliser type; categories are AN, U, IU, C.
  - AN = ammonium nitrate
  - U = urea
  - IU = inhibited urea (agrotain)
  - C = 0N control
- Soil_NH4_mgNkg: Ammonium concentration in soil (mg NH4-N kg-1), dry weight basis.
- Soil_NO3_mgNkg: Nitrate concentration in soil (mg NO3-N kg-1), dry weight basis.
- moisture_dry: Soil moisture on a dry weight basis (g H2O g dry soil-1).
- moisture_wet: Soil moisture on a wet weight basis (g H2O g wet soil-1).
- pH: Soil pH.
- EC: Soil electrical conductivity (µS cm-1).

Note: Soil samples were collected from 0–10 cm depth using a 1 cm diameter corer; for each plot, six samples were bulked prior to analysis.

## Sampling and measurement methods
- Extraction: 5 g soil with 25 ml 0.5 M K2SO4; shake 30 minutes at 200 rpm.
- Nitrate analysis: Colorimetric method (Miranda et al., 2001).
- Ammonium analysis: Method (Mulvaney, 1996).
- Soil moisture: Determined after drying at 105°C for 24 hours.
- pH and EC: Measured with standard electrodes on a 1:2.5 soil to deionised water suspension.

## Experimental design and provenance
- Location: Grassland fertiliser trial, 2016, Henfaes Research Station (Bangor University).
- Design features: Randomised block design with blocks 1–4, plots 1–16; treatments reflect different N sources/types.
- Data context: Supplement to supporting documentation for data series; details linked to broader CINAg experiment documentation.

## Data governance and stewardship considerations
- Provenance clearly documented (trial year, location, sampling depth, and methods), aiding auditability and reproducibility.
- Metadata should align column names, units, and treatment coding with related documentation to ensure consistency across portals.
- Potential data stewardship actions:
  - Validate and standardise units across datasets (e.g., confirm dry vs. wet weight denominators).
  - Maintain traceability between N_app values and actual application rates.
  - Manage any updates or revisions by linking back to the supporting documentation package.
  - Check for any data availability or sharing constraints in related governance documents.