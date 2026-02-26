# Common Frog Spawning Phenology Data (ECN)

## Overview
- ECN Data Centre is the dataset originator and host, with the UK Environmental Change Network (ECN) programme as the dataset owner and sponsor.
- The ECN program involves multiple UK government departments and agencies funding site monitoring or network co-ordination.
- Users are asked to acknowledge data use and to send one reprint of any publication that cites ECN data.

## Governance, provenance, and standards
- ECN has standard operating procedures (protocols) to ensure comparability of data across sites (referenced by BF.pdf for data collection explanations).
- Data sharing follows a publishing-minded approach to make datasets usable for others, with guidance and tools provided to data creators/sharers to meet standards (accuracy, metadata, format).
- Clear expectations for updates and data availability; site managers may annotate data quality using standardized quality codes, with a mechanism to add free-text explanations for unusual events (quality code 999).

## Data structure and metadata
- Data download schema includes:
  - SITECODE: Unique ECN Site code (e.g., T01–T11)
  - LCODE: Location code (unique within site)
  - FROMDATE: From date (last recorded)
  - SDATE: Sampling date
  - FIELDNAME: Variable measured
  - VALUE: Measured value
- Supporting documentation: ECN_BF_qtext.csv provides quality-text mappings for quality codes when needed.
- Explanatory information includes:
  - Site Codes and corresponding site names with precise coordinates (e.g., T01 Drayton; T11 Snowdon)
  - Variables measured (FIELDNAME) with detailed descriptions and units (e.g., ALKY = Alkalinity, mg/L; CONDY = Conductivity, µS/cm; pH values; various nutrients and biochemicals)
  - Example and umbrella categories for measurement (e.g., water chemistry parameters, spawn-related dates, counts)
- Variables cover both frog-spawn related metrics (e.g., CONGDATE, HATCHDATE, SPAWNDATE, NEWMASS, PERCDEAD, SPAWNAREA) and a broad suite of water quality indicators (alkalinity, chlorine, conductivity, color, dissolved organic carbon, metals, major ions, nutrients, pH, temperature, etc.), including multiple fields for quality controls (Q1–Q8).

## Quality assurance and quality codes
- Site managers assign standardized quality codes indicating data quality issues or contextual factors affecting measurements (e.g., 100 No information available; 101 No sample/readings; 102 Sample lost; 200–239 range for observational and environmental conditions; 501–513 for laboratory-related issues).
- A dedicated code 999 indicates an unusual event; accompanying narrative text for such events is stored in ECN_BF_qtext.csv.
- The quality codes cover a broad spectrum of potential data quality impacts, including sample contamination, equipment issues, environmental disturbances, and laboratory processing problems.

## Usage, attribution, and data sharing constraints
- Usage notes emphasize phenology-based methodology: recording spawning of the Common Frog in selected pools/ditches by counting egg masses; parallel laboratory analyses of water samples.
- Users should consult the accompanying quality information (ECN_BF_qtext.csv) for context on data quality.
- Acknowledgement and reprint submission: users should acknowledge ECN data in publications and provide at least one reprint of any publication citing ECN data.

## Site and variable details relevant to data stewardship
- Site mapping: 11 listed sites (T01 Drayton, T02 Glensaugh, T03 Hillsborough, T04 Moor House - Upper Teesdale, T05 North Wyke, T06 Rothamsted, T08 Wytham, T09 Alice Holt, T10 Porton Down, T11 Snowdon) with precise latitude/longitude coordinates.
- Variables (FIELDNAME) include a comprehensive set of environmental and chemical measurements (e.g., ALKY, ALUMINIUM, CALCIUM, CHLORIDE, CONDY, COLOUR, DOC, IRON, MAGNESIUM, MAXTMP, MINTMP, NH4N, NO3N, PERCDEAD, PH, SPAWNDATE, SURFAREA, TOTALN, TOTALP, SODIUM, etc.) with corresponding units.
- Several fields capture timing and biological observations related to frog spawning (CONGDATE, HATCHDATE, SPAWNDATE, NEWMASS, SPAWNAREA, DELAYED or CONTINUING quality contexts).

## Practical considerations for Data Stewards
- Ensure ongoing adherence to ECN SOPs to maintain cross-site data comparability.
- Maintain and update the SITE CODE mapping and coordinates to support accurate site discovery and data provenance.
- Manage and communicate data quality issues through the quality code system, including supplying text descriptions for 999 events.
- Facilitate data sharing while preserving embargoes or proprietary considerations and ensuring that updates are reflected in downstream portals and catalogs.
- Track and request proper acknowledgment and dissemination of reprints to demonstrate data impact and value.