# Common Frog Spawn Phenology Dataset - ECN

## Overview
- Phenology-based dataset of Common Frog spawning health indicators, collected from selected pools and ditches.
- Includes accompanying laboratory water analyses and quality metadata to support data quality assessment.
- Managed by the UK Environmental Change Network (ECN) with a focus on environmental change research.

## Provenance and Stewardship
- Dataset Originator: ECN Data Centre, Centre for Ecology and Hydrology (CEH) - contact: ecn@ceh.ac.uk; http://data.ecn.ac.uk
- Dataset Owners/Sponsors: UK government departments/agencies (e.g., DEFRA, Natural England, Environment Agency, Forestry Commission, devolved administrations, and science councils) contributing funding and governance.
- Usage terms: Acknowledge use of ECN datasets in publications and send one reprint to ECN upon citation.
- Data comparability: ECN operates standard operating procedures (BF.pdf) to ensure cross-site data comparability.

## Data structure and access
- Data download schema: SITECODE (site code), LCODE (location code within site), FROMDATE (from date of last recording), SDATE (sampling date), FIELDNAME (variable measured), VALUE (measured value).
- Supporting documentation: ECN_BF_qtext.csv provides quality text for site-reported factors affecting data quality; quality codes from a standard list are included with the data; 999 in data indicates an unusual event described in the quality text.
- Quality information: Users should consult accompanying quality information when using the data.

## Documentation and quality metadata
- Quality codes: Extensive list (e.g., 100, 101, 102, ..., 513) describing issues affecting data quality (sample loss, contamination, equipment problems, field conditions, etc.), plus 999 for unusual events with narrative in quality text.
- Field-level quality reporting: Quality codes are applied to measurements and are included in the data download for traceability.

## Site codes and coordinates
- T01 Drayton: 52°11'37.95"N, 1°45'51.95"W
- T02 Glensaugh: 56°54'33.36"N, 2°33'12.14"W
- T03 Hillsborough: 54°27'12.24"N, 6°04'41.26"W
- T04 Moor House - Upper Teesdale: 54°41'42.15"N, 2°23'16.26"W
- T05 North Wyke: 50°46'54.96"N, 3°55'4.10"W
- T06 Rothamsted: 51°48'12.33"N, 0°22'21.66"W
- T08 Wytham: 51°46'52.86"N, 1°20'9.81"W
- T09 Alice Holt: 51°9'16.46"N, 0°51'47.58"W
- T10 Porton Down: 51°7'37.83"N, 1°38'23.46"W
- T11 Y Wyddfa (Snowdon): 53°4'28.38"N, 4°2'0.64"W

## Variables and units (FIELDNAME)
- Alkalinity (ALKY) – mg/L
- Aluminium (ALUMINIUM) – mg/L
- Calcium (CALCIUM) – mg/L
- Chloride (CHLORIDE) – mg/L
- Conductivity (CONDY) – µS/cm
- Colour (COLOUR) – nM (absorbance at 436 nm)
- CongenDate (CONGDATE) – date of first frog congregation
- Depth (DEPTH) – cm
- Dissolved Organic Carbon (DOC) – mg/L
- HatchDate (HATCHDATE) – date of first hatching
- Iron (IRON) – mg/L
- LeaveDate (LEAVEDATE) – date frogs first leaving
- Magnesium (MAGNESIUM) – mg/L
- MaxTemp (MAXTMP) – °C
- MinTemp (MINTMP) – °C
- NEWMASS – count of new spawn masses
- NH4N – mg/L
- NO3N – mg/L
- PERCDEAD – percentage dead/diseased eggs
- pH (PH) – pH units
- Daily pH readings: PH1, PH2, PH3 – pH units
- Aquacheck pH: PHAQCS (stirred), PHAQCU (unstirred)
- Phosphate Phosphorus (PO4P) – mg/L
- Potassium (POTASSIUM) – mg/L
- Quality codes Q1–Q8 – integer quality indicators
- Sulphate (SO4S) – mg/L
- Sodium (SODIUM) – mg/L
- SpawnDate (SPAWNDATE) – date of first spawning
- Surface area (SURFAREA) – m²
- Stage (STAGE) – measured stage of water level
- Total Nitrogen (TOTALN) – mg/L
- Total Phosphorus (TOTALP) – mg/L
- Vacuum (VACUUM) – bar
- Volume (VOLUME) – mL
- Other field names may be present as part of site-specific observations

## Usage guidance for Data Leaders
- Holistic view: The dataset combines ecological phenology with water chemistry, enabling integrated data products about frog spawning health and habitat conditions.
- Data quality emphasis: Always leverage the embedded quality codes and the supplementary ECN_BF_qtext.csv to assess data reliability and context for unusual events.
- Metadata and standards: The dataset uses standardized site codes, field names, and unit conventions, with documented site coordinates to support interoperability and discoverability.
- Governance practices: Follow ECN requirements to acknowledge data use and share reprints; rely on ECN SOPs to maintain cross-site comparability.
- Discovery and collaboration: The dataset structure (site codes, field names, and quality metadata) supports data discovery across ECN sites and collaboration with the wider data community, addressing common data-leader challenges around data availability, standardization, and metadata clarity.