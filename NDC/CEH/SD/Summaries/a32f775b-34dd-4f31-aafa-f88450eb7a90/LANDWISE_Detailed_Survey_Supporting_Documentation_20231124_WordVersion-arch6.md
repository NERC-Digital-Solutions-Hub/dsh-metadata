# LANDWISE Detailed Survey Supporting Documentation (Version 1.4)

- A detailed soil survey dataset within the Thames catchment, focusing on surface and sub-surface hydraulic and hydrological properties.
- Includes bulk density, inferred porosity, volumetric soil moisture content, and soil moisture retention (to pF 2, ~100 cm suction); surface infiltration rates; and saturated hydraulic conductivity at 25 cm and 45 cm depths.
- Field-scale point measurements collected across 7 fields in 3 sites with contrasting geology and land-use (mudstone, chalk, limestone) and management (grassland, arable, woodland).

## Data Scope and Structure

- One CSV file: LANDWISE_detailed_survey_soil_data_2021_updated_v2
- 70 columns and 380 rows
- Includes: site/field/location identifiers, Ordnance Grid coordinates (Easting/Northing in meters), sampling dates (Spring 2021 and Autumn 2021), depth information, and a broad suite of soil properties and measurements
- NA values denote missing measurements or data not collected
- Table 5 (in the documentation) provides full descriptions and units for each column

## Sampling Design and Field Locations

- Seven fields selected from the LANDWISE Broad-scale survey for detailed study
- Three sites by geology: Mudstone, Chalk (carbonate), Limestone
- Land-use/management contrasts within sites enable comparisons of grassland, arable, and woodland
- Sampling locations within fields categorized as:
  - TR: Trafficked areas (e.g., tramlines, animal tracks)
  - IN: Infield conditions
  - UN: Untrafficked field margins
- Transects across fields with five locations per category, enabling field-scale heterogeneity assessment
- Spatial references include approximate site and field IDs and Os Grid coordinates for anonymity

## Measurements and Methods

- Bulk density and inferred porosity (depth-resolved) via volumetric cores and oven drying
- Volumetric soil moisture content (VWC) from oven-dried samples
- Soil porosity estimated from bulk density using mineral density convention
- Soil moisture retention (pF 0–2) using Eijkelkamp Sandbox; suction steps include pF 0, 0.4, 1, 1.5, 1.7, 1.8, 2
- Infiltration/unsaturated hydraulic conductivity (Kunsat) measured with Mini Disk Infiltrometers across site types and campaigns
- Saturated hydraulic conductivity (Kfs) measured at 25 cm and 45 cm depths using Guelph Permeameters (two-head method preferred)
- Root depth for soil and vegetation measured with auger and tape measure
- Measurements taken across Spring (April 2021) and Autumn (October 2021) campaigns
- Calculations and derivations:
  - Kunsat derived from cumulative infiltration using Zhang (1997) method with van Genuchten parameters (Carsel & Parrish, 1988)
  - Kfs calculated from Guelph permeameter data using standard calculator (Soilmoisture Equipment Corp., 2020)

## Data Fields and Units

- Core identifiers: ID_SiteNo, ID_FieldNo, ID_LocationCode, ID_SiteNo_FieldNo, ID_SiteNo_FieldNo_Loc
- Location metadata: OS_Grid_Sq, EastingBNG_PUBLIC (m), NorthingBNG_PUBLIC (m)
- Sampling metadata: Date_Sample_1/Date_Sample_2, Time_Sample_1/Time_Sample_2, Sample_1/Sample_2_Soil_Depth and associated horizon depths
- Site/field types: LocationTypeObs (e.g., TR, IN, UN)
- Measured variables (examples): Bulk density, Porosity, Volumetric Water Content (VWC) at spring/autumn samples, Estimated porosity, Kunsat (cm/s and m/s), Infiltration_QC flags, Guelph_Kfs (cm/s and m/s), Guelph_Kfs_QC_Flag, Infiltration_1/2 (pre/post-harvest) values and QC flags, Soil moisture retention values (pF steps), Infiltrometer notes, Root depth
- Units are provided per column in Table 5; many fields are NA where not applicable

## Quality Control and Data Cleaning

- Field and lab data entered in Excel and subjected to cross-checking by a second person
- Infiltration measurements QC:
  - Good, Invalid (physically implausible values; removed), A (unsteady infiltration), B (less than 15 ml infiltrated), C (unusually high K values; may reflect novel soil state)
- Saturated hydraulic conductivity QC:
  - Good, Invalid (out-of-range or implausible values; removed)
- Guelph permeameter notes indicate whether double-head method or averaged single-head measurements were used
- Data flagged for measurement timing or QC concerns; NA used for missing or invalid data

## Data Access and Format

- Primary dataset: LANDWISE_detailed_survey_soil_data_2021_updated_v2.csv
- Structure: 70 columns, 380 rows
- NA denotes missing data; detailed column definitions and units are in the accompanying documentation (Table 5)
- Data can support comparisons of field-scale soil properties across land-use types and management practices, and integration with broader LANDWISE datasets

## Instrumentation and Laboratory Methods

- Field equipment:
  - Eijkelkamp 07.53.SC sample rings with closed ring holder
  - Edelman and Stony augers for sampling
  - Mini Disk Infiltrometers for infiltration measurements
  - Guelph Permeameters for Kfs measurements
- Laboratory equipment:
  - Ovens (Heraeus Function Line) for drying soils
  - Precision balances (Precisa 2200C; Precisa 5000D) for mass measurements
  - Sandbox apparatus for soil moisture retention analyses
- Calibrations and references:
  - Van Genuchten parameterization from Carsel & Parrish (1988)
  - Kunsat calculations following Zhang (1997)
  - Guelph Kfs calculator and related manuals (Soilmoisture Equipment Corp., 2012, 2020)
  - Infiltration methodology per METER Mini Disk Infiltrometer manual (2021)

## Related Work and References

- LANDWISE Detailed Survey Supporting Documentation (Version 1.4)
- Carsel, R. F., & Parrish, R. S. (1988). Soil water retention characteristics
- Zhang, R. (1997). Disk infiltrometer analysis
- Decagon/METER instrumentation manuals for data processing and QC
- LANDWISE Broad-scale survey context: soil near-surface properties and land-use information across the Thames catchment (2018–2021)

- This dataset supports analyses of field-scale hydrological properties under varied land management as part of the LANDWISE project, contributing to understanding natural flood management measures.