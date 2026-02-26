# Soil near-surface properties, vegetation observations, land use and land management information for 1800 locations across the Thames catchment, UK, 2018-2021

- The Landwise Broad-scale Field Survey dataset captures soil near-surface properties, vegetation observations, and land use/management information across the Thames catchment (UK) collected between 2018 and 2021.
- Survey scope: 1836 location points across 164 fields/land parcels, representing four land-use/management classes (arable with and without grass rotation, permanent grassland, broadleaf woodland) and five soil/geology classes. The dataset title refers to 1800 locations, while the documentation notes 1836 sampled points.

## What the dataset contains

- Primary data (point-level and field-contextual information) and derived data (secondary variables) for each sampling location.
- Two public CSV files that form the core dataset:
  - LANDWISE_BroadScale_Survey_Field_Contextual_Data_PUBLIC.csv
  - LANDWISE_BroadScale_Survey_Point_Data_PUBLIC.csv
- Ancillary supporting documentation includes field metadata, point metadata, the survey methodology, survey record sheets, and the lab protocol.

## Data structure and how to join

- The two CSV files can be joined via the unique identifier ID_SiteNo_FieldNo (links field/land parcel to its sampling points).
- Field Contextual Data file:
  - 84 columns, 165 rows
  - Contains land-use-specific contextual information, questionnaire responses, and general field observations
- Point Data file:
  - 66 columns, 1837 rows
  - Contains location-level measurements and observations for each sampling point
- Suffixes in variable names indicate data type:
  - -Txt (free text)
  - -Obs (observations)
  - -Class (secondary classification)
  - -Yr (years for classifications)
  - -Mea (measurements)
  - -Deriv (derived data)

## Spatial and privacy aspects

- Sampling coordinates are recorded in British National Grid (BNG) or latitude/longitude and converted to BNG for GIS use.
- Public version coordinates are anonymised by degrading location points to the nearest 1 km grid point to protect participant privacy.
- Spatial scope is the Thames catchment upstream of Maidenhead, with site-level coordinates aligned to field boundaries and sampling transects.

## Survey design and sampling regime

- Fields/land parcels sampled to cover 20 combinations of land use/management and soil/geology classes (4 land-use classes × 5 soil/geology classes).
- Approximately eight fields per cell, avoiding pseudo-replication; total ~164 fields.
- Sampling patterns by land-use type:
  - Arable: 15 representative sampling locations per field (5 replicates for infield, untrafficked margins, and trafficked headlands/tramlines)
  - Grassland: 10 locations (5 untrafficked, 5 trafficked)
  - Woodland: 6 representative sampling locations for volumetric soil samples
- W-walk sampling pattern used to capture spatial variability; occasional field-specific adjustments based on owner input or mapping.
- Within each field/parcel, a representative subset was selected for VESS (Visual Evaluation of Soil Structure).

## Primary data collected

- Soil near-surface properties (0–50 mm below ground level):
  - Dry bulk density, volumetric water content
  - Organic matter (by measurement methods)
  - Derived porosity (and porosity accounting for variable organic matter)
- Vegetation measurements:
  - Maximum and minimum vegetation height
- Soil qualitative measurements:
  - Hand texture, aggregate stability (slaking/dispersion), calcareous soil tests (HCl), VESS score (subset)
- Observations:
  - Soil surface condition (e.g., slaked, poached, etc.)
  - Vegetation type
- Field contextual data:
  - Land-owner/manager responses to land-use/management questionnaires
  - Derived classifications from free-text questionnaire responses
  - General field observations (slope, surface form, erosion/deposition features)

## Laboratory analyses and instrumentation

- Primary analyses conducted in the lab:
  - Volumetric soil samples dried to determine dry bulk density and volumetric water content
  - Laser particle size distribution (Malvern Mastersizer 2000) for detailed texture and size distribution (0.01–2000 µm bins, with refined 1 µm bins for 2–11 µm range)
  - Texture classification using soiltexture R package (two classifications:
    - Traditional S&E&W soil texture limits
    - Revised laser diffraction-based boundaries (clay-silt cutoff around 7 µm; results provided for comparison)
- Additional analyses:
  - Soil organic matter by loss on ignition (LOI at 400°C)
  - Aggregate stability tests and other texture-related measurements
- Instruments:
  - Eijkelkamp soil rings, drying ovens, analytical balances, ashing furnace, Mastersizer 2000 with Hydro 2000G

## Derived data and texture considerations

- Porosity calculations:
  - Standard porosity from dry bulk density (assuming 2.65 g/cm³ mineral density)
  - Porosity accounting for organic matter using a weighted average particle density (based on estimated soil OM%)
- Soil texture classification:
  - Two classifications provided: 
    - Traditional S&E&W limits
    - Revised laser diffraction-based boundaries with a 7 µm cutoff
  - 1 µm-bin distribution data (2–11 µm) available to reprocess texture classifications as consensus on clay-silt cutoffs evolves
- Notes on texture methodology:
  - LDM data generally aligns with reference methods, but cross-method adjustments may be needed to align with SPM-based soil texture databases

## Data quality, limitations, and caveats

- Field teams had varying levels of expertise; a SurveyStaffCode is provided to contextualize observations.
- Soil organic matter and derived porosity involve estimations; accuracy decreases with higher OM content or uncertain particle densities.
- Secondary classifications are interpretative and may vary between analysts.
- Anonymisation may limit certain locational analyses at very fine scales.
- The Broad-scale dataset links to a related Detailed survey with higher spatial resolution measurements.

## Related datasets and references

- Related Landwise Detailed survey: Hydraulic and hydrological data across the Thames catchment (7 fields, higher resolution, temporal replication)
- Related documentation and standards referenced for methodology, QA, and data interpretation:
  - Field metadata CSV
  - Point metadata CSV
  - Landwise survey methodology PDF
  - Survey record sheet PDFs
  - Laboratory protocol PDF
  - Key literature on soil texture methods and QA procedures (e.g., Ball et al., Hassink et al., Nelson & Sommers, etc.)

## How this dataset can be used in GIS

- Spatial integration:
  - Join Field Contextual Data and Point Data via ID_SiteNo_FieldNo
  - Use BNG coordinates or converted LAT/LONG coordinates; coordinate anonymisation applied for public access
- Map products:
  - Visualize soil properties (dry bulk density, volumetric water content, porosity with and without OM correction)
  - Map vegetation metrics (height ranges)
  - Display land-use/management classifications and soil/geology classes across the Thames catchment
  - Create derived spatial layers for texture class (traditional vs revised LDM-based) and OM-adjusted porosity
- Temporal and cross-dataset analyses:
  - Compare broad-scale findings with detailed, higher-resolution measurements from the Landwise Detailed survey
  - Assess spatial variability patterns across land-use classes and soil/geology classes