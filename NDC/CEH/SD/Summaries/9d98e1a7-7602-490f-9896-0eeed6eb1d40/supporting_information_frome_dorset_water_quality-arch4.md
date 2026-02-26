# Supporting information for dataset Water quality data for the River Frome catchment, Dorset, 1976-2022

## Access, licensing and citation
- Open Government Licence applies; dataset accessible via DOI link.
- Users must cite the dataset in publications describing research that used the data.
- Official citation: Homan, T. (2023). Water quality data for the River Frome catchment, Dorset, 1976-2022. NERC EDS Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/9d98e1a7-7602-490f-9896-0eeed6eb1d40

## What, where, when, how, why, who, completeness

- What: A compilation of water quality data for the River Frome catchment, Dorset, sourced from Environment Agency and Wessex Water.
- Where: 21 monitoring sites in the lower River Frome catchment (chalk stream in West Dorset), between Dorchester and East Stoke; sites include boreholes, STW final effluents, tributaries, and main river channels; each site has a British National Grid reference (NGR).
- When: Measurements 1976–2022; main river and tributaries typically monthly; STW final effluents typically weekly; borehole data weekly to monthly depending on determinand.
- How: Data retrieved from Environment Agency or Wessex Water archives or via request; some data openly available through linked portals.
- Why: Collected for a PhD project modelling nutrient fate and transport; used to analyze spatial/temporal trends and support hydrodynamic modelling.
- Who: Compiled by Thomas Homan (PhD candidate, University of Bath); acknowledgement to Wessex Water and Environment Agency; EA data provided under Open Government Licence.
- Completeness: Focused on Frome catchment determinands relevant to the PhD; not exhaustive; additional monitoring sites exist upstream and downstream beyond those listed.

## Method
- Data sources: EA and Wessex Water archives or direct requests.
- Analytical methods: Contact sources for detailed methods; no major methodological changes detected; checked for step changes; no obvious shifts.
- Data preparation: Cleaned and refined to sites/determinands of interest; removed sites/determinands with insufficient data.
- Site listing: Table 1 includes refined monitor sites, type, and NGRs (22 entries listed in the document, including boreholes, STW effluents, and various river/tributary sites).

## Details of data structure
- File: River_Frome_Dorset_water_quality.csv
- Key fields:
  - SMPT_SHORT_NAME, SMPT_GRID_REF: site identifier and grid reference
  - SAMPLE_DATE, SAMPLE_TIME: date and time of measurement
  - DETE_DESC: determinand description
  - MEAS_SIGN: indication of measurement relative to detection limit (< or >)
  - MEAS_RESULT: measured value
  - UNIT_DESC: units
  - SOURCE: data origin (WW = Wessex Water, EA = Environment Agency)

## Acknowledgements
- Data contributions from Environment Agency Water Quality Archive (Beta) and Wessex Water.
- Acknowledgement of EA data under the Open Government Licence.