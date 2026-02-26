# Soil near-surface properties, vegetation observations, land use and land management information for 1800 locations across the Thames catchment, UK, 2018-2021 Landwise Broad-scale Field Survey

## Overview
- Describes the Landwise Broad-scale Field Survey dataset collected (2018–2021) to quantify how land use and management affect soil properties, with implications for natural flood management.
- Scope: Thames catchment upstream of Maidenhead, UK; 1836 location points across 164 fields/land parcels; anonymised data with coordinates degraded to protect privacy.
- Funded by the NERC Natural Flood Management Research Programme; dataset prepared by UK Centre for Ecology & Hydrology and Landwise partners.

## Dataset scope and purpose
- Primary aim: provide near-surface soil properties, vegetation observations, and land-use/management information to support environmental monitoring and decision-making.
- Intended for use in evaluating policy, monitoring effectiveness, and informing future land-management decisions.
- Publicly documented with accompanying field and lab methodologies to enable reproducibility and informed data usage.

## Sampling design and coverage
- Field classes: four broad land-use/management classes (arable with/without grass in rotation, permanent grassland, broadleaf woodland) and five soil/geology classes (varying surface geology and drainage).
- Sampling distribution: ~8 fields per cell across 20 combinations, totaling 164 fields; pseudo-replicates avoided to maintain design robustness.
- In each field/parcel:
  - Arable: 15 representative sampling locations (IN1–IN5, UN1–UN5, TR1–TR5 across three area types)
  - Grassland: 10 locations (UN1–UN5, TR1–TR5)
  - Woodland: 6 locations (WD1–WD6)
- Sampling pattern: primarily a W-walk per field; adjustments made for field size/topography to target soil/geology classes.
- Timing: one sampling event per field between December 2018 and March 2021; pause in 2020 due to COVID-19.

## Data collected (primary and contextual)
- Point data (per sampling location):
  - Location coordinates (BNG or LAT/LONG; later converted to BNG; rounded to 1 km for public data)
  - Soil measurements: dry bulk density, volumetric water content (0–50 mm below ground), organic matter, porosity (and porosity accounting for organic matter), particle size distribution, texture classification
  - Vegetation measurements: maximum and minimum height
  - Qualitative soil observations: texture via hand test, aggregate stability (slaking/dispersion), calcareous soil test, Visual Evaluation of Soil Structure (VESS) for a subset
  - Observations: soil surface condition, vegetation type
- Field contextual data (owner/management questionnaire and observations):
  - Land use and management details per field (crop types/rotation, cover crops, herbal leys, organic/conventional farming, lime, tillage, tramlines, buffers, drainage, grazing, woodland management, history, flooding)
  - Derived secondary data: classification of free-text responses; field observations
- Anonymisation: farm/field names removed; coordinates degraded to 1 km grid; all data prepared for public release with privacy safeguards.

## Laboratory and measurement methods
- Primary sample collection: 0–50 mm bgl soil samples using 50 mm rings; additional non-volumetric samples; field texturing per Fertiliser Manual methodology; VESS tests for selected points.
- Laboratory analyses:
  - Dry bulk density (105°C drying, 36 h) and volumetric water content
  - Laser particle size distribution (Malvern Mastersizer 2000) across multiple µm bins; subsequent rebinning to include 1 µm wide ranges (2–11 µm)
  - Texture classification using soiltexture R package with traditional and revised clay-silt cutoffs
  - Aggregate stability (VS-FAST method), loss on ignition for organic matter (400°C), hydrochloric acid test for calcareous soil
- Field equipment: Eijkelkamp sampling rings; GPS for location; Think Soils Manual for surface condition references
- Calibration and QA: balances/calibration checks; instrument QA standards; independent data quality checks; transcription verification; coordinate quality control in ArcGIS with multi-stage checks

## Derived and secondary data
- Porosity estimation:
  - Default porosity: from dry bulk density with mineral density of 2.65 g/cm3
  - Porosity accounting for organic matter: uses weighted-average particle density based on soil organic matter percentage
- Soil texture:
  - Traditional texture classification (SWE clay/silt thresholds) and revised clay-silt cutoff using laser diffraction (adopts a 7 µm cutoff with options described in literature)
  - Provides 1 µm bin data (2–11 µm) to facilitate reprocessing as consensus on cutoffs evolves
- Data structure and provenance:
  - Two public CSV files: Field Contextual Data (LANDWISE_BroadScale_Survey_Field_Contextual_Data_PUBLIC.csv) and Point Data (LANDWISE_BroadScale_Survey_Point_Data_PUBLIC.csv)
  - Metadata files reference variable descriptions, units, and applicable survey sections
  - Suffix conventions indicate data type (Txt, Obs, Class, Yr, Mea, Deriv)
- Coordinate handling:
  - Field coordinates converted to British National Grid; accuracy transformations noted; public data rounded to 1 km grid for anonymity

## Data quality, limitations, and governance
- Quality assurance:
  - Independent data assessor checks; cross-verification against field/lab sheets; systematic transcription checks
  - Spatial QC ensures sampling points are within plausible field/site boundaries; outliers investigated and removed when needed
- Limitations:
  - Field teams with varying expertise introduce potential variability; SurveyStaffCode included to enable stratified analyses
  - Derived porosity and organic-matter-based corrections rely on assumed densities and estimates; inherent uncertainties acknowledged
  - Secondary classifications derived from free-text/observations may vary between analysts
- Documentation and metadata:
  - Comprehensive field and point metadata accompany the data; explicit notes on limitations and data reliability
  - Related to Landwise Detailed survey dataset (hydrological measurements at 7 fields) for higher-resolution follow-up

## Access, usage, and relationship to other data
- Primary dataset available via Environmental Data Initiative (EDI/CDON) and Landwise project outputs
- Related datasets: Landwise Detailed survey dataset (hydrological measurements) for deeper soil-hydrology coupling
- Acknowledgments and references:
  - Detailed references provided for field/lab methods, QA practices, and context (e.g., Ball et al., Hassink et al., Mako et al., Qiu et al., etc.)

## Practical implications for monitoring and policy
- The dataset provides a multi-dimensional view of soil properties, vegetation, and land-use practices across a large catchment, enabling:
  - Evaluation of land-use changes on soil physical/hydrological properties
  - Evidence-based monitoring of soil quality and resilience under different management regimes
  - Integration with hydrological data for flood management planning and assessment
- Robust metadata, QA processes, and derived variables (porosity, texture under different cutoffs) support consistent monitoring and potential policy evaluation over time.