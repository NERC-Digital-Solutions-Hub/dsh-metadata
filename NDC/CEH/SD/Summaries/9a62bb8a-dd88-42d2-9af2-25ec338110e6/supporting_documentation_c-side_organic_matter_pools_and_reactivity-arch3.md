# Project Carbon Storage in Intertidal Environments (C-SIDE)

## Overview
- A study funded by NERC (NE/R010846/1) focusing on carbon storage in UK saltmarsh soils.
- Aims to quantify three pools of organic matter (labile, recalcitrant, refractory) and a carbon reactivity index (CRI) across UK saltmarsh sites from 2018–2021.
- Provides data to support monitoring of environmental health and inform policy decisions.

## Datasets and Content
- Data Resource ID: Labile, recalcitrant, and refractory organic matter in soil samples from UK saltmarshes (2018–2021).
- Key outputs: quantification of OM pools (labile, recalcitrant, refractory) and CRI.
- Primary file: C_SIDE_organic_matter_pools_and_reactivity.csv.
  - Variables included: core ID, saltmarsh name, latitude, longitude, sub-sample depth interval (cm), mid-depth, labile/recalcitrant/refractory/total organic matter (%wt), CRI (%).
  - CRI defined as %OM_R / %OM_total, indicating a continuum from fully biodegradable (0) to non-biodegradable (1).
- Metadata file details: each row provides field names, units, and formats for spatial, depth, and OM measurements.

## Study Area and Sampling
- Location: United Kingdom saltmarsh sites, selected to represent diverse but environmentally similar coastal regions.
- Spatial coverage: observations with decimal latitude/longitude in WGS84.
- Depths: core samples collected to capture vertical profiles; depth interval and mid-point recorded for sub-samples.
- Rationale: site selection aims to reflect the UK’s saltmarsh habitat diversity for robust monitoring.

## Measurements and Calculations
- Analytical method: Thermogravimetric Analysis (TGA) on freeze-dried, milled samples (~20 mg).
  - Equipment: Mettler Toledo TGA2.
  - Temperature program: 40°C to 1000°C at 10°C/min under nitrogen.
  - Data processing: thermograms aligned to a common temperature scale; clipped to 200–650°C; normalized to mass loss for comparability.
- OM fractions defined thermally:
  - Labile OM: 200–400°C
  - Recalcitrant OM: 400–650°C (includes both recalcitrant and refractory fractions)
  - Refractory OM: 550–650°C (part of the recalcitrant/refractory range)
- CRI calculation: CRI = %OM_R / %OM_total.
- Calibration and QA: Thermogravimetric calibration with standard substances (Smeaton & Austin, 2022); laboratory equipment calibrated following University of St Andrews practices.
- Data treatment: no advanced statistical processing reported (NA).

## Data Formats and Metadata
- File format: CSV (C_SIDE_organic_matter_pools_and_reactivity.csv).
- Metadata details per variable include:
  - Core Identification (text)
  - Saltmarsh name (text)
  - Latitude/Longitude (decimal degrees, WGS84)
  - Depth interval and mid-depth (cm)
  - Organic matter pools (%wt) for labile, recalcitrant, refractory, and total
  - CRI (dimensionless)
  - Unit and format descriptors for each field

## Data Quality, Governance and Openness
- Quality controls: equipment calibrations and adherence to lab practices; documented calibration and QA steps.
- Metadata emphasis: explicit field definitions, units, and coordinate system to support reproducibility and data reuse.
- Data sharing: dataset and metadata are prepared for dissemination, with clear provenance and methodological transparency to support governance and oversight.

## Funding and References
- Funding: Natural Environment Research Council (NERC), grant NE/R010846/1.
- References guiding methods:
  - Kristensen, E. (1990). Characterization of biogenic organic matter by stepwise thermogravimetry.
  - Smeaton, C. & Austin, W.E.N. (2022). Quality not quantity: Prioritizing sedimentary organic matter management. Geophysical Research Letters.