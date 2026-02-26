# Supporting information for dataset Water quality data for the River Frome catchment, Dorset, 1976-2022

## Overview
- Compilation of water quality data for the River Frome catchment in Dorset, sourced from the Environment Agency (EA) and Wessex Water.
- Aimed to support hydrodynamic modeling of nutrient fate and transport and to analyze spatial and temporal trends along the reach.

## Geography and sites
- Focused on the lower River Frome catchment in West Dorset, between Dorchester and East Stoke.
- 21 monitoring sites, including boreholes, sewage treatment works (STW) final effluents, tributaries, and main river sections.
- Sites are identified by British National Grid references (NGRs) and include examples such as Belhuish (borehole), Dorchester STW FE, Tadnoll Brook (tributary), East Stoke (River Frome), and Wool Bridge (River Frome).

## Temporal scope and sampling
- Data cover 1976–2022.
- Main river and tributaries typically monitored monthly.
- STW final effluents monitored weekly.
- Boreholes monitored weekly to monthly depending on determinand and borehole.

## Data access, licensing, and citation
- Open Government Licence (OGL) terms; dataset accessible via provided DOIs/links.
- Must cite the dataset in publications describing research using the data.
- Cite as: Homan, T. (2023). Water quality data for the River Frome catchment, Dorset, 1976-2022. NERC EDS Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/9d98e1a7-7602-490f-9896-0eeed6eb1d40
- Access links include Environment Agency water-quality portal and Wessex Water data marketplace.

## Data content and determinands
- Determinand data extracted from EA and Wessex Water archives; not an exhaustive list for the catchment.
- The dataset focuses on determinands relevant to the PhD study (nutrients and related water quality parameters).
- Data structure described below; more analytical methods details available from the data sources upon request.

## Data structure and contents
- Single CSV file: River_Frome_Dorset_water_quality.csv
- Key fields (Table 2):
  - SMPT_SHORT_NAME: sample point short name
  - SMPT_GRID_REF: sample point grid reference (NGR)
  - SAMPLE_DATE: date of measurement
  - SAMPLE_TIME: time of measurement
  - DETE_DESC: determinand description
  - MEAS_SIGN: sign indicating reporting limit (< or >) if applicable
  - MEAS_RESULT: measurement value
  - UNIT_DESC: units of measurement
  - SOURCE: data origin (WW = Wessex Water, EA = Environment Agency)

## Data quality and processing
- No formal quality control section described (N/A).
- Data were cleaned and refined to the selected monitoring sites and determinands.
- Checked for obvious step changes in analytical method; none found.
- Determinands or sites with sparse data removed to focus on relevant objectives.
- The refined site list and their types are documented (Table 1 in the dataset).

## Completeness and limitations
- Coverage limited to the Frome catchment and determinands aligned with the PhD objectives.
- Not all potential sites in the catchment are included; there are more sites upstream of Dorchester and downstream of East Stoke than listed.
- Analytical methods for each determinand are not exhaustively documented in this summary; contact source agencies for method details.

## Acknowledgements and provenance
- Data from the Environment Agency Water Quality Archive (Beta) © EA.
- Gratitude to Wessex Water for supplying data from their assets.
- EA data provided under Open Government Licence.

## Relevance for environmental monitoring and policy analysis
- Provides a standardized, time-spanned data resource to assess spatial and temporal water quality trends in a defined catchment.
- Supports integration with other datasets and broader data portals to increase data value and accessibility for monitoring and policy evaluation.
- Useful for analytical workflows aimed at environmental health assessment, trend analysis, and calibration/validation of hydrodynamic models.