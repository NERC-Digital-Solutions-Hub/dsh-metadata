# UK Environmental Change Network (http://www.ecn.ac.uk) Frogs (BF)

## Overview
- Phenology-based frog dataset focusing on the spawning activity of the Common Frog, using egg masses as an indicator of population health.
- Complemented by laboratory analyses of water from observed pools and ditches.
- Data are produced and managed by the ECN Data Centre at the Centre for Ecology and Hydrology; dataset ownership lies with the UK Environmental Change Network programme, sponsored by a consortium of UK government departments and agencies.

## Dataset Origin, Ownership and Sponsorship
- Dataset Originator: ECN Data Centre, Centre for Ecology and Hydrology (data.ecn.ac.uk; ecn@ceh.ac.uk).
- Dataset Owners: UK Environmental Change Network programme.
- Sponsoring organisations (contributors to site monitoring or network coordination): Agri-Food and Biosciences Institute; Biotechnology and Biological Sciences Research Council; Cyfoeth Naturiol Cymru – Natural Resources Wales; Defence Science and Technology Laboratory; Department for Environment, Food and Rural Affairs; Environment Agency; Forestry Commission; Llywodraeth Cymru – Welsh Government; Natural England; Natural Environment Research Council; Northern Ireland Environment Agency; Scottish Environment Protection Agency; Scottish Government; Scottish Natural Heritage.
- Acknowledgement and publication: Users are requested to acknowledge the data usage and to send one reprint of any publication that cites the dataset.

## Protocol and Content
- Methodology: Phenology-based observation of frog spawning, recording the number of egg masses as an indicator of population health.
- Laboratory analyses: Water chemistry analyses accompany field observations.
- Use and interpretation: Users should apply the accompanying quality information when using the data.

## Data Structure and Storage
- Storage: Data are held in Oracle databases, with separate tables for field observations (D1BF_xxx) and laboratory analyses (D2BF_xxx) for each site code (xxx).
- Site codes and metadata:
  - T01 Drayton (52°11'37.95"N 1°45'51.95"W): Date range in dataset 01-JAN-1994 to 22-FEB-2012.
  - T02 Glensaugh (56°54'33.36"N 2°33'12.14"W): 01-JAN-1994 to 19-JUN-2012.
  - T03 Hillsborough (54°27'12.24"N 6°4'41.26"W): 01-JAN-1994 to 25-FEB-2011.
  - T04 Moor House - Upper Teesdale (54°41'42.15"N 2°23'16.26"W): 01-JAN-1994 to 10-OCT-2012.
  - T05 North Wyke (50°46'54.96"N 3°55'4.10"W): 05-JAN-1994 to 28-MAR-2012.
  - T06 Rothamsted (51°48'12.33"N 0°22'21.66"W): 17-FEB-1994 to 14-JUL-2010.
  - T08 Wytham (51°46'52.86"N 1°20'9.81"W): 01-JAN-1994 to 17-JUN-1994.
  - T09 Alice Holt (51°9'16.46"N 0°51'47.58"W): 28-FEB-1995 to 14-MAR-2001.
  - T10 Porton Down (51°7'37.83"N 1°38'23.46"W): 14-FEB-2001 to 07-APR-2010.
  - T11 Y Wyddfa – Snowdon (53°4'28.38"N 4°2'0.64"W): 31-DEC-1995 to 30-MAY-2012.
  - Note: The dataset descriptions include site names, coordinates, and date ranges in the dataset; some sites have shorter date spans than others.
- Data tables:
  - D1BF_xxx: Field observation data for each site (phenology-based measures such as egg masses, spawning indicators) stored per site.
  - D2BF_xxx: Lab analysis data for each site (water chemistry and related measurements) stored per site.
  - Core metadata tables are referenced for structure and relationships (metadata documentation noted).

## Data Fields and Metadata
- Core structure components (per site):
  - SITECODE: Site code.
  - LCODE: Location code.
  - SDATE: Sampling date (dd-mmm-yyyy).
  - FROMDATE, etc.: Additional date fields for data history.
  - FIELDNAME: Name of the measured field (e.g., spawn-related metrics, water quality parameters).
  - VALUE: Measured value.
  - Quality-related fields and codes accompany measurements to indicate data quality and potential issues.
- Field names cover a broad range of variables including:
  - Alkalinity, various metal concentrations, conductivity, pH-related measurements, dissolved organic carbon, nutrient species (ammonium, nitrate, phosphate), major ions, and several frog-spawning- and habitat-related parameters (e.g., spawn counts, spawn date, spawn area, various temperature measures, etc.).
  - Quality codes (Q1–Q8, etc.) provide per-measurement quality flags.
- Quality codes:
  - ECN standard quality codes indicate issues affecting data quality (e.g., missing samples, contaminated samples, equipment or sampling issues, weather effects, etc.).
  - Codes range broadly (e.g., 100–199 for sample/reading issues, 501–513 for laboratory-related issues) plus many specific condition codes.
  - 999 is used for an unusual event not covered by standard codes, with accompanying text explaining the circumstances.
- Quality information is integral to data usage; users are advised to consult accompanying quality metadata before analysis.

## Usage, Acknowledgement, and Deliverables
- Acknowledgement: Please acknowledge ECN data use in publications.
- Publication request: Send one reprint of any publication citing ECN data.
- Data provenance and protocol reference: Protocols and measurement procedures are documented (e.g., Terrestrial measurements for BF project). Access to the protocol reference and accompanying metadata/quality documentation is recommended for proper usage.

## Governance, Access, and Challenges
- Data governance: Managed by ECN Data Centre with defined site ownership and sponsorship; data are intended to be discoverable and usable across the network.
- Access considerations: Data quality is supported by detailed quality codes and accompanying metadata; users should apply the quality information when using data.
- Particular challenges faced by data stewards (as relevant to this dataset):
  - Incomplete picture of user needs and priorities.
  - Timely delivery of data from diverse site coordinators.
  - Ensuring data creators meet standards (particularly metadata completeness).
  - Interoperability across many systems and formats.
  - Handling large datasets and bespoke solutions for older or outdated databases.
- Data stewardship implications:
  - Maintain robust metadata documenting data origin, site details, sampling protocols, and quality codes.
  - Facilitate discovery and reuse by providing clear data structures, site summaries, and guidance on quality interpretation.
  - Ensure proper acknowledgement workflows and capture of data usage metrics.