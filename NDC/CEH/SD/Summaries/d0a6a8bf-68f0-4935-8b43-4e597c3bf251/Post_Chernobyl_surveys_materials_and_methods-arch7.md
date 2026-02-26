# Metadata for datasets available from Chaplow et al. (2015): Chaplow, J.S., Beresford, N.A., Barnett, C.L. (2015). Post Chernobyl surveys of radiocaesium in soil, vegetation, wildlife and fungi in Great Britain. NERC Environmental Information Data Centre. http://doi.org/10.5285/d0a6a8bf-68f0-4935-8b434e597c3bf251

## Overview
- Metadata for five CSV datasets documenting radiocaesium (Cs-134 and Cs-137) in soil, vegetation, wildlife, and fungi across Great Britain.
- Timeframe spans surveys conducted 1986–1997, with multiple sampling campaigns and sites.
- Includes detailed sampling methods, analytical procedures, and a wide range of environmental and sample-specific variables.
- Primarily intended for spatial analysis and map-based data products in GIS.

## Datasets included
- 1_Post_Chernobyl_survey_data_radiocaesium_in_soil_vegetation_wildlife_1986_and_1987.csv
- 2_Post_Chernobyl_survey_data_radiocaesium_in_vegetation_1986_1987_1988.csv
- 3_Post_Chernobyl_survey_data_radiocaesium_in_soil_and_vegetation_1989_and_1990.csv
- 4_Post_Chernobyl_survey_data_radiocaesium_in_soil_and_vegetation_1992.csv
- 5_Post_Chernobyl_survey_data radiocaesium in fungi 1994 to 1997.csv

## Spatial and temporal coverage
- Geographic scope: Great Britain (GB).
- Spatial identifiers include latitude, longitude, location descriptions, and CEH/ITE site codes.
- Temporal coverage: sampling events from 1986–1997 across different regions/sites.

## Key variables and units (GIS-relevant)
- Spatial coordinates: Latitude, Longitude, Location description.
- Sample context: Site name/CEH code, Sampling_date (yyyymmdd).
- Sample metadata: Sample_type (soil, vegetation, wildlife, fungi), Habitat (open ground, woodland), Soil_classification, Soil_pH (lower/upper), Soil_texture (lower/upper), Upper_bulk_density, Bulk_density (soil layers), LOI (loss on ignition).
- Radiocaesium measurements:
  - Cs-134 and Cs-137 activity concentrations in various media (e.g., soil, vegetation, gut contents, flesh).
  - Units include Bq/kg dry weight (Bq/kgDM), Bq/kg fresh, Bq/m2 (deposited), and Bq/kg_dw for soils and organic/ mineral layers.
  - For soils, measurements are provided for 0–4 cm topsoil and below 4 cm depth, plus total soil Cs deposits (Bq/m2) and bulk densities.
- Additional measurements: K-40, Pu isotopes, Ru isotopes, NH4, NH4, pH, trace elements, etc., in some datasets or variables.
- Data quality indicators: MDA (minimum detectable activity) notes and data availability indicators (e.g., some fields not applicable or not measured).

## Materials and methods (highlights)
- Sampling favored grassy/graminaceous vegetation; samples collected away from roadsides and overhanging vegetation to minimize contamination.
- Wildlife and diet samples collected (various herbivores and carnivores) to assess uptake and transferred radiocaesium.
- Vegetation sampling by clipping within 1 m2 plots; drying and grinding for analysis.
- Soil sampling: 20 x 20 x 15 cm blocks from plot centers; handling of litter layer and horizons; cold storage before processing.
- Gamma spectroscopy used for radiocaesium (Ge detectors; 20–25% efficiency; calibration against standards; decay corrected to sampling date).
- Comprehensive metadata fields link sample IDs to site codes, sampling dates, and analytical details.

## Data structure and readiness for GIS
- Data are organized in CSV format with a wide array of fields suitable for GIS joins and map creation.
- Key GIS-ready aspects:
  - Spatial coordinates (latitude/longitude) for point mapping.
  - Depth-specific layers (0–4 cm topsoil vs below 4 cm) enabling construction of stratified maps.
  - Depositional metrics (Bq/m2) and media-specific activity concentrations (Cs-134, Cs-137) for thematic mapping.
  - Habitat, soil type, and land classification attributes enabling contextual map layers and spatial analyses.
- Considerations for GIS use:
  - Units vary by media and context; ensure consistent unit handling during joins and calculations.
  - Some fields include metadata notes (e.g., MDA notations or not sampled), which may require data cleaning or filtering for certain analyses.
  - Multi-year data allow time-series mapping and trend analysis across sites.

## How GIS Specialists can use this data
- Create spatially explicit maps of radiocaesium deposition and uptake across GB over time.
- Build separate layers for Cs-134 and Cs-137 in soil, vegetation, and wildlife, with depth stratification (0–4 cm vs deeper).
- Combine radiocaesium layers with habitat, soil type, land-cover, and topography to analyze drivers of contamination and exposure.
- Develop interactive dashboards showing site-specific time series, concentration trends, and spatial distribution of Cs-134 and Cs-137.
- Integrate with other GIS datasets (e.g., soil maps, land use, wildlife distribution) for risk assessments and policy briefings.
- Perform quality-controlled data integration by joining on CEH/ITE site codes, sampling dates, and sample IDs.

## Access and provenance
- Data are provided as CSV files described above.
- Source: Chaplow et al. (2015), Post Chernobyl surveys of radiocaesium in soil, vegetation, wildlife and fungi in Great Britain.
- Repository: NERC Environmental Information Data Centre (EIDC); DOI/URL provided in the metadata.