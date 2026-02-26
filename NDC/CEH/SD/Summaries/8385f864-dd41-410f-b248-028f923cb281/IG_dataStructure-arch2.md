# Dataset Originator

- The ECN Data Centre (Centre for Ecology and Hydrology) is the dataset originator for ECN ground beetle data.
- Dataset Owners: UK Environmental Change Network (ECN) programme, funded by a consortium of UK government departments and agencies.
- Acknowledgement and citation: Users should acknowledge ECN data usage and send one reprint of any publication citing the data.

## Purpose and Aims

- Monitor environmental change by providing standardized, comparable data across ECN sites.
- Produce outputs such as categorizing environmental health against standards, enabling assessment of environmental policy performance over time.
- Deliver data outputs in clear formats (reports, maps, charts) and maintain datasets in appropriate data portals.

## Protocols and Data Quality

- ECN uses standard operating procedures to ensure comparability across sites (see accompanying ig.pdf for data collection methods).
- Primary monitoring focus in this dataset: abundance of ground beetles (Carabidae) using pitfall traps.
- Sampling cadence: fortnightly recordings from May to October.
- Quality information must be used in conjunction with the data.

## Data Download Structure

- Key fields:
  - SITECODE: Unique code for each ECN site.
  - LCODE: Location ID (unique within site).
  - SDATE: Sampling date.
  - TRAP: Trap number.
  - FIELDNAME: Variable measured (e.g., quality codes, species data).
  - VALUE: Measured value.
  - TYPE: In the Pterostichus madidus (6453 2714) dataset, includes gender (M/F) and leg colour morphs (R, B).
- Special notes: The TYPE field applies specifically to the Pterostichus madidus data; other records use standard fields.

## Supporting Documentation

- ECN_IG2.csv: Trap-set information (FROMDATE, SDATE and trap deployment details).
- ECN_IG3.csv: Habitat information (HABDESC).
- ECN_IG_qtext.csv: Quality text descriptions for untranslated or non-coded quality events; linked via quality codes (see ECN_IG_qtext.csv for details).

## Explanatory Information: Site Codes

- T01 to T12 with site names and precise coordinates:
  - T01 Drayton
  - T02 Glensaugh
  - T03 Hillsborough
  - T04 Moor House - Upper Teesdale
  - T05 North Wyke
  - T06 Rothamsted
  - T07 Sourhope
  - T08 Wytham
  - T09 Alice Holt
  - T10 Porton Down
  - T11 Snowdon (Y Wyddfa)
  - T12 Cairngorms
- Additional site information available at CEH catalogue (link provided in the dataset).

## Explanatory Information: Variables and Taxa

- FIELDNAME mappings include:
  - Q1–Q8: Quality codes (descriptions provided in the Quality Codes section).
  - 6453 2714 etc.: Taxonomic groupings for ground beetles (e.g., Cicindela, Pterostichus madidus, and numerous genera/species with GENUS or SPECIES descriptions and ranks).
- Taxa are organized by genus and species across a comprehensive Cerambycid-like beetle classification, with explicit entries for each taxon and rank (GENUS/SPECIES).

## Explanatory Information: Quality Codes

- Quality Codes (examples and descriptions):
  - 100: No information available - data lost
  - 101–135, 136–190, 200–239, 240–299, 501–507, 999: various data acquisition, processing, and laboratory-related statuses and issues
  - 999: Unusual event (see associated quality text)
  -  XX: No ground beetles present
- Site managers assign multiple quality codes as applicable; unusual events are described in quality text (ECN_IG_qtext.csv).

## Usage Considerations for Analysts

- Data are designed for cross-site comparability; standardization is essential for time-series analyses of environmental health indicators.
- Use ECN_IG2/ECN_IG3/ECN_qtext documentation to interpret dataset qualifiers and habitat context.
- When reusing data, acknowledge ECN and consult the accompanying quality information to assess data reliability and any data losses or anomalies.
- Potential data value enhancement by combining ECN dataset with other environmental data sources and ensuring access to underlying data via portals.

## Access and Further Information

- Site-level details and broader ECN context available through the ECN data portal and CEH catalogue link provided in the dataset.
- For data usage, follow ECN’s guidance on quality codes and supporting documentation to ensure correct interpretation and replication of analyses.