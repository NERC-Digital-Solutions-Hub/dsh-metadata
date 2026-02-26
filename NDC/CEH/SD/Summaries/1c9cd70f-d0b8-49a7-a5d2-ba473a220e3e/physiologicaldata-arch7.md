# Metadata for physiology data

## Overview
- Three data sets derived from threespine sticklebacks from geothermal and ambient populations.
- Data cover physiology and behaviour measured in laboratory conditions: metabolism, sociability, and temperature preference.
- Collected data are based on published work by Pilakouta and colleagues (2020, 2023).
- Data intended for integration with GIS-ready workflows for map-based visualization and spatial analysis.

## Data sets

- Data set 1: Metabolism.csv
  - Context: Respirometry in a flow-through chamber over weeks to measure whole-body metabolism.
  - Key fields (six columns):
    - AcclimTemp: acclimation temperature in °C
    - PopTemp: habitat temperature category (Cold or Warm)
    - Pop: short site codes (e.g., Ashn, GTS, CSWY, Myv) with W/C suffix for Warm/Cold
    - PopPair: sympatric or allopatric population pairing
    - Mass: specimen weight in grams
    - SMR: standard metabolic rate in mg O2/hr

- Data set 2: Sociability.csv
  - Context: Lab-based tracking of social distances using video imaging; focal fish choices between conspecific ecotypes.
  - Key fields (nine columns):
    - populationpair: allopatric or sympatric
    - population: population name
    - HabitatTemp: thermal habitat at origin (Warm or Cold)
    - Temp: acclimation and trial temperature
    - ID: individual fish identifier
    - trial: trial number (1 or 2) at a given temperature
    - sociability: mean distance (cm) from stimulus shoal during 30-minute trial
  - Notes: Densities standardized across treatment groups.

- Data set 3: temperature preference.csv
  - Context: Temperature preference chamber assay over 24 hours to determine preferred temperature.
  - Key fields (seven columns):
    - Test date: date of data collection
    - Population: sympatric or allopatric grouping
    - Popn: population and habitat code as in Data set 1
    - TempPref: time spent in preferred temperature (minutes)
    - LogTempPref: log-transformed time in preferred temperature
    - Mass: weight in grams
    - LogMass: log-transformed weight

## Provenance and references
- Pilakouta et al. 2020. Multigenerational exposure to elevated temperatures leads to a reduction in standard metabolic rate in the wild. Functional Ecology, 34, 1205-1214.
- Pilakouta et al. 2023. Geothermal stickleback populations prefer cool water despite multigenerational exposure to a warm environment. Ecology and Evolution, 13, e9654.
- Pilakouta et al. 2023. A warmer environment can reduce sociability in an ectotherm. Global Change Biology, 29, 206-214.

## GIS considerations and potential map products
- Spatial linkage
  - Population names (Pop, Popn) and populationPair can be joined to geolocated population sites if coordinates are available.
  - Pop codes (e.g., Ashn, GTS, CSWY, Myv) can serve as spatial identifiers for mapping population-level attributes.
- Data harmonization
  - Ensure consistent naming across datasets (e.g., Pop, Popn, population) for joins.
  - Standardize temperature/habitat categories (Cold/Warm, Sympatric/Allopatric) for uniform mapping layers.
- Potential map-based products
  - Map of metabolic rate (SMR) by population, with filters for AcclimTemp and PopTemp.
  - Sociability distance map by population and temperature condition, showing variation across HabitatTemp and Temp.
  - Temperature preference visualization by population with mass-adjusted metrics (LogTempPref, LogMass).
  - Temporal facets showing changes across trials or test dates if time-series visualization is applied.
- Data integration tips
  - Attach geographic coordinates or shapefiles for Pop locations to enable spatial analyses (e.g., clustering, proximity to geothermal features).
  - Consider creating derived GIS attributes from PopPair and PopTemp to support tiered symbology (e.g., allopatric vs sympatric, cold vs warm).

## Data quality, notes, and usage guidance
- Outlier checks performed on temperature preference data; same individual collector to minimize observer bias (observer consistency noted for the dataset).
- Densities in the sociability study were standardized across treatment groups to reduce confounding effects.
- Data are lab-generated from wild-caught sticklebacks, with multi-generational exposure context provided in the references.
- Documentation links to three primary publications should accompany any GIS data products for methodological context.

## Access and citations
- Use the three Pilakouta et al. references to provide methodological context and to justify the linkage between phenotypic measures and environmental conditions when presenting map-based findings.