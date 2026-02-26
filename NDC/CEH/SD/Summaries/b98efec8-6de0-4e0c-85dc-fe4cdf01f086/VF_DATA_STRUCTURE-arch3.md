# ECN Data Centre Dataset Documentation

- Describes the ECN Vegetation Field Data (VF) datasets, including data origin, ownership, protocols, data structure, supporting metadata, and data governance.

## Dataset origin, ownership and acknowledgement

- Originator: ECN Data Centre (Centre for Ecology and Hydrology) - http://data.ecn.ac.uk
- Owners: UK Environmental Change Network (ECN) programme funded by a consortium of government departments/agencies (e.g., DEFRA, Natural England, Environment Agency, SEPA, etc.)
- Acknowledgement: Users should acknowledge ECN data use and send one reprint of any publication citing the data.

## Protocols and data quality

- Standard operating procedures to ensure data comparability across sites; refer to accompanying documentation for collection explanations.
- Data collection framework:
  - At least two 10 m x 10 m plots per site within each NVC type; species presence recorded in 40 cm x 40 cm cells.
  - Primary survey every three years; some sites conduct annual surveys for higher temporal resolution (fewer plots).
- Emphasis on data quality assurance, cleansing, transformation, analysis, and clear presentation (reports, charts, dashboards).

## Data structure and downloads

- Main data download fields:
  - SITECODE, SYEAR, PLOTPID, CELLID, FIELDNAME (VEG_SPEC for species code; Q1/Q2/Q3 for quality codes), VALUE
- Supporting documentation files:
  - ECN_VF2.csv: Plot-level information (SITECODE, SYEAR, PLOTPID, SDATE, PEDATE, LANDUSE, SLOPE, SLOPEFORM, NVCCLASS)
  - ECN_VF3.csv: Cell-level information (SITECODE, SYEAR, PLOTPID, CELLID, FEATURE)
  - ECN_VF_qtext.csv: Qualitative text for data quality issues (site managers select standard quality codes; text attached for code 999)
- Site codes (examples): T01 Drayton, T02 Glensaugh, T03 Hillsborough, T04 Moor House - Upper Teesdale, T05 North Wyke, T06 Rothamsted, T07 Sourhope, T08 Wytham, T09 Alice Holt, T10 Porton Down, T11 Snowdon, T12 Cairngorms
- Explanatory mappings include:
  - Land Use (Hodgson codes)
  - Slope Form (Convex, Straight, Concave)
  - Features (Path, Wall, Stream, Hedge, etc.)
- Species codes:
  - ECN uses the VESPAN coding list with cross-references to the Biological Records Centre (BRC) list
  - Extensive crosswalks for Latin names, BRC concepts, synonyms, subspecies; includes plants, bryophytes, lichens, and other taxa

## Metadata and data availability

- Site managers attach quality codes to indicate data quality factors; quality text available in ECN_VF_qtext.csv.
- Data provenance, site-level and plot-level metadata, and transparent data sharing are emphasized for reuse and verification.

## Data governance, sharing, and reuse

- Clear data provenance and metadata; sharing underlying data publicly where appropriate; enabling reuse and verification.
- Establishing data quality assurance, cleaning, transformation, and transparent reporting.
- Implementing data governance processes to ensure datasets meet standards and remain up to date.

## Explanatory information: Species codes

- Provides extensive mappings between ECN species codes and alternate references, including multiple synonyms and cross-references (e.g., Rumex obtusifolius mappings to various species concepts; highlights the complexity and breadth of taxa coverage).

## Explanatory information: Quality codes

- Quality codes with descriptions (e.g., 100 = No information available; 101 = No sample/reading taken; 999 = Unusual event).
- Covers a wide range of data collection and processing conditions, including field/instrument issues, environmental factors, sampling disturbances, laboratory issues, and data integrity notes.

## Particular challenges for Authors of Monitoring Frameworks

- Common barriers include:
  - Lack of data or data meeting quality standards
  - Limited access to data or delays in access
  - Organisational silos hindering sharing and integration
  - Requirements to publicly share data deterring use of datasets
  - Keeping data up to date as a barrier to sharing
  - Inadequate metadata hindering quick verification
  - Data formats requiring transformation to be usable
  - Communicating complex findings clearly to policymakers
  - Implementing robust data governance to maintain standards and up-to-date datasets

## Implications for policy and monitoring

- Demonstrates rigorous metadata, provenance, and governance practices that support transparency, reuse, and informed decision-making in environmental monitoring frameworks.