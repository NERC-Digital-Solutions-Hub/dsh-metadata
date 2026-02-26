# LANDWISE_detailed_survey_soil_data_2021_updated_v2

## Overview of the dataset
- Contains surface and sub-surface hydraulic and hydrological soil properties across the Thames catchment, UK.
- Measured variables include: soil bulk density, estimated soil porosity, volumetric soil moisture content, and soil moisture retention (to 100 cm suction); surface infiltration rates; and soil saturated hydraulic conductivity (Ks) at 25 cm and 45 cm depth where possible.
- Field-scale point data collected from 7 sites across three land-use/management groups, covering transects in trafficked areas, infield areas, and untrafficked margins.
- Data collected between April 2021 and October 2021 with repeats pre- and post-harvest.
- Collected by UKCEH as part of the LANDWISE project, which investigates natural land-based flood risk reduction; supported by NERC grant NE/R004668/1.

## Sampling design and field sites
- Seven fields selected from a Broad-scale LANDWISE survey for detailed investigation.
- Sites represent three geology/soil groupings: mudstone (slowly permeable loamy/clayey), chalk (free-draining loamy), limestone (shallow limestone), with soils/land-use varying by location.
- Fields are grouped into three sites by geology, enabling comparisons of land-use/management within similar geology.
- Sampling locations per field include:
  - TR: Trafficked areas (e.g., tramlines, animal tracks)
  - IN: Infield conditions
  - UN: Untrafficked field margins
- Location specifics and site tables (e.g., approximate Easting/Northing) are provided for five-field transect sites and field IDs (e.g., 18_6, 23_5, 26_1, 27_4, 27_2, 31_3, 44_1).

## Measurements and analytical methods
- Bulk density and inferred porosity:
  - Measured with volumetric soil cores; oven-dried at 105 °C.
  - Samples per field varied (e.g., 50 per field; 5 fields total for bulk density).
- Soil moisture content and porosity:
  - Volumetric water content (VWC) derived from oven-dried samples.
  - Porosity estimated using dry bulk density and a particle density of 2.65 g/cm3.
- Soil moisture retention (pF 0 to pF 2):
  - Conducted with a Sandbox; samples saturated, then subjected to suction steps (0, 0.4, 1, 1.5, 1.7, 1.8, 2 pF).
- Infiltration (unsaturated hydraulic conductivity, Kunsat):
  - Measured with Mini Disk Infiltrometers at site locations with various suction choices (commonly 2 cm; 0.5 cm for heavier clay soils).
  - Measurements taken across spring and pre-/post-harvest campaigns; at least 15 ml infiltration targeted per measurement.
- Saturated hydraulic conductivity (Ks, Kfs):
  - Measured at 25 cm and 45 cm depths using Guelph Permeameters.
  - Two-head method used (with measurements at two well-head heights) to improve accuracy; alternative single-head averages used if needed.
- Soil and vegetation root depth:
  - Measured with auger and tape measure; different sampling depths per site/type (arable, grassland, woodland).
- Spatial and temporal coverage:
  - Spring sampling (April 2021) and Autumn sampling (October 2021) for various measurements; pre-/post-harvest references included for some parameters.

## Data structure and format
- File: LANDWISE_detailed_survey_soil_data_2021_updated_v2.csv
- Structure: 1 CSV file with 70 columns and 380 rows.
- Key fields (examples, see Table 5 in the documentation):
  - Identifiers: ID_SiteNo, ID_FieldNo, ID_LocationCode, ID_SiteNo_FieldNo, ID_SiteNo_FieldNo_Loc
  - Location: OS_Grid_Sq, EastingBNG_PUBLIC, NorthingBNG_PUBLIC
  - Sampling metadata: Date_Sample_1, Time_Sample_1, Date_Sample_2, Time_Sample_2
  - Depths and horizons: Sample_1_Soil_Depth, Sample_1_Root_Depth, Sample_1_Horizon_1/2/3, Sample_2_Soil_Depth, etc.
  - Measurements: DryBulkDenMea, VolSoilMoistMea, EstPorosityDeriv, SMR_VWC_pF_0, SMR_VWC_pF_0.4, Infiltrometer_1_Kunsat, Guelph_Permeameter_Kfs, Guelph_Permeameter_Kfs_ms, Infiltration_1_Kunsat, etc.
  - Quality and notes: Infiltration_1_QC_Flag, Infiltration_2_QC_Flag, Guelph_Permeameter_QC_Flag, SMR_notes, Infiltrometer_1_notes, Guelph_Permeameter_notes
  - Data quality flags indicate missing values with NA
- Units and variable descriptions are provided in Table 5 of the documentation.

## Quality control and data quality
- A formal QC process flagged potentially spurious measurements or typos.
- Data entry was performed in Excel by the recorders and cross-checked by a second person; corrections applied as needed.
- Infiltration data QC flags (Infiltration_1_QC_Flag, Infiltration_2_QC_Flag):
  - Good: no issues
  - Invalid: physically implausible values; removed
  - A: unsteady infiltration rate
  - B: less than 15 ml infiltrated
  - C: unusually high Ks values (Ks at or beyond typical Kssat + 3 SD; may reflect novel soil state)
- Ks (Guelph permeameter) QC flags (Guelph_Permeameter_QC_Flag):
  - Good, Invalid (physically implausible values; removed)
- Notes indicate when double-head method (preferred) was used or when single-head measurements were averaged due to issues.
- Documentation and QC details available to support data reuse and reproducibility.

## Fieldwork, instrumentation and supporting information
- Field equipment:
  - Soil cores and oven-drying for bulk density
  - Eijkelkamp 07.53.SC sample rings and augers for soil sampling
  - Mini Disk Infiltrometers for infiltration
  - Guelph Permeameters for Ks
  - Eijkelkamp Sandbox for soil moisture retention
- Lab instruments and calibration:
  - Ovens (Heraeus Function Line) for drying
  - Balances (Precisa 2200C; Precisa 5000D) with regular calibration checks
  - Balances checked to 0.1 g precision; annual calibration
- Related datasets and references:
  - LANDWISE Broad-scale survey dataset: Soil near-surface properties, vegetation observations, land use and land management across Thames catchment (2018–2021)
  - Carsel & Parrish (1988) for soil water retention parameters
  - METER Mini Disk Infiltrometer manuals (METER, 2021)
  - SoilmMoisture Equipment Corp. Guelph Permeameter operating instructions (2012) and Ksat calculator (2020)
  - Zhang (1997) method for deriving Ks from disk infiltrometry

## Uses and potential data products
- Data supports cross-site comparisons of soil physical properties under different land uses and geological settings.
- Potential dashboards or self-serve tools for:
  - Spatial maps of Ks, Ks at depth, infiltration rates, VWC, porosity, and soil moisture retention across the seven fields
  - Time-series comparisons of spring vs autumn measurements and pre-/post-harvest conditions
  - Relationship analyses between land use/management practices and hydraulic properties
- Can be integrated with LANDWISE Broad-scale survey data to explore near-surface soil properties, vegetation, land use, and management across the Thames catchment.

## Related data and references
- LANDWISE Detailed Survey Supporting Documentation (Version 1.4)
- Carsel, R. F., & Parrish, R. S. (1988). Developing Joint Probability Distributions of Soil Water Retention Characteristics
- Decagon Devices (2018). METER Environment; Mini Disk Infiltrometer manual
- LANDWISE Broad-scale survey dataset (soil near-surface properties, vegetation, land use)
- Soilmoisture Equipment Corp. (2012, 2020). Guelph Permeameter resources
- Zhang, R. (1997). Determination of Soil Sorptivity and Hydraulic Conductivity from the Disk Infiltrometer