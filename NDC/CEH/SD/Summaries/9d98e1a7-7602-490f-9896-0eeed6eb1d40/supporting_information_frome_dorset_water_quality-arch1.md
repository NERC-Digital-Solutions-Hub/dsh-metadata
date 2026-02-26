# Supporting information for dataset Water quality data for the River Frome catchment, Dorset, 1976-2022

## Overview
- Compilation of water quality data for the River Frome catchment in Dorset.
- Sourced from the Environment Agency (EA) and Wessex Water.
- Time period: 1976–2022.
- 21 monitoring sites (boreholes, STW final effluents, tributaries, and main river channels) in the lower River Frome between Dorchester and East Stoke.
- Data collected monthly (main river and tributaries) and weekly (STW final effluents); borehole data range from weekly to monthly depending on determinand.

## Data sources and licensing
- Data are available under the Open Government Licence.
- Access via the dataset DOI: 10.5285/9d98e1a7-7602-490f-9896-0eeed6eb1d40.
- Data cited as Homan, T. (2023). Water quality data for the River Frome catchment, Dorset, 1976-2022. NERC EDS Environmental Information Data Centre.
- EA data provided under the Open Government Licence; acknowledgments to EA and Wessex Water.

## Geographic and temporal scope
- Location: River Frome catchment, West Dorset, UK (lower River Frome between Dorchester and East Stoke).
- Monitoring sites include boreholes, STW effluent sites, tributaries, and main river sections.
- 1976–2022 time span for measurements; site coverage and determinands reflect the PhD study aims rather than an exhaustive survey of the entire catchment.

## Data collection and access
- Data downloaded from EA or Wessex Water archives or provided on request.
- Some data are openly accessible via:
  - Environment Agency water quality landing page
  - Wessex Water marketplace dataset
- For detailed analytical methods per determinand, contact the respective data source.

## Data structure and content
- Single CSV file: River_Frome_Dorset_water_quality.csv.
- Key fields:
  - SMPT_SHORT_NAME: sample point short name
  - SMPT_GRID_REF: British National Grid reference
  - SAMPLE_DATE: date of measurement
  - SAMPLE_TIME: time of measurement
  - DETE_DESC: determinand description
  - MEAS_SIGN: sign relative to reporting limit (e.g., < or >)
  - MEAS_RESULT: measurement value
  - UNIT_DESC: units
  - SOURCE: data origin (WW = Wessex Water, EA = Environment Agency)
- Table 1 lists 21 monitoring sites with type (Borehole, STW effluent, Tributary, River Frome) and grid references.
- Table 2 (implied) documents the data structure and field descriptions.

## Data quality and preprocessing
- Dataset was cleaned and refined to the monitoring sites and determinands relevant to the PhD objectives.
- Determinands and sites with little data were removed.
- Checked for obvious step changes in analytical methods by comparing data length and transitions; none detected.
- If analytical-method specifics are required, contact the data sources; method details were not central to the work.

## Completeness and limitations
- Completeness: focuses on Frome catchment sites and determinands aligned with the PhD objectives; not exhaustive for the catchment.
- There are more monitoring sites than those listed, notably upstream of Dorchester and downstream of East Stoke.
- Some data determinands are not represented at every site due to objective-driven selection.

## Usage notes
- The dataset supports analysis of spatial and temporal trends and model development for nutrient fate and transport in the River Frome.
- Primary citation and licensing requirements apply; cite Homan (2023) when used.

## Acknowledgements
- Data from Environment Agency Water Quality Archive (Beta) © EA.
- Gratitude to Wessex Water for providing data from their assets.