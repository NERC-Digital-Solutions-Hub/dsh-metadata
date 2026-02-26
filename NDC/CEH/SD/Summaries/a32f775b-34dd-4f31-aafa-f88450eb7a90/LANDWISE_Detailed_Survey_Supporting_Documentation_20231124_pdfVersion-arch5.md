# LANDWISE_detailed_survey_soil_data_2021_updated_v2

## Overview
- A detailed soil dataset from the LANDWISE project focused on field-scale hydraulic and hydrological properties across the Thames catchment.
- Measured variables include: soil bulk density, estimated soil porosity, volumetric soil moisture content, soil moisture retention (to pF 2), surface infiltration rates, and saturated hydraulic conductivity (Ksat) at 25 cm and 45 cm depth where practical.
- Data were collected from 7 fields across 3 sites with varied geology and land use (mudstone, carbonate/chalk, limestone) to compare grassland, arable, and woodland management.
- Sampling occurred across transect types (trafficked, infield, untrafficked margins) in spring 2021 and autumn 2021, with repeats around harvest.

## Data Content and Structure
- Single CSV file: LANDWISE_detailed_survey_soil_data_2021_updated_v2
- Size: 70 columns, 380 rows
- Core metadata fields:
  - Identifiers: ID_SiteNo, ID_FieldNo, ID_LocationCode, ID_SiteNo_FieldNo, ID_SiteNo_FieldNo_Loc
  - Location descriptors: LocationTypeObs (TR, IN, UN), OS_Grid_Sq, EastingBNG_PUBLIC, NorthingBNG_PUBLIC
  - Temporal fields: Date_Sample_1 (Spring), Time_Sample_1, Date_Sample_2 (Autumn), Time_Sample_2
- Measurement-related fields cover:
  - Bulk density and inferred porosity by depth
  - Volumetric soil moisture content (VWC)
  - Estimated soil porosity
  - Soil moisture retention (pF range)
  - Saturated hydraulic conductivity (Kfs) via Guelph Permeameter at depth
  - Infiltration-related metrics (Kunsat) from Mini Disk Infiltrometer
  - Soil and vegetation root depth
  - Depths, horizons, and horizon depths per sampling location
- Units and data types are described in Table 5 of the documentation; NA denotes missing values.

## Sampling Strategy and Site Description
- Seven fields selected across three geology/soil groups:
  - Mudstone: slowly permeable loamy/clayey soils (fields 18_6)
  - Chalk: free-draining loamy soils (field 26_1; 31_3)
  - Limestone: shallow limestone soils (fields 27_2, 27_4, 31_3)
- Land use categories include permanent grassland, arable, and unmanaged woodland to enable comparisons of land-use scenarios.
- Sampling design captures spatial heterogeneity by location type:
  - TR = trafficked areas (tramlines, tracks)
  - IN = infield areas
  - UN = untrafficked field margins
- Field sampling times:
  - Spring (April 2021)
  - Autumn (October 2021)
- Sampling intensity per field/location as per detailed tables (sites organized to enable comparisons across geology and management).

## Measurements and Analytical Methods
- Infiltration (Kunsat):
  - Instrument: Mini Disk Infiltrometer
  - Suction rates: typically 2 cm; 0.5 cm for heavier clay soils
  - Procedure: level surfaces, vegetation cleared, measure cumulative infiltration to derive Kunsat using Zhang (1997) method with van Genuchten parameters (Carsel & Parrish, 1988)
  - Data entry in Excel, with QC flags indicating measurement quality
- Saturated hydraulic conductivity (Kfs):
  - Instrument: Guelph Permeameter
  - Depths: 25 cm and 45 cm
  - Method: two-head measurement for higher accuracy; well holes prepared with Edelman and sizing auger
  - Calculations follow standard Kfs formula (via Excel calculator)
- Volumetric water content (VWC) and dry bulk density:
  - VWC derived from oven-dried mass and sample volumes
  - Dry bulk density = dry soil mass / sample volume
  - Porosity estimated from bulk density assuming particle density of 2.65 g/cm3
- Soil moisture retention:
  - Instrument: Eijkelkamp Sandbox
  - Range: pF 0 to 2 (0–100 cm suction)
  - Process includes saturation to constant mass, controlled evaporation, and daily weighing until equilibrium
- Soil and vegetation root depth:
  - Method: Auger and tape measure
- Additional fields include horizon depths, horizons, sampling depths, and related notes.

## Data Quality Control and Processing
- QC workflow:
  - Field and lab data entered by the recorder; a second person audits for transcription errors
  - Infiltration QC flags:
    - Good, Invalid (physically implausible), A (unsteady), B (<15 ml infiltrated), C (unusually high K)
  - Guelph QC flags:
    - Good, Invalid; notes indicate whether double-head or single-head method was used; double-head preferred
- Handling of data:
  - NA values denote missing or invalid measurements
  - Some measurements with insufficient infiltration volume or poor data quality are flagged or removed
- Data processing references:
  - Zhang (1997) for infiltration, Carsel & Parrish (1988) for soil parameter priors
  - Kfs and Kunsat derived via established field/calculation procedures and instrumental calculators

## Fieldwork and Instrumentation
- Field equipment:
  - Eijkelkamp 07.53.SC sampling kit (core rings, closed ring holder) and augers (Edelman, Stony)
  - Mini Disk Infiltrometers (for infiltration) and Guelph Permeameter (for Kfs)
  - Sandbox for moisture retention analyses
- Laboratory equipment:
  - Ovens (Heraeus 105 °C), precision balances (Precisa 2200C, Precisa 5000D)
  - Field and lab calibration procedures documented; equipment calibrated and traceable

## Data Structure and Documentation
- File: LANDWISE_detailed_survey_soil_data_2021_updated_v2.csv
- Structure: 70 columns, 380 rows
- Column taxonomy and meanings are aligned with Table 5 (Nature and Units of recorded values)
- Field notes and QC flags provide guidance on data quality and data usability
- Data are part of the LANDWISE Broadscale survey dataset relating to soil properties, vegetation observations, land use, and land management ( Thames catchment, 2018–2021)

## Provenance, Usage, and Related Resources
- Project context: LANDWISE Detailed Survey supports understanding how natural land-based measures affect flood risk and soil properties
- Related datasets: Broad-scale LANDWISE survey dataset on Thames catchment (Soil near-surface properties, vegetation observations, land use and land management information for 1800 locations, 2018–2021)
- References and tools cited in the documentation (Carsel & Parrish 1988; Zhang 1997; Decagon METER resources; Guelph permeameter manuals; LANDWISE Supporting Documentation)

## Considerations for Data Stewards
- Ensure discoverability and reuse through comprehensive metadata (identifiers, location, dates, site characteristics, measurement methods, units)
- Preserve data lineage: tie measurements to specific sites/fields/locations, sampling dates, and methods
- Maintain QC flags and notes to aid users in assessing data quality and suitability for analysis
- Validate licensing and access rights; provide clear citation guidance and link to related LANDWISE documentation
- Recognize potential limitations in dataset scope (seven fields across three geology groups, with variable sampling counts per field) when integrating with broader analyses
- Maintain instrument-specific calibration records and methodological references for reproducibility