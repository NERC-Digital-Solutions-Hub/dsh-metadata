# LANDWISE Detailed Survey Supporting Documentation (Version 1.4)

- Scope: This document accompanies a field-based dataset of surface and sub-surface hydraulic and hydrological soil properties across the Thames catchment, collected in 2021 as part of the LANDWISE project to assess natural flood management measures.
- Key variables: soil bulk density, inferred porosity, volumetric soil moisture content, soil moisture retention (to 100 cm suction), surface infiltration rates, and saturated hydraulic conductivity at 25 cm and 45 cm depths.
- Spatial and sampling basis:
  - 7 field sites across three geology/soil groups (mudstone, chalk/carbonate, limestone) with three land-use/management scenarios.
  - Field-scale, transect-based sampling within each field, including trafficked areas (TR), infield (IN), and untrafficked margins (UN).
  - Site IDs and field IDs include 18_6, 44_1, 26_1, 23_5, 31_3, 27_2, 27_4; locations summarized in tables/figures with approximate easting/northing in British National Grid.
- Temporal coverage: Measurements taken in Spring (April 2021) and Autumn (October 2021); some soil moisture retention measurements on limestone sites only.
- Data structure: A single CSV file named LANDWISE_detailed_survey_soil_data_2021_updated_v2 with 70 columns and 380 rows; missing values encoded as NA. Column names and units are documented in the dataset description.

## Research Design

- Field selection: Seven fields chosen from a Broad-scale LANDWISE survey to enable detailed comparisons of land-use and management effects on field-scale heterogeneity. Soils and geology vary across sites (two mudstone, two carbonate/chalk, three limestone).
- Sites and fields: Each site corresponds to a geology/soil type with distinct land-use/management: permanent grassland, arable with/without grass, unmanaged woodland, conventional or controlled traffic management, and herbal ley rotations.
- Sampling objective: Characterise how field-scale heterogeneity under different natural flood management measures influences soil hydraulic and hydrological properties.

## Sampling Strategy and Locations

- Sampling within fields: 15 locations per field arranged along transects:
  - TR: Trafficked areas (e.g., tramlines, animal tracks)
  - IN: Infield areas
  - UN: Untrafficked field margins
- Location mapping: Transect-based layout with five locations per type (TR1–TR5, IN1–IN5, UN1–UN5).
- Measurements per location: A range of soil physical properties collected across seasons, as described in Tables 3 and 4 of the documentation.

## Soil Sampling and Measurements

- Soil collection: Kept in polyethylene bags and refrigerated; samples prepared for lab analyses.
- Bulk density and porosity: Volumetric soil cores with oven-drying (105°C) to determine dry bulk density; porosity inferred from dry bulk density.
- Soil moisture retention: Sandbox method (pF 0 to pF 2) to derive moisture retention characteristics.
- Infiltration and hydraulic conductivity:
  - Infiltration: Mini Disk Infiltrometers used to estimate unsaturated hydraulic conductivity (Kunsat) from cumulative infiltration over time; suction rates typically 2 cm, with 0.5 cm used for heavier clay soils; at least 15 ml infiltration targeted.
  - Saturated hydraulic conductivity: Guelph Permeameters measured at 25 cm and 45 cm depths; two-head method preferred for higher accuracy; measurements taken at nearby locations to avoid disturbance.
- Root depth and vegetation: Soil and vegetation root depth measured with auger and tape measure for arable, grassland, and woodland sites.
- Field-to-lab workflow: Field data entered in Excel, then processed per established calculation methods (e.g., Zhang 1997 for infiltration; Carsel & Parrish 1988 for soil texture/class parameters).

## Nature and Units of Recorded Values

- Data columns cover identifiers (site, field, location), location types, grid references (OS Grid, Easting/Northing), sampling dates/times, depths, horizons, and a wide range of measured properties (e.g., VWC, bulk density, porosity, Kunsat, Kfs, soil moisture retention values at various pF stages).
- Units are stated within the documentation and included in the dataset reference table (Table 5).

## Quality Control

- Data entry QC: Field and lab data transcribed into Excel by the recording author and validated by a second person.
- Infiltration QC flags: Good, Invalid, A, B, C to flag data quality issues (e.g., implausible values, insufficient infiltration volume, unsteady trends, or unusually high K values). Invalid entries removed from the dataset.
- Saturated hydraulic conductivity QC flags: Good or Invalid (e.g., physically implausible or out-of-range alpha values); affected measurements are documented in notes.
- Method choice notes: When double-head Guelph measurements yielded inadmissible values, single-head measurements were used and averaged; details available in the Guelph permeameter operating instructions.

## Details of Data Structure

- File: LANDWISE_detailed_survey_soil_data_2021_updated_v2.csv
- Content: 70 columns, 380 rows; column order follows the documented schema (Table 5).
- NA values indicate missing or invalid measurements as flagged in QC fields or notes.

## Fieldwork and Laboratory Instrumentation

- Equipment used:
  - Soil sampling: Eijkelkamp 07.53.SC kit with closed ring holder; Edelman and Stony augers.
  - Drying and weighing: Heraeus Function Line ovens; Precisa balances (lab and sandbox); calibration checks performed.
  - Infiltration: Mini Disk Infiltrometers (Decagon Devices).
  - Saturated conductivity: Guelph Permeameter (Soilmoisture Equipment Corp.).
  - Moisture retention: Eijkelkamp Sandbox.
- Calibration and quality: Balances calibrated to 0.1 g; annual calibration of lab balances; field equipment used per manufacturer guidance.

## Miscellaneous and Related Data

- Relationship: Connected to the Landwise Broad-scale survey dataset covering soil near-surface properties, vegetation observations, land use, and land management at 1,800 Thames catchment locations (2018–2021).
- References: Carsel & Parrish (1988); Zhang (1997); METER/Decagon manuals; Soilmoisture Equipment Corp. instructions and calculators.

## References

- Carsel, R. F., & Parrish, R. S. (1988). Developing Joint Probability Distributions of Soil Water Retention Characteristics.
- Zhang, R. (1997). Determination of Soil Sorptivity and Hydraulic Conductivity from the Disk Infiltrometer.
- Decagon Devices (2018). METER Environment Documentation.
- METER (2021). MINI DISK INFILTROMETER manual.
- Soilmoisture Equipment Corp. (2012, 2020). Guelph Permeameter operating instructions and K-sat calculator.