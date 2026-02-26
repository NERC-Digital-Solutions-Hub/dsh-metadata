# UK Environmental Change Network (ECN) soil solution chemistry data: 1992-2012

## Overview
- A dataset of soil solution chemistry measurements collected from ECN sites between 1992 and 2012.
- Intended for map-based exploration and GIS analyses of environmental change indicators.

## Data provenance
- Dataset Originator: ECN Data Centre, Centre for Ecology and Hydrology (ECN data site: data.ecn.ac.uk)
- Data Providers: UK ECN programme funded by a consortium of government departments and agencies
- Usage acknowledgement: Users should acknowledge data and send one reprint of any publication citing the data

## Protocol and sampling details
- Sampling method: Suction samplers used to measure soil solution chemistry
- Cadence: Fortnightly sampling
- Replicates: RID (replicate ID) used; new RID issued when a sampler is replaced
- Bulk sampling: If insufficient sample collected, samples for a day may be bulked and tagged with RID XXS (shallow) or XXD (deep)
- Quality control: A standard QC solution analyzed alongside field samples; QC data included with the dataset
- Data quality: Use the accompanying quality information for proper data interpretation

## Data model and structure
- Core structure: SITECODE, SDATE, RID, FIELDNAME, VALUE
  - SITECODE: ECN site code
  - SDATE: sampling date
  - RID: replicate ID
  - FIELDNAME: measured variable
  - VALUE: measured value

## Site codes and spatial/temporal coverage
- 12 ECN sites (T01–T12) with site names, coordinates, and dataset date ranges
  - Examples: Drayton, Glensaugh, Hillsborough, Moor House - Upper Teesdale, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Snowdon, Cairngorms
- Date ranges vary by site, spanning roughly 1992–2012 (with some sites ending earlier in 2000–2012)
- Spatial data provided via precise coordinates for each site

## Field measurements and units
- Alkalinity (ALKY) – mg/L
- Aluminium (ALUMINIUM) – mg/L
- Calcium (CALCIUM) – mg/L
- Chloride (CHLORIDE) – mg/L
- Colour (COLOUR) – absorbance at 436 nm (nM)
- Conductivity (CONDY) – µS/cm
- Dissolved organic carbon (DOC) – mg/L
- Iron (IRON) – mg/L
- Magnesium (MAGNESIUM) – mg/L
- Ammonium (NH4N) – mg/L
- Nitrate nitrogen (NO3N) – mg/L
- pH (PH) – pH units (1–14)
- Aquacheck pH (PHAQCS, PHAQCU) – pH (1–14), stirred and unstirred
- Phosphate phosphorus (PO4P) – mg/L
- Potassium (POTASSIUM) – mg/L
- Sulphate (SO4S) – mg/L
- Sodium (SODIUM) – mg/L
- Total nitrogen (TOTALN) – mg/L
- Total phosphorus (TOTALP) – mg/L
- Vacuum (VACUUM) – bar
- Volume (VOLUME) – mL
- Quality codes (Q1–Q5) – quality indicators (details in accompanying quality information)
- Note: Some variables have multiple related measurements (e.g., pH by different methods)

## Quality management and guidance
- ECN site managers assign standard quality codes to flag data quality concerns
- Codes cover issues like no information, sample loss, equipment problems, weather impacts, laboratory issues, etc.
- Unusual events may be described in accompanying quality text (code 999)
- Always review the associated quality information before analysis

## Supporting and additional documentation
- Supporting documentation: ECN soil solution chemistry data: 1992-2012 (doi provided)
- Additional dataset information: ECN_SS2.csv outlines the timing and lab metadata for analyses (FROMDATE, FROMHOUR, FROMMINUTE, SDATE, SHOUR, SMINS, LAB_NID, PHDATE, PHHOUR, PHMINS, FILTDATE, COMPDATE)

## Data use and access considerations for GIS work
- Data are multi-site, multi-year, and multi-measure, requiring careful harmonization of sites, dates, and units
- Account for replicate IDs and potential bulked samples (XXS/XXD) in spatial-temporal analyses
- Integrate quality codes to filter or weight data according to reliability
- Acknowledge data sources and reference accompanying QC information and protocol documentation for accurate mapping and interpretation

## Access and acknowledgement requirements
- Acknowledge ECN data usage
- Provide one reprint of any publication citing the dataset
- Consult accompanying protocol and QC documentation for correct data handling and interpretation