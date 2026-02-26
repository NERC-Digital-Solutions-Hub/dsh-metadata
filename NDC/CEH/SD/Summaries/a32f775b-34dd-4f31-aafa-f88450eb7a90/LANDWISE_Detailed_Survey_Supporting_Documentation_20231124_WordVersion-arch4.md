# LANDWISE Detailed Survey Supporting Documentation (Version 1.4)

- The dataset provides surface and sub-surface hydraulic and hydrological soil properties for seven fields across the Thames catchment, spanning three geology/soil groups (mudstone, chalk, limestone) and multiple land uses (permanent grassland, arable with and without grass, woodland). Key measured properties include soil bulk density, porosity, volumetric soil moisture content, soil moisture retention to 100 cm suction, surface infiltration rates, and saturated hydraulic conductivity at 25 cm and 45 cm depth.
- Data were collected April–October 2021 as part of the LANDWISE project, which investigates natural flood management (NFM) efficacy. The work contributes to a broader LANDWISE effort across the Thames catchment (LANDWISE Broad-scale survey and other detailed surveys).

## Data Content and Structure

- File: LANDWISE_detailed_survey_soil_data_2021_updated_v2
- Size: 70 columns, 380 rows
- Content: Site/field/location identifiers, coordinates (OS grid, Easting/Northing), sampling dates, depths, root depths, horizons, and a comprehensive set of measured and derived soil properties (bulk density, porosity, volumetric water content, porosity estimates, soil moisture retention, saturated and unsaturated hydraulic conductivity, infiltration rates, soil and vegetation root depth).
- Data lineage: Linked to LANDWISE Broad-scale survey data for Thames catchment; NA values indicate missing measurements or invalid/omitted data.

## Research Design

- Objective: Characterize field-scale heterogeneity under different Natural Flood Management (NFM) measures.
- Sites: Seven fields selected from a prior Broad-scale survey, grouped into three geology/soil types (mudstone, carbonate/chalk, limestone). Each site enables comparison across land-use types or management practices.
- Sampling strategy includes field-scale transects across three location types (trafficked, infield, untrafficked margins) to capture spatial variability.

## Sampling Strategy and Locations

- Sampling across multiple periods within a year: Spring (April) and Autumn (October) campaigns.
- Field locations: 18_6, 44_1, 26_1, 23_5, 31_3, 27_2, 27_4, with three sites representing mudstone, chalk, and limestone geology.
- Sampling locations within fields: 15 per field (TR = trafficked areas, IN = infield, UN = untrafficked margins). Five sublocations per category to cover spatial variation.

## Soil Sampling Methods

- Tools: Eijkelkamp 07.53.SC sample ring kit with closed ring, Edelman and Stony augers.
- Handling: Samples sealed, refrigerated immediately; laboratory analyses performed under controlled conditions.
- Analyses: Oven-drying to determine bulk density and infer porosity; Sandbox method for moisture retention; porosity estimated from bulk density.

## Field Measurements and Protocols

- Infiltration (unsaturated hydraulic conductivity Kunsat):
  - Tool: Mini Disk Infiltrometers.
  - Procedure: Clear vegetation, ensure level surface, apply suction (typically 2 cm; 0.5 cm for heavy clay), measure cumulative infiltration over time, calculate Kunsat using Zhang 1997 method with van Genuchten parameters from Carsel & Parrish (1988).
  - Locations: TR, IN, and UN sites as per Table 4 mapping.
  - Data handling: At least 15 ml infiltration targeted; measurements may be flagged if below target or data quality issues arise.
- Saturated hydraulic conductivity (Kfs):
  - Tool: Guelph Permeameter (two-head method preferred for accuracy).
  - Depths: 25 cm and 45 cm.
  - Procedure: Excavated wells, standardized geometry, tests at offset locations to avoid disturbance; use two head heights (commonly 5–10 cm; sometimes 10–15 cm or 15–20 cm for slower soils); data processed with external calculator to derive Kfs.
  - QC: Flags for quality (Good/Invalid) and notes on head-method usage (double-head preferred; fallback to single-head with averaging when needed).
- Soil moisture retention:
  - Tool: Sandbox with pF pressure steps (0 to 2, e.g., pF 0, 0.4, 1, 1.5, 1.7, 1.8, 2).
  - Procedure: Saturation until constant mass, minimize evaporation, monitor until equilibrium; use copper sulfate to prevent algal growth.
  - Outputs: Volumetric water contents at target suctions, mu marked as SMR_VWC_pF_x values.

## Data Quality and QC

- Processes: Independent data entry verification to minimize typos; subsequent QC review.
- Infiltration QC flags (Infiltration_1_QC_Flag, Infiltration_2_QC_Flag):
  - Good: no issues
  - Invalid: physically implausible values; removed
  - A: unsteady infiltration rate
  - B: less than 15 ml infiltrated
  - C: unusually high K values (within context of soil state; may indicate novel conditions)
- Saturated conductivity QC flags (Guelph_Permeameter_QC_Flag):
  - Good; Invalid (negative or alpha outside 0.01–0.5 cm-1) and removal
- Notes explain method choices (double-head vs. single-head for Kfs) and preference, with fallback procedures when data are inadmissible.

## Fieldwork, Instrumentation, and Calibration

- Field equipment:
  - Mini Disk Infiltrometers for infiltration
  - Guelph Permeameters for Kfs
  - Eijkelkamp Sandbox for moisture retention
  - Oven drying for VWC and bulk density
- Laboratory equipment:
  - Heraeus 105 °C ovens, Precisa balances (0.1 g precision), calibration checks and annual re-calibration
- Documentation: All field data and lab measurements recorded in Excel spreadsheets; backups and QC processes described; data processing references include Zhang (1997) and Carsel & Parrish (1988).

## Field Notes and Metadata

- Spatial metadata: OS grid references and coordinates (Easting/Northing) for each site/field; field sampling locations mapped along transects.
- Temporal metadata: Spring and Autumn campaigns with explicit dates; some measurements have NA for non-applicable periods.
- Data are linked to broader LANDWISE datasets and related documentation.

## Data Structure and Accessibility

- Primary dataset: LANDWISE_detailed_survey_soil_data_2021_updated_v2.csv
- Columns: 70 variables including identifiers, location codes, sampling dates, depths, and a comprehensive suite of soil properties and QC fields.
- NA values indicate missing or inapplicable data.
- Related documentation and references support data provenance and methodology.

## Practical Considerations for Data Leaders

- Data completeness and provenance:
  - Longitudinal design across two seasons and multiple site types enables cross-site comparability and temporal trend analyses.
  - Clear lineage to LANDWISE Broad-scale survey data enhances interoperability and networked data use.
- Metadata and discoverability:
  - Rich metadata on site type, geology, land use, management, and sampling layout supports reuse and integration with other datasets.
  - QC flags and methodological notes improve data quality assessment for downstream users.
- Data gaps and standards:
  - Some measurements are NA for certain campaigns or locations; users should account for missing data in analyses.
  - Documentation references established analytical methods; alignment with Carsel & Parrish (1988) and Zhang (1997) supports standardization and cross-study comparability.
- Governance and reuse:
  - Data are collected under the LANDWISE program, with clear instrumentation, procedures, and QC protocols that support reproducibility and auditability.
  - The dataset is well-suited for informing flood risk reduction strategies, soil hydraulic property modeling, and cross-site comparisons within networked water-related data platforms.

## References

- Carsel, R. F., & Parrish, R. S. (1988). Developing Joint Probability Distributions of Soil Water Retention Characteristics. Water Resources Research, 24(5), 755-769.
- Decagon Devices (2018). METER Environment. 
- METER (2021). MINI DISK INFILTROMETER Manual.
- Soilmoisture Equipment Corp. (2012). Guelph Permeameter - Operating Instructions.
- Soilmoisture Equipment Corp. (2020). Guelph Permeameter K-sat Calculator.
- Zhang, R. (1997). Determination of Soil Sorptivity and Hydraulic Conductivity from the Disk Infiltrometer. Soil Science Society of America Journal, 61(4), 1024-1030.