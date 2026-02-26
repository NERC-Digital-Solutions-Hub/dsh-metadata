# Soil near-surface properties, vegetation observations, land use and land management information for 1800 locations across the Thames catchment, UK, 2018-2021 Landwise Broad-scale Field Survey

## Overview and scope
- Large field-scale dataset from the Landwise Broad-scale Field Survey, funded by NERC (Grant NE/R004668/1).
- Covers soil near-surface properties (0–50 mm bgl), vegetation observations, and land use/management information across the Thames catchment upstream of Maidenhead, UK.
- Data collected at 1836 location points across 164 fields/land parcels between 2018 and 2021 (pause in 2020 due to Covid-19).
- Primarily aimed at understanding how different land uses and management practices affect soil properties, with implications for natural flood management.
- Data anonymised for public release: location identifiers retained, but field/site coordinates degraded to the nearest 1 km grid point.

## Data content
- Field Contextual Data (Field_Contextual_Data_PUBLIC.csv)
  - 84 columns, 165 rows; primary data from landowner/manager questionnaires and general field observations.
  - Includes land use/management information (crop types, rotation, grazing, lime, tillage, drainage, buffer strips, woodland management, etc.), and derived secondary classifications from free-text responses.
  - Administrative notes on survey staff and site relevance per land use type.
- Point Data (Point_Data_PUBLIC.csv)
  - 66 columns, 1837 rows; per-sampling-point measurements and observations.
  - Includes:
    - Location: survey point coordinates (BNG or LAT/LONG, then transformed to BNG; later anonymised to 1 km grid).
    - Soil measurements (0–50 mm bgl): dry bulk density, volumetric water content, organic matter, derived porosity (basic and OM-adjusted).
    - Vegetation measurements: maximum and minimum height.
    - Qualitative soil measurements: hand texture, aggregate stability (slaking/dispersion), calcareous soil test, and subset VESS scores.
    - Observations: soil surface condition (e.g., slaked/unslaked, poached) and vegetation type.
  - Data dictionaries (Field metadata and Point metadata) describe variable names, units, and meanings.

## Sampling design and survey methodology
- Four broad land-use/management classes: arable (with and without grass in rotation), permanent grassland, and broadleaf woodland.
- Five soil/geology classes: shallow over chalk/limestone; free-draining loamy over chalk/limestone; impeded drainage loamy/clayey over chalk/limestone; slowly permeable loamy/clayey over mudstone; floodplain/high groundwater loamy/clayey over mudstone.
- Approximately eight fields per combination, totaling 164 fields; pseudo-replicates avoided.
- Sampling locations per field:
  - Arable: 15 representative locations (IN1–IN5, UN1–UN5, TR1–TR5 across three zones).
  - Grassland: 10 locations (UN1–UN5 and TR1–TR5).
  - Woodland: 6 locations for volumetric soil samples; 2×3 grid planning for sampling area.
- Sampling pattern: typically a W-walk to capture spatial variability, with field-area adjustments as agreed with landowners/managers.
- Sampling window: December 2018 – March 2021 (Covid-19 pause in 2020).

## Collection methods and laboratory analysis
- Primary data collection:
  - In-field sampling of 0–50 mm bgl soil using 50 mm diameter rings; additional non-volumetric samples collected by trowel.
  - Field observations of soil surface condition and vegetation type; GPS-derived coordinates (preferred handheld GPS).
  - Hand texture classification and Visual Evaluation of Soil Structure (VESS) at selected points.
  - Soil samples stored, refrigerated, and analysed in the lab.
- Laboratory analyses:
  - Dry bulk density and volumetric water content via oven-drying (105°C, 36 h).
  - Particle size distribution via laser diffraction (Malvern Mastersizer 2000) with multiple bin definitions; subset of data reprocessed for 1 µm bins in 2–11 µm range to support texture classification refinements.
  - Soil texture classification using soiltexture R package with two criteria:
    - Traditional SS&E&W classification.
    - Revised clay-silt cutoff using a 7 µm boundary, with 1 µm resolution data provided to enable reprocessing as needed.
  - Organic matter by loss on ignition (LOI) at 400°C; calcareous soil test via hydrochloric acid.
  - In-field and lab QA steps, instrument calibration, and cross-checks with field sheets.

## Derived data and texture methodology
- Derived soil porosity estimates:
  - Standard porosity: 1 − (Dry bulk density / 2.65 g/cm³).
  - Porosity accounting for organic matter (two approaches):
    - Weighted-average particle density based on soil organic matter percentage.
    - Porosity adjusted for variable organic matter content with a density mix of mineral (2.65) and organic matter (1.25) g/cm³.
- Soil texture classification:
  - Two texture definitions provided:
    - Traditional (SS&E&W cutoff sizes).
    - Revised (Laser Diffraction Method, LDM) with a 7 µm clay/silt boundary.
  - Detailed particle size distribution data available in 1 µm bins from 2–11 µm to support future reprocessing and harmonization with different texture schemes.
- Metadata and data structure:
  - Two public CSV files linked by ID_SiteNo_FieldNo.
  - Suffix conventions in variable names:
    - -Txt (free text)
    - -Obs (observations)
    - -Class (secondary classification)
    - -Yr (years)
    - -Mea (measurements)
    - -Deriv (derived data)
- Coordinates and privacy:
  - Public dataset coordinates degraded to the nearest 1 km grid; BNG transformation steps documented.

## Data quality, limitations, and caveats
- Data reliability considerations:
  - Field teams varied in expertise; a SurveyStaffCode is included to support cross-team comparisons.
  - LOI as a proxy for soil organic matter; derived porosity depends on assumed particle densities.
  - Secondary (derived) classifications originate from interpretation of free-text responses and field observations; potential variability across analysts.
- Measurement considerations:
  - Some measurements (e.g., LOI) are estimates; derived porosity has higher uncertainty when OM content is high.
  - The public dataset provides anonymized location data; some field-level detail is retained in contextual data but not in geolocation.
- Relationship to other datasets:
  - Related to Landwise Detailed survey dataset (Hydraulic and hydrological measurements in 7 fields) for higher-resolution, time-series analyses.

## Data structure and access
- Public data files:
  - LANDWISE_BroadScale_Survey_Field_Contextual_Data_PUBLIC.csv (84 columns, 165 rows)
  - LANDWISE_BroadScale_Survey_Point_Data_PUBLIC.csv (66 columns, 1837 rows)
- Linking key:
  - ID_SiteNo_FieldNo: unique identifier to join field contextual and point data.
- Documentation and references:
  - Field metadata and Point metadata CSVs describe variable names, units, and descriptions.
  - Supporting methodological and laboratory protocols linked within the public documentation.
  
## Usage implications and potential applications
- Suitable for exploring relationships between land use/management and near-surface soil properties across a large catchment.
- Enables self-serve data exploration through derived porosity, texture classifications (traditional and revised), and spatially distributed soil properties.
- Valuable for policy, land management, and flood-risk assessments that require integration of soil characteristics with land-use data.
- The presence of QA steps, staff variability indicators, and anonymized coordinates supports careful cross-site comparisons while preserving participant privacy.

## Related materials and references
- Landwise Detailed survey dataset: Hydraulic/hydrological data across Thames catchment (subset, 2021) available through NERC EIDC.
- Supporting documents include:
  - Field Contextual Data metadata
  - Point Data metadata
  - Landwise Broad-scale Field Survey Methodology
  - Landwise Laboratory Analysis Protocol
- References for methods and classifications (e.g., VESS, LOI, laser diffraction texture, texture cutoff debates) are cited within the dataset documentation.