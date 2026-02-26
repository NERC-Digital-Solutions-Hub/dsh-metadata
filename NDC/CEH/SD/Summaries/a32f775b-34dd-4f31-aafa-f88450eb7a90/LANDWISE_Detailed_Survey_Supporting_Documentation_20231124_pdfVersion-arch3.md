LANDWISE_detailed_survey_soil_data_2021_updated_v2

## Overview and purpose
- Detailed field-scale soil dataset from the Thames catchment, covering surface and sub-surface hydraulic and hydrological properties.
- Measurements include bulk density, inferred porosity, volumetric soil moisture content, soil moisture retention (to pF 2), surface infiltration rates, and saturated hydraulic conductivity (Ksat) at 25 cm and 45 cm depth.
- Data collected across 7 fields (three land-use/management groups) and 3 geological soil-type sites (mudstone, chalk, limestone), with sampling in trafficked areas, infield areas, and untrafficked margins.
- Sampling occurred April–October 2021, with repeats pre- and post-harvest; part of the LANDWISE project within NERC’s Natural Flood Management Research Programme.

## Study design and context
- A detailed follow-up to a Broad-scale LANDWISE survey to characterise field-scale heterogeneity under different Natural Flood Management (NFM) measures.
- Seven fields were selected to represent soil/types and land-use/management, enabling comparisons across geology and management practices (e.g., grassland vs arable, conventional vs controlled traffic, herbal ley rotations).
- Site locations and field IDs are provided, with a structured sampling plan across three site types (Mudstone, Chalk, Limestone) and corresponding land uses.

## Measurements and key variables
- Bulk density and inferred porosity (depth-resolved, via volumetric cores and oven-drying).
- Volumetric soil moisture content and soil moisture retention (pF 0–2) using sandbox analysis.
- Saturated hydraulic conductivity (Ksat) measured at 25 cm and 45 cm depth with Guelph Permeameters.
- Infiltration measurements (unsaturated hydraulic conductivity, Kunsat) via Mini Disk Infiltrometers across transects, trafficking zones, infield areas, and margins.
- Soil and vegetation root depth (via auger and tape measure) across field types.
- Measurements captured across multiple periods within the annual cycle, with spring (April 2021) and autumn (October 2021) campaigns; repeated sampling at arable fields around harvest.

## Sampling strategy and locations
- Field sampling along transects at three location types within fields: TR (trafficked), IN (infield), UN (untrafficked margins).
- 5 IN, 5 TR, and 5 UN sampling points per field, totaling 15 locations per field for certain measurements; 7 fields total.
- Detailed site layouts and sampling locations are described, with mapping to field IDs and site geology.
- Table mappings outline field IDs, land use, management, and geology per site.

## Analytical methods and field procedures
- Soil samples collected with Eijkelkamp kit and augers; samples sealed, refrigerated, and analyzed in UKCEH laboratories.
- Dry bulk density and volumetric moisture via oven-drying at 105°C; porosity inferred from bulk density.
- Soil moisture retention determined with a Sandbox across a range of suctions (pF 0–2) using deionised water and a controlled desaturation protocol.
- Infiltration measurements using Mini Disk Infiltrometers with appropriate suction (mostly 2 cm; 0.5 cm for heavier clays); level surface preparation and contact ensured; water volume recorded over time; cumulative infiltration used to derive unsaturated conductivity via Zhang (1997) method.
- Saturated hydraulic conductivity measured with a two-head Guelph Permeameter method; two well-head heights used to improve accuracy; Kfs calculated via an established calculator incorporating reservoir geometry, head height, and measured flow.
- Field and lab data entered into Excel; particle/soil physics parameters (e.g., van Genuchten) sourced from Carsel & Parrish (1988) for analysis.

## Quality control and data quality
- Post-collection QC to flag potentially spurious measurements; data entry cross-checked by a second person.
- Infiltration QC flags: Good, Invalid (physically implausible), A (unsteady infiltration), B (<15 ml infiltrated), C (unusually high K values; may reflect novel soil states).
- Guelph permeameter QC flags: Good, Invalid (physically implausible values or out-of-range alpha).
- Notes indicate preferred use of the double-head Guelph method when valid; otherwise single-head measurements were used and averaged.
- Missing or invalid measurements stored as NA with notes in accompanying fields.

## Data structure and accessibility
- One CSV file: LANDWISE_detailed_survey_soil_data_2021_updated_v2.
- Contains 70 columns and 380 rows; column headers and units are defined in the accompanying dataset documentation.
- Data fields include site and field identifiers, location codes, sampling locations (TR/IN/UN), grid references, sampling dates/times, depths, horizons, and all measured variables (bulk density, porosity, VWC, soil moisture retention, Kunsat, Ksat, root depth, etc.).
- NA values represent missing or invalid measurements; detailed QC flags and notes accompany measurement columns.

## Fieldwork and instrumentation
- Equipment used: Eijkelkamp soil sampling kit with augers; oven-drying equipment (105°C); sandbox for soil moisture retention; Mini Disk Infiltrometers for infiltration; Guelph Permeameter for saturated conductivity.
- Laboratories and instruments calibrated and validated; balances used with traceable accuracy; periodic calibration and documentation maintained.

## Context, provenance, and related datasets
- Dataset linked to LANDWISE Broad-scale survey: “Soil near-surface properties, vegetation observations, land use and land management information for 1800 locations across the Thames catchment, UK, 2018-2021.”
- References include Carsel & Parrish (1988), Zhang (1997), and Soilmose/Decagon/METER manuals for instrumentation and calculations.

## Relevance for monitoring frameworks
- Provides standardized, provenance-rich measures of soil hydraulic properties and infiltration across multiple land uses and geologies, enabling evaluation of natural flood management strategies and land management impacts on soil porosity, moisture dynamics, and hydraulic conductivity.
- Rich metadata and QC framework illustrate governance practices around data quality, traceability, and transparency—critical for policy scrutiny and future decision-making.
- Identifies operational data gaps and practical challenges (e.g., field-level data completeness, variable measurement success across soils, and data sharing constraints) that may inform governance and data-management enhancements in monitoring programs.