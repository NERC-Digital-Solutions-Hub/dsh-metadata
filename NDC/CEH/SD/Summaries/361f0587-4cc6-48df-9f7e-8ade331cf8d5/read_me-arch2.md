# Data collected by Vicky Bowskill (https://orcid.org/0000-0003-0293-327X) as part of PhD research with School of Environment, Earth and Ecosystem Sciences, Faculty of Science, Technology, Engineering and Mathematics, The Open University, Walton Hall, Milton Keynes, MK7 6AA

## Overview
- Dataset from a PhD project funded by NERC CENTA2 (NE/S007350/1).
- Nutritive data for floodplain meadow hay collected in central England.
- Data description includes structure, sampling design, lab methods, and units.
- 1 CSV file is provided.
- Linked publications with full methodological descriptions and datasets:
  - https://doi.org/10.1016/j.biocon.2023.110140
  - https://doi.org/10.21954/ou.ro.00097871
- The dataset supports standardized reporting of environmental nutritive quality over time and across sites.

## Data content and structure
- Topics covered: nutritive composition of floodplain meadow hay.
- Collection scope: 4 sites in central England (narrative) with structured dataset listing 3 sites.
- Temporal coverage: 2 years.
- Sampling design:
  - Samples per site: 6 (bulked pairwise in year 2 to reduce sampling costs)
  - Replicates per sample: 2 (each data point is the mean of two replicates)
- Data file format: 1 CSV file.
- Layout:
  - Columns represent variables.
  - Rows represent records.
- Site/year/replicate details:
  - Sites: 3 (narrative also mentions 4 sites)
  - Years: 2
- Data provenance: Lab-derived nutritive metrics with defined field/lab methodologies.

## Variables, methods, and units
- Lab methods:
  - Near Infrared Spectroscopy (NIRS) for CP, ME, ADF, NDF
  - Inductively Coupled Plasma Optical Emission Spectrometry (ICP-OES) for P, B, Ca, Cu, K, Mg, Mn, Mo, Na, Se, S, Zn
  - Inductively Coupled Plasma Mass Spectrometry (ICP-MS) for I
- Data labels (guides):
  - GDD: Accumulated Growing Degree-days (thermal time)
  - AET: Accumulated Actual Evapotranspiration
  - GFratio: Graminoid:Forb ratio
  - CP: Crude Protein
  - ME: Metabolisable Energy
  - ADF: Acid Digestible Fibre
  - NDF: Neutral Digestible Fibre
- Units:
  - gm2: grams per square meter
  - gkg: grams per kilogram
  - mgkg: milligrams per kilogram
  - percent: percent content
  - offtake: (% content × yield) / 100
  - Mjkg: MegaJoules per kilogram

## Data provenance and accessibility
- Funding: NERC CENTA2 grant NE/S007350/1.
- File format: 1 CSV file.
- Publications for methodological context:
  - https://doi.org/10.1016/j.biocon.2023.110140
  - https://doi.org/10.21954/ou.ro.00097871

## Applications for environmental monitoring
- Provides standardized nutritive indicators for floodplain meadow hay across multiple sites and two years.
- Facilitates time-series analyses of environmental health and land-management impacts on forage quality.
- Can be integrated into broader environmental monitoring portals with standardized unit definitions and variable labels.

## Considerations for reuse and quality
- Inconsistency to note: narrative mentions 4 sites, while the structure lists 3 sites.
- Sampling design includes bulked samples in year 2 to reduce costs; replicates are averaged, which affects variance estimates.
- Ensure consistent interpretation of derived variables (e.g., I/ICP-MS data) and confirm site-year mapping for longitudinal analyses.
- Data are structured for straightforward integration into monitoring dashboards via the provided CSV and defined units/labels.