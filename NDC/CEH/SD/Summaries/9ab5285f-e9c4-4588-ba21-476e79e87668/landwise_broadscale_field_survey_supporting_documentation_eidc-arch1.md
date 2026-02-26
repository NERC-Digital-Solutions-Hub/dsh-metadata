Soil near-surface properties, vegetation observations, land use and land management information for 1800 locations across the Thames catchment, UK, 2018-2021

## Overview
- Dataset from the Landwise Broad-scale Field Survey, funded by NERC Natural Flood Management Programme (Grant NE/R004668/1).
- Contains soil near-surface physical/hydrological properties, vegetation observations, and land use/management data across the Thames catchment upstream of Maidenhead (UK).
- Aims to quantify how innovative land use/management affects soil properties with implications for natural flood management.
- Co-produced by UK Centre for Ecology & Hydrology and Landwise Partners; anonymised coordinates (degraded to 1 km grid) for privacy.

## What is included
- Field coverage: 1836 location points across 164 fields/land parcels; sampled to represent four land-use/management classes and five soil/geology classes.
- Field/point data types:
  - Primary field data: site context, land use, management questionnaire responses, field observations.
  - Primary point data: location, soil measurements (0–50 mm depth), vegetation heights, qualitative soil observations.
  - Secondary (derived) data: porosity estimates (with/without organic matter adjustments), soil texture classifications (two definitions), laser-diffraction particle size distribution (2–11 µm in 1 µm bins), and related calculations.
- Relation to other datasets: linked to Landwise Detailed survey dataset (hydraulic/hydrological data) for 7 fields.

## Survey design and sampling
- Fields sampled: across Thames catchment upstream of Maidenhead; four land-use/management classes (arable with/without grass, permanent grassland, broadleaf woodland) and five soil/geology classes (shallow over chalk/limestone, free-draining loamy over chalk/limestone, impeded drainage loamy/clayey over chalk/limestone, slowly permeable loamy/clayey over mudstone, floodplain/high groundwater loamy/clayey over mudstone).
- Approximately eight fields per cell (total 164 fields); pseudo-replicates avoided.
- Within fields:
  - Arable: 15 sampling locations (IN1–IN5, UN1–UN5, TR1–TR5) per representative area.
  - Grassland: 10 sampling locations (UN1–UN5, TR1–TR5).
  - Woodland: 6 representative sampling locations (WD1–WD6) with 2×3 grid layout; any organic layer samples handled per plan, but typically only mineral soil sampled.
- Sampling occurred Dec 2018–Mar 2021 (pause Mar–Dec 2020 due to COVID-19).

## Collection methods (primary data)
- Field actions and sampling are documented in the Survey Methodology (and related appendices).
- Location data: coordinates collected with handheld GPS or mobile GPS; field observations recorded on survey sheets.
- Soil sampling: 0–50 mm bgl volumetric samples using 50 mm rings; additional non-volumetric samples with trowel.
- In-field measurements: soil texture by hand, VESS scores for a subset, field observations of soil surface condition.
- Sample handling: soils sealed and refrigerated; lab analyses started typically within ~4 weeks.

## Analytical methods (lab)
- Dry bulk density and volumetric water content via oven-drying (105°C, 36 h).
- Laser particle size distribution (Malvern Mastersizer 2000) with Hydro 2000G.
- Sub-samples for: aggregate stability (slaking/dispersion), loss-on-ignition for soil organic matter (400°C 16 h), hydrochloric acid test for calcareous soil.
- Texture classification: two approaches
  - Traditional SS England & Wales limits (sand/silt/clay).
  - Revised clay-silt cutoff using laser diffraction data (adopts ~7 µm cutoff; provides 1 µm bin data from 2–11 µm for reprocessing as consensus evolves).

## Secondary (derived) data
- Porosity estimates:
  - Basic porosity: 1 − (bulk density / 2.65 g/cm³).
  - Porosity accounting for organic matter: weighted average particle density (based on OM%) and revised porosity formula.
- Texture: two classifications (traditional vs revised cutoff) and 1 µm-binned laser diffraction data for reclassification as needed.
- Coordinate handling: primary coordinates converted to British National Grid (BNG) and rounded; public dataset uses 1 km grid for anonymity.

## Data structure and access
- Two main public CSV files:
  - LANDWISE_BroadScale_Survey_Field_Contextual_Data_PUBLIC.csv: Field contextual data; 84 columns, 165 rows; joinable via ID_SiteNo_FieldNo.
  - LANDWISE_BroadScale_Survey_Point_Data_PUBLIC.csv: Point data; 66 columns, 1837 rows; joinable via ID_SiteNo_FieldNo.
- Metadata references (field and point) provided in accompanying metadata CSV files; field observations, measurements, and derived classifications are documented.
- Data notes:
  - SurveyStaffCode indicates varying field-team expertise (useful for bias checks).
  - OM-based porosity and derived measures carry typical uncertainties; secondary classifications may vary between analysts.
- Documentation and related dataset:
  - Field context and point data tables with units and descriptions in separate metadata files.
  - Related to Landwise Detailed survey dataset (hydraulic and hydrological measurements at higher resolution).

## Practical considerations for analysts
- Spatial analyses should account for anonymised 1 km grid coordinates, which may limit fine-scale spatial inference.
- Derived porosity and organic-matter-adjusted porosity provide more robust estimates in organic-rich sites (e.g., woodland soils).
- Texture classifications can be harmonised over time by choosing traditional vs revised clay-silt cutoffs; the 1 µm binned data enables reprocessing as methodological consensus evolves.
- Data quality controls are documented, with multi-stage QA for coordinates and a blind transcription/verification workflow; still, field-team variability and free-text-derived classifications should be considered in analyses.
- The dataset supports modeling soil physical properties, vegetation factors, and land-use impacts on soil attributes, with potential integration into broader Flood Management and soil-health studies.

## References and notes
- Data collection and methodology are described across Field Contextual Data, Point Data, Survey Methodology, Lab Protocol, and supporting literature cited within the dataset description.
- Key references include methods for soil texture classification, VESS scoring, soil organic matter measurement, and laser diffraction considerations (e.g., Hassink et al., Ball et al., McGarry, Fae et al., Bittelli et al., Mako et al., Qiu et al., Natural England TIN037).