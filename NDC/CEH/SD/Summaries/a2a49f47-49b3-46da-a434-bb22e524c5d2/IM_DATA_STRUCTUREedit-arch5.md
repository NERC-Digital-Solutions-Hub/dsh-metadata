# ECN Moth Trap Dataset Documentation

- Dataset Originator: ECN Data Centre, Centre for Ecology and Hydrology (http://data.ecn.ac.uk; ecn@ceh.ac.uk)
- Dataset Owners: UK Environmental Change Network (ECN) programme; funded by a consortium of UK government departments and agencies including Agri-Food and Biosciences Institute, BBSRC, Cyfoeth Naturiol Cymru, Dstl, DEFRA, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, NIEA, SEPA, Scottish Government, and Scottish Natural Heritage
- Purpose for data stewardship: ECN requests acknowledgement of data use and one reprint of any publications citing ECN data; governance and attribution are essential for demonstrating data value and impact

## Purpose and Stewardship Focus

- Ensures datasets are discoverable, properly attributed, and used to understand environmental change
- Documents that data are collected and managed under standard procedures to enable cross-site comparability
- Encourages use with a publishing mindset to create usable, well-documented datasets
- Recommends data creators/sharers follow standards for accuracy, metadata, and formats; provide guidance and tools; identify data availability and limitations

## Protocol and Data Collection

- Standard Operating Procedures (SOPs) to ensure comparability across ECN sites
- Methodology: standard light trap for Macrolepidoptera; data collection aligned with Rothamsted Insect Survey protocols
- Data cadence: nightly data recording
- Quality information: use accompanying supplementary quality information when using data
- Two key supporting files:
  - ECN_IM2.csv: trap period data (how many days traps were open)
  - ECN_IM_qtext.csv: site manager quality codes and textual notes about data quality

## Data Structure and Download Formats

- Site and location identifiers:
  - SITECODE: unique code per ECN site (e.g., T01, T02, …)
  - LCODE: location code (unique within site)
  - FROMDATE: date traps were set
  - SDATE: sampling date
  - SPERIOD_D: period over which traps were set (days)
- Temporal and measurement fields:
  - YEAR, WEEK
  - FIELDNAME, VALUE: variable being measured and its value
- Comprehensive species coding:
  - FIELDNAME values include quality codes and a large mapping to moth species (e.g., 100 = Alder Kitten; 101 = Puss Moth; 2178 = Plutella xylostella; etc.)
  - Extensive one-to-one mappings between numeric codes and Common Names
- Supporting documentation:
  - ECN_IM2.csv provides trap open periods
  - ECN_IM_qtext.csv provides site-level quality notes and codes

## Metadata, Site Codes, and Variable Mapping

- Explanatory site information:
  - Site codes (T01–T12, etc.) with site names and precise coordinates
  - Examples: T01 Drayton, T02 Glensaugh, T03 Hillsborough, T04 Moor House, T05 North Wyke, T06 Rothamsted, T07 Sourhope, T08 Wytham, T09 Alice Holt, T10 Porton Down, T12 Cairngorms
  - Additional site information available at the ECN site catalogue
- Variable mapping:
  - FIELDNAME entries correspond to quality indicators and species identifications
  - For species lists, codes map to common names (e.g., 100 = Alder Kitten; 101 = Poplar Kitten; 2178 = Diamond-backed Moth; etc.)
  - Note: some codes denote unidentified or macro species and may appear as partial or ambiguous identifications

## Quality Codes and Data Quality

- Quality codes are defined by a standard ECN code set (ECN quality codes)
  - Examples include 100 (No information available), 101 (No sample/reading taken), 102 (Sample lost), 103 (Partial loss), 104 (Sample frozen), etc.
  - Higher-detail entries cover issues such as environmental conditions, sampling disturbances, equipment problems, and data edits
  - A 999 code can indicate an unusual event; accompanying explanations are provided in ECN_IM_qtext.csv
- Quality codes are designed to be associated with specific fields (FIELDNAME) and dates (FROM_DATE, TO_DATE)

## Usage, Acknowledgement, and Data Governance

- Users should acknowledge ECN data use and provide one reprint of any resulting publication
- ECN emphasizes data comparability across sites through standardized protocols and metadata
- Data stewardship requires monitoring for incomplete user needs, timeliness of data delivery, and completeness and interoperability of metadata and quality codes

## Challenges and Considerations for Data Stewards

- Incomplete picture of user needs and priorities across diverse datasets
- Timely acquisition of data from multiple data creators
- Getting data creators to meet metadata and standardization requirements (e.g., site-level quality codes, consistent field naming)
- Interoperability across many different site systems and formats
- Handling large datasets with extensive species mappings and quality codes
- Dealing with outdated or bespoke systems that hinder interoperability

## Special Notes

- Species pair considerations:
  - 3392: Mesapamea secalis/didyma is a species pair; separation requires dissection; females are inseparable in some contexts
  - 3394: Amphipyra berbera berbera can appear as 2507 in data; historically treated as subspecies, now regarded as the same
- See ECN site catalogue for further site information and coordinates

## Contact and Further Information

- ECN Data Centre contact: ecn@ceh.ac.uk
- Data access and site information: https://catalogue.ceh.ac.uk/id/813712d4-d162-4edeaff8-cf1c337bdc27
- Supporting documentation references:
  - ECN_IM2.csv (trap-period data)
  - ECN_IM_qtext.csv (quality text per site/measurement)
  - Standard protocols explained in accompanying documentation (im.pdf)