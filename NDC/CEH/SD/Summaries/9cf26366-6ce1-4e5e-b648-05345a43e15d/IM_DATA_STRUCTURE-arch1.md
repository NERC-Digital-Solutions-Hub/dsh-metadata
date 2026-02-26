# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology.

## Overview
- Source: UK Environmental Change Network (ECN) moth dataset, focusing on Macrolepidoptera collected with standard light-trap protocols.
- Methodology: Nightly observations using Rothamsted Insect Survey protocol; data collected to identify taxa and abundances.
- Purpose: Provide data to understand environmental change impacts on moth populations; support analysis, modeling, and reporting.

## Data structure and content
- Core structure: Each observation includes SITECODE (site), LCODE (location/trap), SDATE (sampling date), FIELDNAME (either quality code or species code), VALUE (count or quality value).
- Single-trap per site in this dataset (LCODE is 1 for all observations).
- Data types:
  - Quality codes: Encoded in FIELDNAME with corresponding quality values (see Table 4 quality codes).
  - Species counts: FIELDNAME indicates a species code; VALUE gives the number of individuals observed.
- Taxonomic coding: Table 3a provides quality codes; Table 3b provides comprehensive species codes with Latin and common names (extensive mapping across many macro-moths).

## Site information
- Drayton (T01): 52°11'37.95"N, -1°45'51.95"W; date range 02-Jan-1993 to 26-Dec-2012
- Glensaugh (T02): 56°54'33.36"N, -2°33'12.14"W; 23-Mar-1994 to 09-Dec-2012
- Hillsborough (T03): 54°27'12.24"N, -6°4'41.26"W; 14-Feb-1993 to 23-Nov-2012
- Moor House - Upper Teesdale (T04): 54°41'42.15"N, -2°23'16.26"W; 01-Jan-1993 to 17-Nov-2012
- North Wyke (T05): 50°46'54.96"N, -3°55'4.10"W; 10-Dec-1992 to 21-Dec-2012
- Rothamsted (T06): 51°48'12.33"N, -0°22'21.66"W; 24-Feb-1992 to 17-Dec-2012
- Sourhope (T07): 55°29'23.47"N, -2°12'43.32"W; 14-Jan-1993 to 19-Dec-2012
- Wytham (T08): 51°46'52.86"N, -1°20'9.81"W; 22-Oct-1992 to 17-Dec-2012
- Alice Holt (T09): 51°9'16.46"N, -0°51'47.58"W; 10-Nov-1992 to 04-Dec-2012
- Porton Down (T10): 51°7'37.83"N, -1°38'23.46"W; 01-Mar-1994 to 24-Oct-2012
- Cairngorms (T12): 57°6'58.84"N, -3°49'46.98"W; 01-Jan-2001 to 31-Dec-2012
- Additional site information available at ECN catalogue link provided in the dataset notes.

## Species and quality codes
- Quality codes (Table 3a): Q1–Q8 (and 999 for unusual events with accompanying quality text).
- Species codes (Table 3b): Extensive mapping of >3000 codes to Latin names and common names (e.g., Alder Kitten, Peppered Moth, Garden Tiger, etc.). Both 3a quality codes and 3b species codes are used to standardize data entries.

## Supplemental quality information
- Supplementary files:
  - ECN_IM2.csv: Information about the period over which moth traps were set (e.g., PERIOD = 1 for daily; other periods documented here).
  - ECN_IM_qtext.csv: Text notes providing additional quality/context for observations (used when standard quality codes are insufficient).

## Usage, attribution, and data provenance
- Acknowledgement: ECN requests acknowledgement of data use in publications; when possible, supply one reprint of publications citing the data.
- Data provenance: ECN dataset maintained by ECN Data Centre; dataset owners include a consortium of UK government departments and agencies (e.g., Defra, Natural England, Scottish Environment Protection Agency, etc.).
- Discoverability and metadata: Datasets are described with site metadata, sampling periods, and quality codes; datasets and related quality information are intended to be discoverable via data portals and metadata records.

## Particular challenges and considerations for analysts
- Data at the local scale: Potential lack of data at fine spatial resolution or at local levels for certain questions.
- Accessibility and fragmentation: Data may be stored in journals, reports, or local authority records, complicating retrieval; expect some barriers to dataset discovery.
- Standardization and integration: Unifying data across multiple sites and formats requires careful handling of varying scales and measurement details; extensive use of standardized codes (species and quality codes) aids consistency but requires robust reference tables.
- Data quality and interpretation: Site managers assign quality codes; unusual events require consulting accompanying quality text (3xx-999); occasional non-standard sampling dates or periods may require special handling.
- IT and workflow demands: Large, multi-site datasets can involve heavy computational needs; ensure appropriate software versions and data processing pipelines are in place.
- Data protection and timely access: Public health and related analyses may face stricter data protection considerations; ensure compliant handling when combining datasets with other sources.
- Reporting and impact: For academics and practitioners, translating coded data (species and quality codes) into actionable insights requires clear mapping to searchable taxonomic names and transparent quality flags.

## How to approach analysis with this dataset
- Leverage the nightly Macrolepidoptera observations across multiple ECN sites to investigate temporal trends, correlations with environmental variables, and potential predictors of moth abundance.
- Use the provided site metadata, trapping periods, and quality codes to clean and quality-check datasets before modelling.
- Cross-reference Table 3b species codes with Latin/Common names to interpret abundances; pay attention to quality codes for data reliability.
- Consult supplemental quality information files for context on sampling periods and any unusual events affecting observations.