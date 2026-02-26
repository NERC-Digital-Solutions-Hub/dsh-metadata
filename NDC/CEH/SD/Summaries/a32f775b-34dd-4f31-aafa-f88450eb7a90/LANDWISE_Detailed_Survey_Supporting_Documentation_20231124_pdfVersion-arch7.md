LANDWISE detailed survey soil data 2021 updated v2

- Overview
  - A dataset of surface and sub-surface hydraulic and hydrological soil properties across the Thames catchment.
  - Measurements include soil bulk density, estimated porosity, volumetric soil moisture content, and soil moisture retention (to 100 cm suction). Infiltration rates and saturated hydraulic conductivity (Ksat) were measured at 25 cm and 45 cm depths where possible.
  - Data collected from seven fields across three sites with varying land use/management (arable, grassland, woodland) in 2021, with transects across trafficked, infield, and untrafficked margins.
  - Part of the LANDWISE project within the NERC Natural Flood Management programme; spring 2021 and autumn 2021 sampling, with pre- and post-harvest repeats.

- Spatial coverage and sampling design
  - Seven fields selected from a Broad-scale LANDWISE survey; Sites include mudstone, chalk, and limestone geology.
  - Location identifiers: ID_SiteNo, ID_FieldNo, ID_LocationCode; combined IDs (ID_SiteNo_FieldNo, ID_SiteNo_FieldNo_Loc).
  - Spatial coordinates provided as OS Grid references with Easting and Northing (BNG) for GIS mapping.
  - Sampling locations within fields categorized as:
    - TR (trafficked areas, e.g., tramlines, tracks)
    - IN (infield)
    - UN (untrafficked field margins)
  - Temporal coverage: Spring (April 2021) and Autumn (October 2021) campaigns.

- Measurements and methods (high-level)
  - Bulk density and inferred porosity (depth-resolved) via volumetric cores and oven drying.
  - Volumetric soil moisture content (VWC) and soil porosity estimation.
  - Soil moisture retention across pF0 to pF2 using Sandbox analysis.
  - Saturated hydraulic conductivity (Ksat) at 25 cm and 45 cm using Guelph Permeameters.
  - Infiltration measurements (unsaturated hydraulic conductivity, Kunsat) using Mini Disk Infiltrometers.
  - Soil and vegetation root depth (arable, grassland, woodland) via auger and tape measure.
  - Depths and horizons recorded for each sampling location.
  - Measurements conducted along transects in each field (TR1–TR5, IN1–IN5, UN1–UN5) with field types mapped to site geology and land use.

- Instruments and field/lab workflow
  - Soil sampling: Eijkelkamp ring kit with closed ring holder; Edelman and Stony augers.
  - Drying and weighing: Heraeus ovens; Precisa balances; standard calibration checks.
  - Infiltration: Mini Disk Infiltrometers; measurements at controlled suction; water used to avoid altering soil solution chemistry.
  - Ksat: Guelph Permeameters with two-head method for higher accuracy; field prep to ensure uniform wells.
  - Soil moisture retention: Eijkelkamp Sandbox with deionised water and copper sulfate to minimize algal growth.

- Data structure and content
  - File: LANDWISE_detailed_survey_soil_data_2021_updated_v2.csv
  - Size: 70 columns, 380 rows
  - Location and sample fields include:
    - IDs: ID_SiteNo, ID_FieldNo, ID_LocationCode, ID_SiteNo_FieldNo, ID_SiteNo_FieldNo_Loc
    - Location metadata: LocationTypeObs, OS_Grid_Sq, EastingBNG_PUBLIC, NorthingBNG_PUBLIC
    - Temporal data: Date_Sample_1, Time_Sample_1, Date_Sample_2, Time_Sample_2
    - Depths and horizons: Sample_1_Soil_Depth, Sample_1_Root_Depth, Sample_1_Horizon_1/2/3, etc. (Autumn equivalents Sample_2_*)
    - Soil measurements: VolSoilMoistMea, DryBulkDenMea, EstPorosityDeriv
    - Infiltration data: Infiltration_1_Kunsat, Infiltration_1_Kunsat_ms, Infiltration_1_QC_Flag, Infiltration_1_notes; Infiltration_2_* (Autumn)
    - Ksat data: Guelph_Permeameter_Date, Guelph_Permeameter_Depth, Guelph_Permeameter_Kfs, Guelph_Permeameter_Kfs_ms, Guelph_Permeameter_QC_Flag, Guelph_Permeameter_notes
    - Additional QC notes: SMR_notes, Infiltrometer_1_notes, Infiltrometer_2_notes
    - Core field measurements: SMR_VWC_pF_0 to SMR_VWC_pF_2 (in sandbox tests)
    - Spatial coordinates: EastingBNG_PUBLIC, NorthingBNG_PUBLIC
  - NA values indicate missing data or not measured.
  - Data also linked to supporting documentation and references for methodology.

- Quality control and data governance
  - Data entry checked by separate staff to catch typos; cross-validated against original recordings.
  - Infiltration measurements QC flags:
    - Good, Invalid, A (unsteady infiltration), B (<15 ml infiltrated), C (unusually high K values)
  - Saturated hydraulic conductivity QC flags:
    - Good, Invalid
  - Notes indicate use of double-head vs average of two single-head measurements; preference given to double-head when valid.
  - Some measurements flagged or removed if physically implausible.

- Usage notes for GIS and data products
  - Ready-to-map variables include bulk density, porosity, VWC, moisture retention (pF), Kunsat, Ksat, root depth, horizon depths, and land-use/geology context.
  - Spatial layers can be built by site, field, geology (mudstone, chalk, limestone) and land-use type (arable, grassland, woodland).
  - Time-series capabilities by campaign (Spring 2021 vs Autumn 2021) and pre-/post-harvest context where applicable.
  - Suitable for creating thematic maps of soil hydraulic properties, infiltration capacity, and depth profiles across the Thames catchment.
  - Can be integrated with the related LANDWISE Broad-scale survey dataset to produce multi-resolution maps of soil near-surface properties, vegetation observations, land use, and land management.

- Related resources and references
  - LANDWISE Detailed Survey Supporting Documentation (Version 1.4) and related LANDWISE broad-scale datasets.
  - Method references for data processing (Zhang 1997; Carsel & Parrish 1988) and instrument manuals.
  - Field and lab instrumentation specifications cited in dataset documentation.