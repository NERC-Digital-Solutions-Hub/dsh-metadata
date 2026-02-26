# UK Environmental Change Network (ECN) soil solution chemistry data: 1992-2012

## Overview
- This dataset presents soil solution chemistry measurements from the UK Environmental Change Network (ECN) across multiple sites and years (1992–2012).
- Data originator: ECN Data Centre (Centre for Ecology and Hydrology).
- Data providers: Consortium of UK government departments and agencies sponsoring ECN monitoring and coordination.
- Acknowledgment: Users should acknowledge the use of ECN data and send one reprint of any publication citing the data.

## Data Provenance and Governance
- Sponsoring organisations include: Agri-Food and Biosciences Institute; BBSRC; Natural Resources Wales; DSTL; DEFRA; Environment Agency; Forestry Commission; Welsh Government; Natural England; NERC; Northern Ireland Environment Agency; Scottish Environment Protection Agency; Scottish Government; Scottish Natural Heritage.
- ECN encourages acknowledgment of data use and sharing a reprint of publications that cite ECN data.

## Protocol and Sampling
- Sampling method: Suction samplers used to measure soil solution chemistry.
- Frequency: Fortnightly samples.
- Replication: Samplers can be replaced; new replicate ID (RID) assigned when replacement occurs.
- Bulk sampling: If insufficient sample, days’ samples may be bulked with RID codes XXS (shallow) or XXD (deep).
- Quality checks: A standard QC solution is analysed alongside field samples; QC data accompany the dataset and should be used as part of data quality assessment.

## Data Structure and Content
- Core data fields:
  - SITECODE: Unique ECN site code
  - SDATE: Sampling date
  - RID: Replicate ID
  - FIELDNAME: Variable measured
  - VALUE: Measured value
- Site Codes (12 sites): Drayton, Glensaugh, Hillsborough, Moor House - Upper Teesdale, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Y Wyddfa - Snowdon, Cairngorms
  - Each site entry includes site name, location (latitude/longitude), and dataset date range (e.g., Drayton 1993–2012, Cairngorms 1999–2012).
- Fieldnames (selected examples with units):
  - ALKY: Alkalinity (mg/L)
  - ALUMINIUM: Aluminium (mg/L)
  - CALCIUM: Calcium (mg/L)
  - CHLORIDE: Chloride (mg/L)
  - COLOUR: Absorbance at 436 nm (nM)
  - CONDY: Conductivity (µS/cm)
  - DOC: Dissolved organic carbon (mg/L)
  - IRON: Iron (mg/L)
  - MAGNESIUM: Magnesium (mg/L)
  - NH4N: Ammonium (mg/L)
  - NO3N: Nitrate nitrogen (mg/L)
  - PH: pH
  - PHAQCS/PHAQCU: Aquacheck system pH (stirred/unstirred)
  - PO4P: Phosphate phosphorus (mg/L)
  - POTASSIUM: Potassium (mg/L)
  - SO4S: Sulphate (mg/L)
  - SODIUM: Sodium (mg/L)
  - TOTALN: Total nitrogen (mg/L)
  - TOTALP: Total dissolved phosphorus (mg/L)
  - VACUUM: Residual vacuum at sampling
  - VOLUME: Volume of sample collected (mL)
  - Q1–Q5: Quality codes (see below)
- Additional analytical information: Supplementary dataset ECN_SS2.csv provides timing and lab information for analyses (FROMDATE, FROMHOUR, FROMMINUTE, SDATE, SHOUR, SMINS, LAB_NID, PHDATE, etc.).

## Metadata, Documentation, and Quality Information
- Supporting documentation: "UK Environmental Change Network (ECN) soil solution chemistry data: 1992-2012" (doi: 10.5285/456c24dd-0fe8-46c0-8ba5-855c001bc05f).
- Additional notes: Quality information accompanies the dataset; use these quality details for data interpretation and filtering.
- Quality Codes: ECN site managers assign standard quality codes (listed below) to indicate data quality factors. If an unusual event occurs not covered by codes, code 999 is used with accompanying text.
  - 100: No information available – data lost
  - 101: No sample/reading taken – equipment out of action
  - 102: Sample lost or discarded
  - 103: Partial loss of sample
  - 104: Sample frozen on collection
  - 106: Snow during sampling
  - 108: Insects in sample
  - 110: Soil in sample
  - 111: Unidentified debris in sample
  - 113: Sample discoloured
  - 115: Heather burning nearby
  - 122–126: Equipment/collection issues (e.g., funnel/clip/tubing problems)
  - 137: Flooding of survey area
  - 140: Application of chemicals (details provided)
  - 160: Pitfall trap damaged
  - 182: Snow/sleet during sampling
  - 200–201: Adverse weather or biting insects affecting sampling
  - 222–223: Non-standard sampling date/time
  - 501–507: Laboratory-related issues (no sample, loss, contamination, pre-filtered, etc.)
  - 508–509: Material deposits on filters
  - 511: No separate acidified subsample for Al and Fe
  - 999: Unusual event – see accompanying quality text

## Access, Citations, and Usage Guidance
- Researchers should acknowledge ECN data use and provide a reprint of any publication citing the data.
- The dataset includes a comprehensive quality and metadata framework to support data-driven decisions and cross-site data integration.

## Relevance for Data Leadership and Strategy
- Supports end-to-end data stewardship: clear provenance, multi-site long-term time series, standardized field definitions, and robust quality metadata.
- Enables system-wide data understanding: site-level context, replication identifiers, and data-quality codes facilitate governance and prioritization.
- Encourages co-ownership and collaboration: standardized data products and acknowledgement practices support cross-network coordination and data sharing.
- Highlights challenges relevant to data strategy: dispersed data across sites, variable data quality, metadata gaps, and need for consistent standards and discoverability.