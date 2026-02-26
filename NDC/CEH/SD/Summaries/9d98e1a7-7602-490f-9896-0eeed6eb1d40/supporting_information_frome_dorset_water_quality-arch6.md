# Supporting information for dataset Water quality data for the River Frome catchment, Dorset, 1976-2022

## Overview
- Compilation of water quality data for the River Frome catchment, Dorset, sourced from the Environment Agency (EA) and Wessex Water.
- Created as part of a PhD project to hydrodynamically model nutrient fate and transport; used to analyse spatial and temporal trends and support the model.
- Time period: 1976–2022; 21 monitoring sites (lower River Frome), with monthly measurements on main river and tributaries, weekly to monthly measurements for STW final effluents, and borehole data varying by determinand.

## Access, licensing and citation
- Data available under the Open Government Licence.
- Access/download via:
  - https://environment.data.gov.uk/water-quality/view/landing
  - https://marketplace.wessexwater.co.uk/dataset
- Cite as: Homan, T. (2023). Water quality data for the River Frome catchment, Dorset, 1976-2022. NERC EDS Environmental Information Data Centre. Dataset. https://doi.org/10.5285/9d98e1a7-7602-490f-9896-0eeed6eb1d40

## Dataset content and scope
- What: Water quality measurements for the River Frome catchment, compiled from EA and Wessex Water data archives.
- Where: Lower River Frome catchment, West Dorset, UK; monitoring sites located between Dorchester and East Stoke (21 sites listed in the original dataset; NGRs provided).
- When: Measurements 1976–2022; main river and tributaries typically monthly; STW final effluents weekly; boreholes weekly to monthly depending on determinand.
- Why: To support hydrodynamic modelling and analysis of spatial/temporal trends.
- Who: Compiled by Thomas Homan (PhD candidate, University of Bath); EA and Wessex Water data providers acknowledged.

## Data sources and collection
- Data retrieved from EA and Wessex Water archives or provided on request; some data openly available via links.
- If needed, analytical methods for determinands can be obtained by contacting the respective data source.
- The dataset was checked for obvious step changes in methods; none found.

## Data structure and contents
- Format: Single CSV file named River_Frome_Dorset_water_quality.csv.
- Key fields (Table 2 in the source):
  - SMPT_SHORT_NAME: sample point short name
  - SMPT_GRID_REF: British National Grid reference for the sample point
  - SAMPLE_DATE, SAMPLE_TIME: date and time of measurement
  - DETE_DESC: determinand description
  - MEAS_SIGN: sign of measurement relative to reporting limit (< or >)
  - MEAS_RESULT: measurement value
  - UNIT_DESC: units of measurement
  - SOURCE: origin of measurement (WW = Wessex Water, EA = Environment Agency)
- Table 1 (listed in the document) provides the monitoring site list with type (Borehole, STW effluent, Tributary, River Frome) and grid references.

## Completeness and limitations
- Completeness: dataset covers Frome catchment determinands relevant to the PhD objectives; not an exhaustive list of determinands for the catchment. More monitoring sites exist upstream of Dorchester and below East Stoke.
- Data coverage may vary by site and determinand; some sites or data points may have limited data.

## Quality control
- No formal QA procedures described beyond broad validation (checking for apparent method changes). No explicit step changes detected in the data.

## Usage guidance
- Suitable for analyzing spatial and temporal water quality trends within the River Frome catchment and to support hydrodynamic modelling.
- For detailed analytical methods per determinand, contact the data sources (EA or Wessex Water).
- Acknowledge data sources and license when using the dataset; cite as provided.

## Acknowledgements
- Acknowledges Environment Agency Water Quality Archive (Beta) data and Wessex Water data contributions.