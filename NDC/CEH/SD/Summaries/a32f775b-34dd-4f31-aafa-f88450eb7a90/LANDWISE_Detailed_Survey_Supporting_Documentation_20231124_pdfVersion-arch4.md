# LANDWISE detailed survey soil data 2021 updated v2

## Overview and purpose
- Dataset from the LANDWISE project within the Thames catchment to characterize field-scale soil properties under different land-management practices and to inform Natural Flood Management (NFM) assessments.
- Aims to capture how natural land-based measures influence flood risk by comparing field-scale heterogeneity across land uses (permanent grassland, arable with rotation, woodland) and geology (mudstone, chalk, limestone).

## Study design and locations
- Seven fields selected from a Broad-scale survey, organized into three sites by geology: Mudstone, Chalk, Limestone.
- Land uses and management varied: permanent grassland, arable with rotations, unmanaged woodland (deer grazing in some cases).
- Detailed survey fields sampled at two periods in 2021: Spring (April) and Autumn (October), with repeats around harvest.
- Site/field identifiers and approximate locations provided; sampling transects across trafficked (TR), infield (IN), and untrafficked (UN) margins to capture spatial heterogeneity.

## Measurements and variables
- Soil properties (bulk density, inferred porosity) and volumetric water content (VWC) at multiple depths.
- Soil moisture retention (pF 0–2) measured on a subset of limestone fields.
- Saturated hydraulic conductivity (Ksat, Kfs) measured at 25 cm and 45 cm depths using Guelph Permeameters.
- Infiltration rate (unsaturated hydraulic conductivity, Kunsat) measured with Mini Disk Infiltrometers at various suctions (0.5–6.0 cm).
- Soil and vegetation root depth; maximum soil depths and horizon depths recorded.
- Sampling locations within fields identified as TR1–TR5, IN1–IN5, UN1–UN5 per field.

## Data collection and methods
- Field sampling tools: Eijkelkamp sample rings with closed ring holders, Edelman and Stony augers.
- Bulk density and porosity: volumetric cores and oven-drying (105°C) with porosity inferred from bulk density.
- VWC: oven-dried samples; porosity calculations assume density of 2.65 g/cm3 for mineral soils.
- Soil moisture retention: Sandbox with pF values (0–2) using deionised water; saturation achieved before measurements; careful temperature and evaporation controls.
- Infiltration: Mini Disk Infiltrometers; measurements recorded at set intervals to derive unsaturated conductivity via Zhang (1997) method and Carsel & Parrish (1988) soil-water retention parameters.
- Saturated conductivity: Guelph Permeameter (two-head method preferred for accuracy); 25 cm and 45 cm depths with careful well preparation to avoid disturbance.

## Data structure and content
- One CSV file: LANDWISE_detailed_survey_soil_data_2021_updated_v2
- Size: 70 columns, 380 rows
- Key identifiers: ID_SiteNo, ID_FieldNo, ID_LocationCode, ID_SiteNo_FieldNo, ID_SiteNo_FieldNo_Loc
- Location descriptors: LocationTypeObs (TR, IN, UN categories); OS_Grid_Sq; EastingBNG_PUBLIC; NorthingBNG_PUBLIC
- Temporal and depth fields: Date_Sample_1 (Spring), Date_Sample_2 (Autumn), Sample_1_Soil_Depth, Sample_2_Soil_Depth, horizons and depths per location
- Measured variables include Kunsat, Kunsat_ms, Kfs, Guelph_Permeameter_Kfs, VWC (various pF values), soil dry bulk density, estimated porosity, infiltration measurements, and root depth
- Missing values represented as NA

## Quality control
- Data entry QC: cross-checked by a second person to correct typos.
- Field and lab data QC: infiltration flags (Infiltration_1_QC_Flag, Infiltration_2_QC_Flag) with codes:
  - Good, Invalid, A, B, C (e.g., invalid values, insufficient infiltration, unrealistically high Ks)
- Saturated conductivity QC: Guelph_Permeameter_QC_Flag with codes:
  - Good, Invalid
- Notes explain when double-head permeameter measurements were used or when single-head measurements were averaged due to inadmissible double-head results
- Some measurements removed or flagged as invalid based on QC

## Fieldwork and instrumentation details
- In-field and lab equipment:
  - Mini Disk Infiltrometers for unsaturated infiltration
  - Guelph Permeameter for saturated hydraulic conductivity
  - Eijkelkamp Sandbox for soil moisture retention
  - Eijkelkamp 07.53.SC sample rings with Edelman/Stony augers for soil sampling
  - Ovens (105°C) and precision balances for gravimetric analysis
- Instrument calibration and traceability: balances calibrated to 0.1 g; annual lab calibration; detailed procedural notes provided for measurement heights, suction settings, and measurement timing

## Data usage and context
- Data linked to the broader LANDWISE Broad-scale survey dataset for Thames catchment (soil properties, vegetation observations, land use, and land management information across 1800 locations, 2018–2021).
- Dataset supports analysis of field-scale soil property variability under different land management to inform flood risk reduction strategies and data-driven decision-making in data-led organizations.

## Practical considerations for data leaders
- Comprehensive metadata and QC flags enable robust data quality assessment and integration with other data layers.
- Heterogeneity across land uses and geology provides insights into data gaps and the need for standardized metadata and harmonized units when expanding networks.
- The dataset emphasizes repeat measurements across seasons and transects (TR/IN/UN) to capture temporal and spatial variability, informing co-ownership of data products with policy colleagues and partners.
- Useful for prioritizing data collection efforts in regions with scarce data or high variability in soil hydraulic properties.