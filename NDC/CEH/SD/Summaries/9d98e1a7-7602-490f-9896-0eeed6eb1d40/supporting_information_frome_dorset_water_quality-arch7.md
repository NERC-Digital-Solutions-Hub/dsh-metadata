# Supporting information for dataset Water quality data for the River Frome catchment, Dorset, 1976-2022

## Overview
- Compilation of water quality data for the River Frome catchment in Dorset, sourced from the Environment Agency (EA) and Wessex Water.
- Created to support hydrodynamic modelling of nutrient fate and transport; used to analyse spatial and temporal trends.

## Spatial and temporal coverage
- Study area: lower River Frome catchment, chalk stream in West Dorset, between Dorchester and East Stoke.
- 21 monitoring sites at boreholes, STW final effluents, tributaries, and main river channels; sites have British National Grid references (NGRs).
- Measurement period: 1976–2022.
- Sampling frequency: main river channel and tributaries typically monthly; STW final effluents weekly; boreholes weekly to monthly depending on determinand.

## Data sources and access
- Data downloaded from EA and Wessex Water archives or provided on request.
- Some data openly accessible via:
  - Environment Agency water quality landing page
  - Wessex Water marketplace dataset
- Analytical methods: not all methods detailed in this summary; users should contact data sources for method specifics.

## Data structure and contents
- File: River_Frome_Dorset_water_quality.csv
- Key fields:
  - SMPT_SHORT_NAME: sample point short name
  - SMPT_GRID_REF: sample point grid reference (NGR)
  - SAMPLE_DATE, SAMPLE_TIME: date and time of measurement
  - DETE_DESC: determinand description
  - MEAS_SIGN: sign of measurement relative to reporting limit
  - MEAS_RESULT: measurement value
  - UNIT_DESC: units
  - SOURCE: data origin (WW = Wessex Water, EA = Environment Agency)

## Data quality and processing
- Data were cleaned and refined to sites and determinands of interest; determinands/sites with little data were removed.
- Checked for obvious method changes (no major step changes detected); analytical methods details available from original sources if required.
- Table 1 in the dataset lists the refined monitoring sites, their type, and NGRs.

## Completeness and limitations
- Focused only on Frome catchment sites and determinands relevant to the underlying PhD study; not an exhaustive set.
- More monitoring sites exist upstream of Dorchester and below East Stoke that are not included.
- Completeness varies by site and determinand.

## Licensing and citation
- Data available under the Open Government Licence (OGL v3).
- Users must cite the dataset in publications describing research that used the data.
- Citation format provided in the document:
  Homan, T. (2023). Water quality data for the River Frome catchment, Dorset, 1976-2022. NERC EDS Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/9d98e1a7-7602-490f-9896-0eeed6eb1d40

## How to use in GIS and related workflows
- The dataset provides geolocated sample points (NGRs) and time-series measurements suitable for map-based visualisations and spatial analyses.
- Use the CSV with NGRs to join to river network shapefiles or catchment boundaries; plot determinands over time for trend analysis.
- Be mindful of gaps in data coverage and the non-exhaustive list of determinands when planning GIS analyses or modelling inputs.

## Acknowledgements
- Acknowledges Environment Agency water quality data from the Water Quality Archive (Beta) and Wessex Water data contributions.