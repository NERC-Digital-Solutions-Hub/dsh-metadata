# LANDWISE Detailed Survey Supporting Documentation (Version 1.4)

## Overview and purpose
- A detailed soil dataset from the Thames catchment capturing surface and sub-surface hydraulic and hydrological properties.
- Measurements include: soil bulk density, inferred porosity, volumetric soil moisture content (VWC), and soil moisture retention (to pF 2); surface infiltration rates; saturated hydraulic conductivity (Ksat) at 25 cm and 45 cm depth.
- Field-scale, site-specific data collected across seven fields representing three land-use/management groups, intended to help evaluate natural flood management measures and inform land-management decisions.

## Project context and study design
- Collected by UKCEH as part of LANDWISE, within the Natural Flood Management Research Programme funded by the Natural Environment Research Council (NERC NE/R004668/1).
- Three geological/geographical site types: mudstone, chalk (carbonate), and limestone.
- Land-use groups: permanent grassland, arable with varying practices, and unmanaged woodland.
- Seven fields sampled in detail following a previous broad-scale soil property survey; field sites allow comparisons between grassland and woodland and between different arable management strategies.

## Sampling strategy and site details
- Sampling along transects within fields at three location types: TR (trafficked areas like tramlines), IN (infield), UN (untrafficked field margins).
- Five IN, five TR, and five UN sampling locations per field, with 15 locations per field total; samples collected spring 2021 (April) and post-harvest (October 2021).
- Sites organized into three locations per site-type group, with three geology/soil types (mudstone, chalk, limestone) across fields.
- Table-level site descriptors include land use, soil type, and management (e.g., conventional traffic, controlled traffic, herbal ley, unmanaged grazing).

## Measurements, techniques, and timing
- Bulk density and inferred porosity: volumetric cores and oven drying (105°C); depth-resolved measurements; samples per field and number of fields specified by site type (arable or woodland/grassland).
- Soil moisture retention (pF 0–2): sandbox method with deionised water, saturating samples and applying suction steps (pF values 0, 0.4, 1, 1.5, 1.7, 1.8, 2); measurements taken spring and autumn as part of seasonal cycle.
- Saturated hydraulic conductivity (Ksat): measured at 25 cm and 45 cm depths using Guelph Permeameter; two-head method preferred; multiple well-head heights used to optimize accuracy depending on soil type.
- Infiltration (unsaturated hydraulic conductivity): Mini Disk Infiltrometers across field sites; infiltration measured over time to derive Kunsat; field suction typically 2 cm (0.5 cm for heavy clay soils).
- Soil and vegetation root depth: auger and tape measure across site types (arable, grassland, woodland).
- Data capture: field measurements recorded in Excel spreadsheets; post-processing to derive Kunsat and VWC values.

## Data structure and content
- Dataset filename: LANDWISE_detailed_survey_soil_data_2021_updated_v2
- Format: CSV with 70 columns and 380 rows.
- Core variables include: IDs (site, field, location), LocationTypeObs, OS grid references, date/time stamps for spring and autumn campaigns, sample depths and horizons, root depths, bulk density, porosity estimates, VWC, moisture retention values, infiltration results (Kunsat), Kfs (saturated hydraulic conductivity), and corresponding QC flags and notes.
- Units and metadata documented; missing values represented as NA. Descriptive column details are provided in the Supporting Documentation.

## Quality control and data governance
- Data entry underwent double-entry checks to catch typographical errors.
- Infiltration QC flags:
  - Good: no issues
  - Invalid: physically implausible values (removed)
  - A: unsteady infiltration rate over time
  - B: less than 15 ml infiltrated (minimum for robust calculation)
  - C: unusually high K values (within context of soil state)
- Saturated hydraulic conductivity QC flags:
  - Good or Invalid (negative values or implausible alpha values removed)
- Guelph permeameter notes indicate preference for double-head measurements; if issues arose, single-head measurements were used and averaged.
- Data accessibility: dataset is a single CSV with accompanying notes; metadata and QC flags enhance traceability and data quality.

## Fieldwork and instrumentation
- Soil sampling: Eijkelkamp 07.53.SC kit with closed-ring holder; Edelman and Stony augers.
- Laboratory analysis: oven drying (105°C) for bulk density and moisture content; sandbox for moisture retention; Guelph Permeameter for Ksat; Mini Disk Infiltrometers for infiltration.
- Calibration and quality checks: balances calibrated to 0.1 g; annual calibration of lab balances; instruments and methods referenced to standard manuals and literature (Carsel & Parrish 1988; Zhang 1997; METER 2021; Soilmoiisture Equipment Corp. 2012/2020).

## Relevance to monitoring frameworks and environmental health monitoring
- Provides a comprehensive, field-scale dataset of soil hydraulic properties across multiple land uses and soil types, enabling monitoring of how land management and moisture regimes influence infiltration, soil moisture retention, and groundwater recharge risk.
- The transect-based design and inclusion of trafficked vs. untrafficked areas capture spatial heterogeneity critical for robust monitoring indicators.
- Clear data governance features (metadata, QA/QC flags, and documented instrumentation) support transparency, reproducibility, and comparability with other monitoring frameworks.
- The dataset supports evaluating natural flood management (NFM) outcomes by linking soil hydraulic properties to flood risk reduction scenarios across different management practices.

## Access, limitations, and related datasets
- Related to LANDWISE Broad-scale survey data (soil near-surface properties, vegetation observations, land use, and management across Thames catchment, 2018–2021).
- Some measurements are site-specific with NA values where data were not collected or deemed invalid; detailed QC notes provide context for data interpretation.
- References and supporting documentation provided for methodological transparency and reproducibility.