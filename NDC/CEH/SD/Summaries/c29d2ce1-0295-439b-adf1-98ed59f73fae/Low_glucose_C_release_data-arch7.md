# Time series of microbial carbon release from soil as carbon dioxide under different nitrogen and phosphorus treatments with a low glucose concentration added as a carbon source in the Conwy catchment, North Wales, UK (2015)

## Overview
- Dataset documenting microbial carbon mineralization as CO2 from soil using 14C-glucose under four nutrient treatments (Control, N, P, N&P) in the Conwy catchment, North Wales, UK, 2015.
- Time-series measurements captured over up to 1008 hours (approximately 6 weeks) using NaOH traps and liquid scintillation counting.
- Applicable for GIS-based visualization of spatial (plot locations) and depth-resolved (top, mid, subsoil) carbon release dynamics under different nutrient inputs.

## Data sources and structure
- Primary time-series data: Low_glucose_C_release_data.csv (14CO2 release over time).
- Metadata and quality: Low_glucose_C_release_data_metadata.csv (data field descriptions) and related quality control/reference data.
- Plot locations: Plot_locations.csv (boresite coordinates and cage/plot references) with Plot_locations_metadata.rtf describing fields.
- Supporting context: Miscellaneous supporting documents and standard abbreviations used (HWMC, N, P, etc.).
- Application data details: Treatment combinations include Low concentration glucose with 0.006 mM C addition across four treatments:
  - Control (no N or P)
  - N only
  - P only
  - N & P
- Data quality notes: Empty cells indicate missing data.

## Spatial and sampling coverage
- Spatial area: Conwy catchment, North Wales, UK.
- Plot-level locations and borehole references provided in Plot_locations.csv (Transect and Row fields link to cage locations in Plot_locations.csv).
- Depth resolution: Soil cores divided into depth intervals and later grouped into:
  - Topsoil: 0–30 cm (0–15 cm and 15–30 cm segments)
  - Midsoil: 50–100 cm
  - Subsoil: 100–300 cm (100–150, 150–200, 250–300 cm)
- Each plot/Transect/Row combination captures multiple depths for time-series data.

## Measurements and methods
- Substrate and incubation: 5 g dry-weight soil per sample; 14C-glucose added to the soil surface.
- CO2 capture: NaOH trap (1 M) positioned in each tube to absorb evolved 14CO2.
- Incubation conditions: 10°C to reflect mean annual catchment temperature.
- Duration and sampling schedule: Traps changed at multiple time points and then weekly for up to 6 weeks (0.5, 1, 2, 4, 6, 24, 48, 72, 96, 120, 144, 168, 192, 336, 504, 672, 840, 1008 hours).
- Measurement: Captured 14CO2 quantified by liquid scintillation counting (Wallac 1404).

## Data fields and structure
- Core identifiers: Transect (plot reference), Row (cage/plot reference), Depth (cm).
- Time-series fields: DPM counts for each time interval (e.g., 0.5 hr, 1 hr, 2 hr, 4 hr, 6 hr, 24 hr, 48 hr, 72 hr, 96 hr, 120 hr, 144 hr, 168 hr, 192 hr, 288 hr, 336 hr, 504 hr, 672 hr, 840 hr, 1008 hr).
- Data status: Empty cells indicate no data for that transect/depth/time point.

## Data quality and caveats
- Metadata file provides quality control and reference details for the Low_glucose_C_release_data.csv dataset.
- Data may contain gaps (empty cells) where measurements were not available.
- Plot and depth alignment relies on Plot_locations.csv; discrepancies between files may require alignment via Transect/Row references.

## GIS applications and integration
- Suitable for creating map-based visualizations of spatial patterns in carbon mineralization across plots, depths, and nutrient treatments.
- Can be joined with Plot_locations.csv to map temporal changes in 14CO2 release by location and depth.
- Time-series data enable 3D GIS analyses (horizontal plot locations plus vertical depth; time as an additional dimension) to explore treatment effects and depth-dependent responses.
- Useful for policy or stakeholder-facing maps showing soil carbon dynamics under nitrogen and phosphorus inputs.

## References and metadata
- Plot locations and descriptions: Plot_locations.csv with Plot_locations_metadata.rtf describing field definitions.
- Metadata and quality documentation: Low_glucose_C_release_data_metadata.csv (and quality control/reference data files).
- Abbreviations and supporting documents provided to aid data interpretation (e.g., HWMC, N, P).