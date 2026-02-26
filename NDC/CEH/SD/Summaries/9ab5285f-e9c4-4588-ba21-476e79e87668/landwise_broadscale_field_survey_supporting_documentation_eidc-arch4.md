# Soil near-surface properties, vegetation observations, land use and land management information for 1800 locations across the Thames catchment, UK, 2018-2021

## Overview
- Dataset from the Landwise Broad-scale Field Survey, funded by NERC Natural Flood Management (Grant NE/R004668/1).
- Covers soil near-surface physical/hydrological properties, vegetation observations, and land use/management information across the Thames catchment (upstream of Maidenhead), collected 2018–2021.
- Co-produced by UK CEH and Landwise Partners; anonymised and spatially generalized in public release.

## Dataset description and structure
- Total sampling: 1,836 location points across 164 fields/land parcels.
- Four land-use/management classes: arable with grass in rotation, arable without grass, permanent grassland, broadleaf woodland.
- Five soil/geology classes: shallow over chalk/limestone; free-draining loamy over chalk/ limestone; impeded drainage loamy/clayey over chalk/limestone; slowly permeable loamy/clayey over mudstone; floodplain/high groundwater loamy/clayey over mudstone.
- Two primary CSV files (public):
  - LANDWISE_BroadScale_Survey_Field_Contextual_Data_PUBLIC.csv (Field contextual data, 84 columns, 165 rows).
  - LANDWISE_BroadScale_Survey_Point_Data_PUBLIC.csv (Site point data, 66 columns, 1,837 rows).
- Linking key: ID_SiteNo_FieldNo to join field contextual data with point data.
- Public data include anonymized coordinates (rounded to nearest 1 km grid) to protect participant locations.

## Sampling design and field methodology
- About 8 fields sampled per cell combination (20 land-use/geology combinations), totaling 164 fields.
- Field sampling patterns by land use:
  - Arable: 15 sampling locations per field (IN1–IN5, UN1–UN5, TR1–TR5 across infield, untrafficked margins, trafficked headlands/tramlines).
  - Grassland: 10 locations per field (UN1–UN5, TR1–TR5).
  - Woodland: 6 locations (WD1–WD6).
- Sampling within fields:
  - 0–50 mm below ground level (bgl) for volumetric and additional non-volumetric soil samples.
  - Visual Evaluation of Soil Structure (VESS) at selected locations.
  - Woodland: sampling grid of approximately 2×3; organic layer depth generally <50 mm; one mineral soil sample per location.
- Sampling period: December 2018–March 2021 (pause Mar–Dec 2020 due to COVID-19).

## Data collected (primary data)
- Field contextual data: owner/manager responses to land-use questionnaires, field observations (e.g., slope, surface condition), and free-text classifications.
- Point data: location coordinates (BNG or lat/long), soil measurements (0–50 mm bgl):
  - Volumetric water content, dry bulk density.
  - Qualitative/texture data: hand texturing, slaking/dispersion, calcareous soil indicator.
  - Vegetation height (min/max) observations; surface conditions.

## Laboratory analyses and instrumentation
- Soil analyses (primary data):
  - Dry bulk density and volumetric water content (oven-dried at 105°C, 36 h).
  - Laser diffraction particle size distribution (Malvern Mastersizer 2000) for detailed texture (binning 0.01–60–63–2000 µm; expanded 1 µm bins in 2–11 µm range).
  - Organic matter by loss on ignition (LOI) at 400°C (Nelson & Sommers method).
  - Calcareous soil test (HCl).
  - Aggregate stability (slaking/dispersion) per VS-FAST with Field et al. scoring.
  - Hand texturing (in-field or lab).
- Visual soil structure assessment (VESS) at selected points.

## Derived (secondary) data and methods
- Soil porosity estimates:
  - Standard porosity: 1 − (dry bulk density / 2.65 g/cm3).
  - Porosity accounting for organic matter using weighted average particle density (2.65 g/cm3 for mineral, 1.25 g/cm3 for organic fraction) based on organic matter percentage.
- Texture classification:
  - Two texture definitions provided: traditional S&E&W (USDA/W) limits; revised clay-silt cutoff for laser diffraction data.
  - Revised cutoff centered around 7 µm (with discussion of 5–8 µm alternatives in literature); dataset also provides 1 µm-binned distribution (2–11 µm) to adapt to future consensus.
- Coordinate data handling:
  - Field coordinates originally captured in BNG or lat/long, converted to OSGB 1936 and rounded to 1 m; public release further rounded to 1 km for anonymity.

## Data quality, governance, and limitations
- Quality control:
  - Transcription verification; independent data assessor reviews primary data; QA standards for equipment (balances, Mastersizer, calibration checks).
  - Multi-stage QC for soil coordinates: proximity checks within sites, field boundary checks, and site-level outlier checks.
  - Independent checks for secondary classifications.
- Data limitations:
  - Field teams varied in expertise; SurveyStaffCode available for cross-analysis by team.
  - LOI and porosity derived values are estimates with uncertainties, particularly at higher organic matter contents.
  - Secondary classifications from free-text responses involve analyst interpretation and may vary between analysts.
  - Public coordinates are anonymized to 1 km grid.

## Related data and usage
- Related dataset: Landwise Detailed survey dataset (Hydraulic/hydrological measurements at 7 fields; 2021) available via NERC EIDC; complements Broad-scale data with higher spatial resolution and temporal repeat measurements.
- Potential uses for data leaders:
  - Assessing soil physical properties in relation to land use and management across a major catchment.
  - Verifying data suitability and gaps for flood management, soil health, and land-use policy analyses.
  - Integrating with broader data networks to support co-ownership of data products and system-wide data stewardship.

## References and documentation
- Supporting documents include field metadata, point metadata, survey methodology, survey record sheets, and laboratory protocol.
- Methodological and analytical references cover soil texture classifications, VESS, LOI, particle size methodology, and data quality practices.