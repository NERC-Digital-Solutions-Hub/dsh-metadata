# Supporting information for dataset Water quality data for the River Frome catchment, Dorset, 1976-2022

## 1 Access, licensing and citation
- Open Government Licence; dataset can be accessed via provided DOIs/links.
- Users must cite the dataset in any publication describing research using the data.
- Citation format: Homan, T. (2023). Water quality data for the River Frome catchment, Dorset, 1976-2022. NERC EDS Environmental Information Data Centre. Dataset. https://doi.org/… 

## 2.1 What?
- Compilation of water quality data for the River Frome catchment, Dorset.
- Data sourced from Environment Agency (EA) and Wessex Water Ltd.

## 2.2 Where?
- River Frome catchment in West Dorset, UK; lower Frome reach between Dorchester and East Stoke.
- 21 monitoring sites including boreholes, STW final effluents, tributaries, and main river channels.
- NI/NG references provided for each site.

## 2.3 When?
- Measurements span 1976–2022.
- Main river and tributaries: typically monthly.
- STW final effluents: typically weekly.
- Boreholes: weekly to monthly depending on determinand.

## 2.4 How?
- Data downloaded from EA or Wessex Water archives or received on request.
- Some data openly available via links; analytical methods available from data sources.
- Methods not always detailed in dataset; users should contact sources for specifics.
- Data were checked for obvious method changes; none detected.
- Dataset cleaned/refined to sites/d determinands of interest; Table 1 lists refined sites.

## 2.5 Why?
- Prepared for a PhD project modeling nutrient fate and transport in the River Frome.
- Used to analyse spatial/temporal trends and support hydrodynamic modeling.

## 2.6 Who?
- Compiled by Thomas Homan (PhD candidate, University of Bath).
- Acknowledges EA and Wessex Water for data contributions.
- EA data provided under the Open Government Licence.

## 2.7 Completeness?
- Dataset covers Frome catchment sites and determinands relevant to the PhD objectives.
- Not exhaustive: more sites exist upstream of Dorchester and below East Stoke; not all determinands are included.

## 3 Method
- Data sourced as above; analytical methods per determinand available from corresponding sources.
- Due to dataset length/varied sources, notable method changes were not identified.
- Data cleaned to keep only relevant sites and determinands; little-used data removed.
- Refined site list and structure summarized in Table 1 (provided in the dataset).

### 3.1 Quality control
- No formal QC in this document; authors conducted basic checks for step changes (no changes detected).

## 4 Details of data structure
- Single CSV file: River_Frome_Dorset_water_quality.csv
- Key fields (Table 2):
  - SMPT_SHORT_NAME: sample point short name
  - SMPT_GRID_REF: British National Grid reference
  - SAMPLE_DATE, SAMPLE_TIME: measurement date/time
  - DETE_DESC: determinand description
  - MEAS_SIGN: < or > for reporting limits
  - MEAS_RESULT: measurement value
  - UNIT_DESC: units
  - SOURCE: data source (WW = Wessex Water; EA = Environment Agency)

## 5 Acknowledgements
- Data from Environment Agency Water Quality Archive (Beta) © EA.
- Gratitude to Wessex Water for providing monitoring data.