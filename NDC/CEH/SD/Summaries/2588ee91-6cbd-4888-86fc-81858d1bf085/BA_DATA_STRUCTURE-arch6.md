# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

- The ECN bat transect dataset provides bat detection data collected along transects across multiple ECN sites, with accompanying habitat and site metadata, and quality information.
- Data are managed by the ECN Data Centre, with data usage expected to be acknowledged and a reprint of any citing publication sent to ECN.

## Overview and Purpose
- ECN environmental change dataset focused on bat presence/absence and activity along transects.
- Uses standardized protocols to ensure comparability across sites and over time.
- Supports data reuse by linking bat results to habitat context and site metadata; intended for researchers and policymakers studying environmental change impacts on bat populations.

## Dataset Ownership and Funding
- ECN programme sponsored by a consortium of UK government departments and agencies (funding site monitoring or network coordination).
- Participating organizations include: AFBI, BBSRC, CCW, DSTL, DEFRA, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, SEPA, Scottish Government, and others.
- Users should acknowledge the data use and send one reprint of any publication citing ECN data.

## Protocol and Data Quality
- Standard operating procedures ensure data comparability across sites.
- A quality information file accompanies the dataset to document data quality and any issues.
- Limitations exist in deriving precise relationships between bat populations and environmental change; linking ECN data with broader monitoring helps mitigate these limits.
- Users should consult accompanying quality information when using the data.

## Data Download Structure and Core Fields
- Core dataset fields:
  - SITECODE: Unique code for each ECN Site
  - SDATE: Sampling date
  - TRANSECT: Transect identifier
  - BATLOC_ID: Location where a bat was seen or heard (unique per survey date)
  - FIELDNAME: Variable measured (species codes below)
  - VALUE: Value of the measured variable
  - ACTS: Activity code – bat seen
  - ACTH: Activity code – bat heard
  - ACTF: Activity code – bat feeding buzz heard

- Supporting Documentation – ECN_BA2.csv (survey methodology details):
  - BATDETECTORTYPE: Bat detector used
  - KEPTPROTOCOLFREQUENCY: Was detector frequency kept at 45 Hz? (Y/N)
  - ADJUSTFREQUENCY: Was frequency adjusted to aid identification? (Y/N)
  - USEREFERENCECD: Was detector output recorded and compared with a CD of heterodyne calls? (Y/N)
  - USESONOGRAMANALYSIS: Was sonogram analysis used? (Y/N)

- Supporting Documentation – ECN_BA3.csv (habitat information observed on transect):
  - SITECODE, SDATE, TRANSECT, BATLOC_ID: As above
  - FIELDNAME: Variable measured (habitat code)
  - VALUE: Code for habitat type

- Supporting Documentation – ECN_BA_qtext.csv (quality notes from site managers):
  - SITECODE, FIELDNAME
  - FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION

## Explanatory Reference Data

- Site Codes
  - T01 Drayton
  - T02 Glensaugh
  - T03 Hillsborough
  - T04 Moor House - Upper Teesdale
  - T05 North Wyke
  - T07 Sourhope
  - T08 Wytham
  - T09 Alice Holt
  - T10 Porton Down
  - T11 Y Wyddfa - Snowdon
  - Each includes geographic coordinates and site-specific context

- Species Codes
  - Codes map to Latin and common names (e.g., Bb = Barbastella barbastellus; Pp = Pipistrellus; Ppl = Pipistrellus pipistrellus; Nl = Nyctalus leisleri; Nn = Nyctalus noctula; Rh = Rhinolophus hipposideros; Rf = Rhinolophus ferrumequinum; XX = No bats found; UU = Unidentified bat; etc.)
  - Enables standardized reporting of bat detections and identifications

- Habitat Codes and Habitat Types
  - HAB1, HAB2, HAB3: First, second, and third habitat types recorded near sighting (qualitative)
  - Habitat Types 1–43: Descriptions cover vegetation, land cover, and landscape features (e.g., hedgerows, treelines, woodlands, grasslands, arable, built land, water features, etc.)
  - Detailed descriptions provide the context needed to analyze bat-habitat associations

## Usage Notes and Considerations
- Bat detections are recorded on transects with four surveys per year across specific date windows.
- Survey windows: mid-June to early September, across four 3-week periods; surveys are skipped in heavy rain or strong winds.
- Methodology aligns with established bat survey practices (e.g., Bats and Habitats survey for JNCC).
- Limitations exist for deriving precise population-environment relationships; integrating ECN data with broader monitoring helps address these gaps.
- Ensure use of accompanying quality information to assess data reliability and site-specific caveats.

## Access and Acknowledgement
- Users should acknowledge the ECN data and share one reprint of any publication citing the data.
- For questions or more information about data usage, contact ecn@ceh.ac.uk.