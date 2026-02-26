# LANDWISE_detailed_survey_soil_data_2021_updated_v2

## Overview
- Spatial scope: surface and sub-surface hydraulic and hydrological soil properties across the Thames catchment.
- Measured variables: soil bulk density, estimated soil porosity, volumetric soil moisture content, and soil moisture retention to 100 cm suction; surface infiltration rates; saturated hydraulic conductivity at 25 cm and 45 cm depth where possible.
- Field data: 7 fields across 3 sites with varied land use and management (arable and grassland/woodland) including trafficked areas, infield, and untrafficked margins.
- Timeframe: samples collected April 2021 to October 2021 with repeats pre- and post-harvest.
- Project context: UKCEH LANDWISE project assessing natural land-based flood risk reduction; funded by Natural Environment Research Council Grant NE/R004668/1.
- Relationship: part of LANDWISE; linked to Broad-scale survey and related datasets.

## Research Design
- Purpose: detailed survey to characterise field-scale heterogeneity under different Natural Flood Management (NFM) measures; follows a Broad-scale survey to enable site-specific comparisons.
- Site selection: seven fields chosen from Broad-scale survey based on soil type, geology, land-use, and management; sites include mudstone, chalk, and limestone geological groupings.
- Site configuration: three sites enabling comparisons across land-use/management within distinct geologies.
- Sampling framework: transects with 15 location types per field to capture trafficked (TR), infield (IN), and untrafficked margins (UN).

## Sampling Strategy
- Temporal design: multi-period sampling across an annual cycle; Spring, pre-harvest, and post-harvest campaigns.
- Measurements by location type: TR (trafficked), IN (infield), UN (untrafficked margin) across fields.
- Quantities per field: multiple samples per property type (e.g., 50 bulk density/porosity samples per field; 24 moisture retention samples across limestone sites; 12 saturated hydraulic conductivity measurements per field for some site types).
- Field layout: schematic transects with specific sampling locations (IN1-5, TR1-5, UN1-5) indicating representative infield, trafficked, and margin areas.
- Site and field mapping: Table 2 lists seven field sites with geology, land-use, and management details; approximate coordinates provided for anonymity.

## Soil Sampling
- Equipment: Eijkelkamp 07.53.SC sample rings, closed-ring holder, Edelman and Stony augers.
- Sample handling: sealed in polyethylene bags and refrigerated the day of collection.
- Laboratory processing: dry bulk density and volumetric moisture by oven drying (105 °C); porosity inferred from dry bulk density; moisture retention via Eijkelkamp Sandbox.

## Field Measurements: Infiltration
- Method: Mini Disk Infiltrometers (upper/lower chamber; controlled suction; porous disk).
- Procedure: vegetation cleared, surface levelled as needed, suction rate chosen by soil type (typically 2 cm; 0.5 cm for heavy clay sites); measurements recorded at set intervals to compute cumulative infiltration.
- Data handling: field data entered into Excel; unsaturated hydraulic conductivity (Kunsat) derived using Zhang (1997) method with van Genuchten parameters from Carsel & Parrish (1988).
- Notes: some measurements with limited infiltration (<15 ml) flagged in QC.

## Field Measurements: Saturated Hydraulic Conductivity (Kfs)
- Instrument: Guelph Permeameter (Mariotte principle).
- Depths: 25 cm and 45 cm, with wells prepared to consistent geometry; offset wells placed ~1 m apart to avoid saturation bulbs.
- Method: two-head technique (two different head heights) for higher accuracy; alternative heights used when slower permeable soils.
- Calculation: Kfs derived from steady-state water recharge rate, reservoir area, head height, and well geometry using a dedicated calculator.
- QC: data flagged for quality; preferred double-head measurements used when valid; otherwise two single-head measurements averaged.

## Volumetric Water Content & Dry Bulk Density
- VWC: obtained from oven-dried weight and soil mass; calculation uses water volume and sample volume with assume density of water = 1 g/cm³.
- Dry bulk density: mass of dry soil divided by sample volume (100.1 cm³).
- Porosity: estimated from dry bulk density using particle density 2.65 g/cm³ (for mineral soils).

## Soil Moisture Retention
- Method: Sandbox with multiple suction steps (pF 0 to pF 2) to derive retention curves.
- Sample preparation: soils saturated in sandbox; moisture loss tracked by daily weighings; evaporation minimized with lids.
- Suction sequence: 2.5 cm head for pF 0.4, then 1, 1.5, 1.7, 1.8, 2; data used to derive moisture retention characteristics.

## Nature and Units of Recorded Values
- Data file: LANDWISE_detailed_survey_soil_data_2021_updated_v2.csv with 70 columns and 380 rows.
- Key data columns cover: identifiers (site, field, location), location type, coordinates (BNG Easting/Northing), sampling dates/times, depths/horizons, measured properties (bulk density, porosity, VWC, moisture retention, Kunsat, Kfs, infiltration), root depth, and related notes.
- Missing values: represented as NA where measurements were invalid or not taken.

## Quality Control
- QC process: independent verification of entered field/lab data to catch typos or entry errors.
- Infiltration QC flags (Infiltration_1_QC_Flag and Infiltration_2_QC_Flag):
  - Good: no issues.
  - Invalid: physically implausible (removed).
  - A: unsteady infiltration rate.
  - B: <15 ml infiltrated (target requirement not met).
  - C: unusually high K values (potentially novel or erroneous; flagged).
- Saturated hydraulic conductivity QC flags (Guelph_Permeameter_QC_Flag):
  - Good or Invalid (invalid values removed).
- Note: Guelph_Permeameter_notes documents use of double-head vs single-head measurements; preference given to double-head when valid.

## Details of Data Structure
- File format: single CSV file named LANDWISE_detailed_survey_soil_data_2021_updated_v2.
- Columns: 70; Rows: 380.
- Data quality: NA used for missing or invalid entries; QC flags accompany specific measurements.

## Fieldwork and Laboratory Instrumentation
- Soil sampling: Eijkelkamp kit; Edelman and Stony augers.
- Drying and weighing: Heraeus ovens; Precisa balances (0.1 g precision); annual calibration.
- Infiltration: Mini Disk Infiltrometers (Decagon Devices).
- Saturated conductivity: Guelph Permeameter (Soilmoisture Equipment Corp.).
- Moisture retention: Eijkelkamp Sandbox.

## Miscellaneous
- Related dataset: Landwise Broadscale survey dataset “Soil near-surface properties, vegetation observations, land use and land management information for 1800 locations across the Thames catchment, UK, 2018-2021.”

## References
- Carsel, R. F., & Parrish, R. S. (1988). Developing Joint Probability Distributions of Soil Water Retention Characteristics. Water Resources Research.
- Decagon Devices (2018). METER Environment.
- METER (2021). MINI DISK INFILTROMETER manual.
- LANDWISE Detailed Survey Supporting Documentation (Version 1.4).
- Soilmoisture Equipment Corp. (2012). Guelph Permeameter—Operating Instructions.
- Soilmoisture Equipment Corp. (2020). Guelph Permeameter K-sat Calculator.
- Zhang, R. (1997). Determination of Soil Sorptivity and Hydraulic Conductivity from the Disk Infiltrometer. Soil Science Society of America Journal.