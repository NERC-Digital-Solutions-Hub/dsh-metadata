# Supporting information for dataset Water quality data for the River Frome catchment, Dorset, 1976-2022

- Access, licensing and citation
  - Data are available under the Open Government Licence.
  - Accessed via the dataset DOI: 10.5285/9d98e1a7-7602-490f-9896-0eeed6eb1d40.
  - Users must cite the dataset in publications describing research using the data (Homan, 2023).
  - Publication guidance and licence terms are provided by the hosting repositories.

- What? Where? When? How? Why? Who? Completeness
  - What: A compilation of water quality data for the River Frome catchment, Dorset, sourced from the Environment Agency and Wessex Water.
  - Where: River Frome catchment in West Dorset; lower River Frome between Dorchester and East Stoke; 21 monitoring sites including boreholes, STW final effluents, tributaries, and main river sections; each site has a British National Grid reference.
  - When: Data from 1976–2022; main river and tributaries monitored monthly; STW final effluents weekly; borehole data weekly to monthly depending on determinand.
  - How: Data downloaded from Environment Agency or Wessex Water archives or obtained on request; some data openly accessible via linked portals.
  - Why: Compiled to support a PhD study modeling nutrient fate and transport; used to analyse spatial and temporal trends and to inform hydrodynamic modeling.
  - Who: Compiled by Thomas Homan (PhD candidate, University of Bath); thanks extended to Wessex Water and Environment Agency.
  - Completeness: Limited to Frome catchment determinands and sites aligned with the PhD objectives; not exhaustive; additional sites upstream of Dorchester and downstream from East Stoke exist but are not listed.

- Method
  - Data sources: EA and Wessex Water archives; some data provided on request.
  - Analytical methods: If needed, details can be obtained from the originating source; no separate methods were required for the reported work.
  - Quality checks: No formal QC described; the dataset was checked for obvious step changes (none found).
  - Data refinement: Cleaned and narrowed to monitoring sites and determinands of interest; sites/determinands with little data removed.
  - Table 1 (referenced in the document) lists the refined set of monitoring sites, their type (e.g., borehole, STW effluent, tributary, river), and their grid references.

- Details of data structure
  - Data file: River_Frome_Dorset_water_quality.csv.
  - Columns (as per Table 2): 
    - SMPT_SHORT_NAME (sample point short name)
    - SMPT_GRID_REF (sample point grid reference)
    - SAMPLE_DATE (date of measurement)
    - SAMPLE_TIME (time of measurement)
    - DETE_DESC (determinand description)
    - MEAS_SIGN (sign of measurement relative to reporting limit)
    - MEAS_RESULT (measurement value)
    - UNIT_DESC (units)
    - SOURCE (data source: WW = Wessex Water, EA = Environment Agency)

- Acknowledgements
  - Acknowledges Environment Agency Water Quality Archive (Beta) © EA for data.
  - Gratitude to Wessex Water for providing monitoring data from their assets.