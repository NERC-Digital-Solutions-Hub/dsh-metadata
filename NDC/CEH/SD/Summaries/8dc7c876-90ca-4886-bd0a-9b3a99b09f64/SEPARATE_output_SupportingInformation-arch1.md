# Source apportionment of annual nutrients and sediment loads to rivers in England and Wales modelled with SEPARATE

## Overview
- Dataset apportions annual loads of nitrogen, phosphorus, and fine-grained sediment to rivers at Water Framework Directive (WFD) waterbody scale.
- Modelled with SEPARATE version 2 (SEPARATOR Pollutant AppoRtionment for the AquaTic Environment).
- Includes emissions from diffuse sources (agriculture, urban, river channel banks, atmospheric deposition, groundwater) and point sources (sewage treatment works, septic tanks, combined sewer overflows, storm tanks).
- Data summarized by non-coastal WFD Cycle 2 waterbodies; covers individual and cumulative waterbodies.

## What is included
- Table 1: Modelled pollution sources (diffuse and point sources).
- Table 2: Modelled pollutants (nitrogen, phosphorus forms, and sediment).
- Table 3: File column names for the dataset.
- Emissions are provided for each pollutant and source, at local and cumulative scales.

## SEPARATE framework and inputs
- SEPARATE provides a national-scale, multi-pollutant source apportionment framework for England and Wales.
- Inputs are organised by pollutant-source categories and produced for non-coastal WFD Cycle 2 waterbodies, for both individual and cumulative waterbodies.

## Pollutant emissions by source

- Diffuse agricultural
  - Inputs generated with the ADAS Agricultural Pollutant Transfer (APT) framework, building on PSYCHIC and NIPPER models for phosphorus, sediment, and nitrogen.
  - Key inputs:
    - NSRI Natmap Soils Database
    - UK Met Office daily weather data (rainfall, temperature, sunshine hours, wind, vapor pressure)
    - Elevation data (altitude, slope)
    - 2010 June Agricultural Census crop data ( mapped to 1 km grid)
    - Field boundary features (Countryside Survey)
    - Manure and excreta distribution (MANURE-GIS)
    - 2010 British Survey of Fertiliser Practice (BSFP)

- Diffuse urban
  - Emissions derived from annual average urban runoff using the Wallingford Modified Rational Method plus representative event mean concentrations (EMCs) from published data.
  - Main inputs: rainfall and land cover/soil type data.

- Diffuse river channel banks
  - Emissions estimated using a national-scale bank erosion index updated to reflect geomorphological control via sinuosity.
  - Main inputs: river flow, HOST (Hydrology of Soil Types), and EA Detailed River Network (DRN).

- Direct atmospheric deposition
  - Nitrogen deposition estimated with NEAP-N; phosphorus deposition derived from rainfall phosphorus content (ECN monitoring) and average rainfall (1961–1990).

- Sewage treatment works (STWs)
  - Emissions estimated from a national register of consented discharges (n=~6790) with measured flows and pollutant concentrations (2010–2012).
  - Excludes STWs with mean daily discharges < 3 m3 or lacking discharge data.

- Septic tanks
  - Emissions taken from EA study on phosphorus emissions.

- Combined sewer overflows (CSOs)
  - Discharges informed by SAGIS framework; assumption: combined sewers can carry six times dry weather flow before CSOs discharge; discharge modeled as a function of rainfall, sewer capacity, surface permeability, and runoff entering the sewer.

- Storm tanks
  - Similar approach to CSOs; assumed storm tanks retain three times the dry weather flow before discharging.

## Uncertainty and limitations
- Results must be interpreted with multiple caveats when informing local decisions from national-scale evidence.
- Approximately 43% of waterbodies have areas <25 km2; results for these small waterbodies should be treated with caution due to data accuracy and up-scaling issues.
- Agricultural emissions represent a baseline with prior mitigation implemented for 2010–2012; a no-mitigation baseline is also provided.
- STW emissions reflect tightened permits and nutrient stripping (progressing toward 600 works by 2015); uncertainties remain for smaller STWs and for outfalls with multiple permits needing reconciliation with Environment Agency experts.
- STW emissions to estuarine/coastal environments are not included.
- Channel bank emissions do not account for bank protection works.
- Temporal coverage is not perfectly uniform (e.g., 2010 for agriculture, 2010–2012 for STWs).

## Data format and accessibility
- Stored in CSV format; mapable to GIS by joining to WFD River Waterbody Cycle 2 shapefiles using EA_WB_ID.
- Columns cover regional and catchment metadata, waterbody identifiers, local and cumulative areas, and pollutant load data.
- Example column types:
  - X_au_L_t: Agricultural unmitigated load (tonnes/year) – local
  - X_am_L_t: Agricultural mitigated load – local
  - X_be_L_t: Bank erosion load – local
  - X_ur_L_t: Urban diffuse load – local
  - X_sw_L_t: STW load – local
  - X_to_L_t: Waterbody total load – local
  - X_to_C_t: Waterbody total load – cumulative
  - X_am_L_p, X_be_L_p, etc.: corresponding percentages (local or cumulative)
- Supporting documentation and detailed methodology are provided via CEH and linked references.

## Usage notes and mapping
- The dataset is designed for policy support and scientific analysis, enabling attribution of nutrient and sediment loads to specific sources.
- Useful for comparing “diffuse” versus “point” source contributions and for exploring mitigation scenarios.
- When mapping to waterbodies, use the Waterbody IDs (wb_ID) to join with WFD Cycle 2 shapefiles and interpret local vs cumulative results.

## References and supporting documentation
- CEH dataset documentation and sources:
  - Source apportionment of annual nutrient and sediment loads to rivers in England and Wales, SEPARATE framework.
  - Supporting materials and methodology (including PSYCHIC, NIPPER, MODIFIED RATIONAL method, SAGIS, and related input datasets).
- Key references include published modelling work and data sources for agricultural loads, urban runoff, bank erosion, deposition, STWs, septic tanks, CSOs, storm tanks, and groundwater contributions.