# Dataset Originator

- ECN Data Centre (http://data.ecn.ac.uk), Centre for Ecology and Hydrology
- Dataset Owners: UK Environmental Change Network (ECN) programme funded by a consortium of UK government departments and agencies
- Acknowledgement: ECN requests acknowledgement of data use and one reprint of any publication citing ECN data

## Purpose and scope

- Provides standardized moth trap (Macrolepidoptera) data from ECN sites to understand environmental change and insect biodiversity
- Used to support ecological research and data products for wider data use

## Protocol and data collection

- Standard operating procedures to ensure comparability across sites
- Methodology aligned with Rothamsted Insect Survey
- Data collected nightly using a standard light trap
- accompanying quality information should be used when analyzing data

## Data download format and structure

- Site code (SITECODE): unique code for each ECN site
- Location code (LCODE): location ID within site
- Sampling date (SDATE): date of sampling
- Field name (FIELDNAME): variable being measured
- Value (VALUE): measured value
- Additional files:
  - ECN_IM2.csv: period over which moth traps were set (days), with daily trap emptying in most cases
  - ECN_IM_qtext.csv: quality text entries explaining data quality events; a quality code 999 indicates unusual events
- Data can include both species-level codes and quality indicators; “XX” denotes no moths present in some records

## Supporting documentation and site metadata

- ECN_IM2.csv: trap period data (e.g., PERIOD_D)
- ECN_IM_qtext.csv: quality text and associated dates, with codes
- Site codes: T01–T12 with site names and precise coordinates (e.g., T01 Drayton; T12 Cairngorms)
- Additional site information available at ECN catalogue

## Site codes and locations (exemplars)

- T01 Drayton: 52°11'37.95"N, 1°45'51.95"W
- T02 Glensaugh: 56°54'33.36"N, 2°33'12.14"W
- T03 Hillsborough: 54°27'12.24"N, 6°4'41.26"W
- T04 Moor House - Upper Teesdale: 54°41'42.15"N, 2°23'16.26"W
- T05 North Wyke: 50°46'54.96"N, 3°55'4.10"W
- T06 Rothamsted: 51°48'12.33"N, 0°22'21.66"W
- T07 Sourhope: 55°29'23.47"N, 2°12'43.32"W
- T08 Wytham: 51°46'52.86"N, 1°20'9.81"W
- T09 Alice Holt: 51°9'16.46"N, 0°51'47.58"W
- T10 Porton Down: 51°7'37.83"N, 1°38'23.46"W
- T12 Cairngorms: 57°6'58.84"N, 3°49'46.98"W

## Variables and coding

- FIELDNAME values map to:
  - Quality codes (Q1–Q8): indicate data quality factors
  - Species and common names: extensive mapping of numeric codes to moth species (e.g., 100 Alder Kitten, 1001 Rush Veneer, etc.)
  - XX and other codes used to denote unidentifiable or non-moth entries in some records
- Comprehensive, but large, species code table included in the dataset documentation

## Quality codes

- Codes describe data quality issues or contextual factors (e.g., 100 No information available; 101 No sample/reading; 102 Sample lost; 103 Partial loss; 104 Sample frozen)
- Additional quality context codes (e.g., 105 Snow in funnel; 106 Snow during sampling period; 200 Adverse weather; 201 Biting insects; 202 Failing light; 999 Unusual event)
- Quality text (ECN_IM_qtext.csv) provides human-readable explanations for codes like 999

## Special notes and caveats

- Some species codes are paired (e.g., 3392 Mesapamea secalis/didyma) and cannot be separated without dissection
- Some codes (e.g., 3394 Amphipyra berbera berbera) may appear under alternative identifiers (e.g., 2507) as taxonomic treatment evolves
- Data may include periods with no moths detected (XX) or incomplete records requiring interpretation with caution

## How this supports Data Support archetype work

- Provides a robust, standardized data source for cross-site insect monitoring and environmental change analysis
- Facilitates building self-serve dashboards or reports by offering a clear data structure (SITECODE, LCODE, SDATE, FIELDNAME, VALUE) and accompanying quality information
- Requires data cleaning and quality assurance steps (as per Protocol and ECN_qtext) to ensure reliable insights
- Offers rich metadata (site coordinates, trap protocols, quality codes) to contextualize analyses and promote data reuse across topics and organisations such as local councils or private enterprises