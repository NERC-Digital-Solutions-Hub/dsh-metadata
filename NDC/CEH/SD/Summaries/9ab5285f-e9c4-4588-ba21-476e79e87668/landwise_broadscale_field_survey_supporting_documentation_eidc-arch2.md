# Soil near-surface properties, vegetation observations, land use and land management information for 1800 locations across the Thames catchment, UK, 2018-2021
## Landwise Broad-scale Field Survey

- Aim and context
  - Part of the Landwise project Broad-scale Field Survey, funded by NERC Natural Flood Management Programme.
  - Goal: quantify how innovative land use and management affect soil properties, with implications for natural flood management.
  - Covers the Thames catchment upstream of Maidenhead, UK.

- What the dataset includes
  - Soil near-surface physical and hydrological properties (0–50 mm below ground level), vegetation observations, and land use/management information.
  - Data collected at 1836 location points across 164 fields/land parcels.
  - Four land-use/management classes: arable with grass in rotation, arable without grass, permanent grassland, and broadleaf woodland.
  - Five soil/geology classes: shallow over chalk/limestone; free-draining loamy over chalk/limestone; impeded drainage loamy/clayey over chalk/limestone; slowly permeable loamy/clayey over mudstone; floodplain/high groundwater loamy/clayey over mudstone.
  - Anonymised location data (farm/field names removed; coordinates degraded to the nearest 1 km grid point).

- Sampling design and scope
  - Sampling conducted 2018–2021 (pause in 2020 due to Covid-19).
  - Approximately eight fields per cell across 20 combinations (resulting in 164 fields sampled).
  - Within each field/parcel:
    - Arable: 15 sampling locations (IN1–IN5; UN1–UN5; TR1–TR5 patterns).
    - Grassland: 10 sampling locations (UN1–UN5; TR1–TR5).
    - Woodland: 6 sampling locations (WD1–WD6), with field-area grids for planning.
  - Field sampling pattern aimed to cover expected soil variability, including infield, untrafficked margins, and trafficked headlands/tramlines.
  - Each field/parcel sampled once; a short Covid-related pause occurred in 2020.

- Primary data collected
  - Point data:
    - Location coordinates; soil measurements (0–50 mm bgl): dry bulk density, volumetric water content, organic matter, derived porosity, porosity accounting for organic matter.
    - Vegetation measurements: maximum and minimum height.
    - Qualitative soil measurements: hand texture, aggregate stability (slaking/dispersion), calcareous soil test, and subset VESS score.
    - Observations: soil surface condition and vegetation type.
  - Field contextual data:
    - Landowner/manager questionnaire data on crops, rotations, cover crops, management practices, tillage, drainage, grazing, woodland management, flood history, etc.
    - Derived secondary classifications from free-text questionnaire responses.
  - The dataset includes primary data, observations, and derived classifications, structured to support cross-field analyses.

- Analytical methods and derived data
  - Laboratory analyses:
    - Volumetric and bulk density; laser laser diffraction for particle size distribution; total and organic matter via loss on ignition; texture classification using hand texture and laser data.
    - Aggregate stability tests (VS-FAST) and hydrochloric acid test for calcareous soils.
  - Derived/secondary data:
    - Soil porosity estimates with and without accounting for organic matter (using assumed mineral/organic matter densities).
    - Soil texture classes determined from laser diffraction data using revised (7 µm) clay-silt cutoff alongside traditional cutoffs; two texture classifications provided to facilitate cross-method comparisons.
    - Detailed particle size distribution data in 1 µm bins between 2 and 11 µm to support reprocessing if needed.
  - Data handling and transformation:
    - Field coordinates converted to British National Grid; then anonymised to 1 km grid points.
    - Data processed in ArcGIS for quality checks; QA steps documented.

- Data structure and availability
  - Two main CSV files:
    - LANDWISE_BroadScale_Survey_Field_Contextual_Data_PUBLIC.csv (field contextual data; 84 columns, 165 rows).
    - LANDWISE_BroadScale_Survey_Point_Data_PUBLIC.csv (point data; 66 columns, 1837 rows).
  - A unique ID (ID_SiteNo_FieldNo) links the field contextual data to point data.
  - Supporting metadata files accompany the dataset (Field metadata CSV, Point metadata CSV) describing variable names, units, and descriptions.
  - Public dataset includes notes on measurement units and data provenance (field staff codes, QA processes).

- Quality control and limitations
  - QA processes include independent verification of transcription, cross-checks against field/lab sheets, and three-stage spatial coordinate validation (within-site proximity, within-field boundaries, and site-scale consistency).
  - Field teams had varying levels of expertise; a SurveyStaffCode is provided to aid cross-team comparisons.
  - Limitations:
    - Soil organic matter by loss on ignition is an estimate.
    - Derived porosity depends on assumed densities; accuracy improves with higher organic matter accuracy.
    - Secondary classifications from free-text are subject to analyst interpretation and may vary between analysts.
  - Data consistency and anonymisation measures ensure participant privacy while enabling cross-site analyses.

- Related datasets and references
  - Related to Landwise Detailed dataset: Hydraulic and hydrological data (surface and subsurface soils) across the Thames catchment, 2021, for seven fields sampled from the Broad-scale survey.
  - Methodology and lab protocols are documented in dedicated supporting documents and references (survey methodology, lab protocols, field record sheets).

- Practical relevance for environmental monitoring
  - Provides standardized, anonymised, multi-modal soil, vegetation, and land-management data across a wide spatial extent for flood management and soil-health assessments.
  - Enables comparison of soil properties across land-use types and soil/geology classes, with derived porosity and texture data suitable for modelling and policy evaluation.
  - Supports integration with broader Landwise datasets to assess hydrological and structural soil properties over time and space.