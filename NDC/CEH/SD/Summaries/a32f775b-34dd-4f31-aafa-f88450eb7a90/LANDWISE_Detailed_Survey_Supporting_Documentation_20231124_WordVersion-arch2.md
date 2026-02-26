# LANDWISE Detailed Survey Supporting Documentation (Version 1.4)

- Purpose: Document a detailed LANDWISE survey of soil hydraulic and hydrological properties in the Thames catchment to understand field-scale heterogeneity under different Natural Flood Management (NFM) practices and to support flood risk reduction analyses.

## Overview of the dataset

- Contains surface and sub-surface soil properties across the Thames catchment: bulk density, inferred porosity, volumetric soil moisture content, and soil moisture retention (to 100 cm suction); surface infiltration rates; and saturated hydraulic conductivity (Ksat) at 25 cm and 45 cm depth.
- Field-scale, point-based measurements from 7 plots/sites, covering three land-use/management groups.
- Sampling periods: April 2021 to October 2021, with repeats pre- and post-harvest; subset of sites measured for soil moisture retention.
- Part of the LANDWISE project (NERC), aiming to assess natural land-based measures for flood risk reduction; linked to a Broad-scale survey and other LANDWISE documentation.

## Study design and sites

- Seven fields selected from a Broad-scale survey for detailed investigation; sites grouped by geology and soil type: mudstone, chalk (carbonate), and limestone.
- Land-use/management variation includes permanent grassland, woodland, arable with conventional or controlled traffic, and herbal ley in rotation.
- Sampling locations within fields categorized as:
  - TR = Trafficked areas (tramlines, animal tracks)
  - IN = Infield areas
  - UN = Untrafficked field margins
- Sampling layout: 15 locations per field (TR1-5, IN1-5, UN1-5) to capture within-field heterogeneity; Figure 1 and Table 2 detail site layout and IDs.

## Measurements and methods

- Bulk density and inferred porosity
  - Ground-truth via volumetric soil cores and oven-drying (105 °C); samples per field and per site type specified.
- Soil moisture retention (pF 0–pF 2)
  - Sandbox method with deionized water; measurements at multiple suction pressures; used to derive porosity and moisture characteristics.
- Infiltration and unsaturated hydraulic conductivity
  - Infiltration rate (Kunsat) measured with Mini Disk Infiltrometers across arable, grassland, and woodland fields; suction rates typically 2 cm (0.5 cm on heavier clay soils); intervals chosen per soil type.
  - Calculations use Zhang (1997) method to fit cumulative infiltration and derive unsaturated hydraulic conductivity; van Genuchten parameters sourced from Carsel & Parrish (1988).
- Saturated hydraulic conductivity (Kfs)
  - Measured at 25 cm and 45 cm depths using Guelph Permeameters; two-head method preferred for accuracy; measurements offset to avoid disturbance; Kfs calculated using a dedicated calculator.
- Soil and vegetation root depth
  - Depths measured with Auger and tape measure across field types.

## Data structure and content

- One CSV file: LANDWISE_detailed_survey_soil_data_2021_updated_v2
- Variables: 70 columns and 380 rows (including identifiers, location data, site/field/location codes, measurement results, QC flags, and notes)
- Location identifiers: ID_SiteNo, ID_FieldNo, ID_LocationCode, plus combined codes for site-field-location
- Spatial references: OS Grid, Easting/Northing in British National Grid
- Temporal coverage: Spring (April 2021) and Autumn (October 2021) campaigns; pre- and post-harvest timings for certain measurements
- Data completeness: NA values used for missing measurements or where measurements were not taken

## Quality control and data processing

- Data entry QC: field/lab measurements entered by the recorder and cross-checked by another person to correct typos.
- Infiltration QC flags (Infiltration_1_QC_Flag, Infiltration_2_QC_Flag):
  - Good, Invalid (physically implausible; removed), A (unsteady infiltration rate), B (<15 ml infiltrated), C (unusually high K values).
- Saturated conductivity QC flags (Guelph_Permeameter_QC_Flag):
  - Good, Invalid (plausibility issues; removed)
- Notes indicate whether double-head or averaged single-head Guelph measurements were used; double-head preferred for accuracy where valid.
- QC details and flag meanings are documented to support traceability and data reuse.

## Fieldwork and instrumentation

- Soil sampling: Eijkelkamp 07.53.SC sample rings with closed ring holder; augers (Edelman, Stony) as required.
- Lab equipment: ovens (105 °C) for drying; precise balances for mass measurements; sandbox for moisture retention; mini-disk infiltrometers; Guelph permeameter for Kfs.
- Calibration and traceability: balances calibrated to 0.1 g; annual independent calibration of lab balances; reference manuals and software cited for data processing.

## Context and related datasets

- Related to LANDWISE Broad-scale survey dataset: Soil near-surface properties, vegetation observations, land use and land management for Thames catchment locations (2018–2021).
- Documentation and software references provided for methods (Zhang 1997; Carsel & Parrish 1988; METER infiltrometer manual; Guelph permeameter instructions; LANDWISE supporting docs).

## Relevance for Analysts Monitoring the Environment

- Provides standardized, field-scale soil hydraulic data across multiple sites and land-management regimes, enabling cross-site comparisons and trend analyses relevant to flood risk management.
- Facilitates data integration with other environmental datasets (e.g., soil, land use, hydrology) to enhance assessment of natural flood management effectiveness.
- Clear metadata, QC flags, and detailed methods support reproducibility, auditability, and data sharing with stakeholders and policy teams.
- The dataset supports understanding how different land uses and soil types influence infiltration, porosity, and water retention, informing monitoring and decision-making for environmental health and policy performance over time.