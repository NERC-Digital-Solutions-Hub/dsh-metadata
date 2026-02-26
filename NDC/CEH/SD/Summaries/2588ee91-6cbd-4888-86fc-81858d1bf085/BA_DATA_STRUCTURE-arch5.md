# ECN Bat Activity Data

## Overview
- Dataset Originator: ECN Data Centre (http://data.ecn.ac.uk), Centre for Ecology and Hydrology
- Dataset Owners: UK Environmental Change Network (ECN) programme; funded by a consortium of UK government departments and agencies (e.g., DEFRA, Natural England, NERC, Environment Agency, etc.)
- Purpose and scope: Provide bat activity data collected across ECN sites with standard procedures to ensure cross-site comparability; enable data sharing and reuse for environmental change research; acknowledge data use and share one reprint of publications citing the data
- Publication and reuse expectations: Acknowledge ECN data usage; send one reprint of any publication citing the data

## Protocols and Standards
- Standard Operating Procedures: ECN maintains protocols to ensure data comparability across sites; a accompanying protocol (PDF) explains data collection methods
- Publishing approach: Data are uploaded to relevant portals and catalogued; data may be updated over time with governance around updates

## Data Content and Structure
- Primary data fields (ECN_BA dataset):
  - SITECODE: Unique code for each ECN Site
  - SDATE: Sampling date
  - TRANSECT: Transect identifier
  - BATLOC_ID: Location within the site where a bat was seen or heard (unique per survey date; mapped on a paper map)
  - FIELDNAME: Variable measured (bat-related)
  - VALUE: Value of the measured variable
  - ACTS: Activity code - bat seen
  - ACTH: Activity code - bat heard
  - ACTF: Activity code - bat feeding buzz heard
- Supporting documentation (ECN_BA2.csv):
  - BATDETECTORTYPE: Bat detector used
  - KEPTPROTOCOLFREQUENCY: Detector kept at 45Hz?
  - ADJUSTFREQUENCY: Frequency adjustment for identification
  - USEREFERENCECD: Detector output compared with heterodyne calls
  - USESONOGRAMANALYSIS: Detector output recorded and sonogram analysis used
- Supporting documentation (ECN_BA3.csv):
  - HABITAT- related fields: SITECODE, SDATE, TRANSECT, BATLOC_ID, FIELDNAME (habitat variable), VALUE (habitat code)
- Quality and context (ECN_BA_qtext.csv):
  - Site-specific qualitative notes on data quality and circumstances affecting data
  - Fields include SITECODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION
- Explanatory reference data:
  - Explanatory Information - Site Codes: mapping of site codes (e.g., T01–T11) to site names and geographic coordinates
  - Explanatory Information - Species Codes: mapping of abbreviations to Latin and common bat names (e.g., Pp = Pipistrellus, Nf = No bats found, etc.)
  - Explanatory Information - Habitat Codes and Habitat Types: structured list from HAB1 to HAB27 (and beyond) describing habitat types (e.g., hedgerows, treelines, woodlands, grasslands, water bodies, urban areas, etc.)
- Access and reference:
  - Further ECN site information available at the CEH catalogue link
  - Data can be downloaded with the defined field structure; instructions and field names (e.g., species codes, habitat types) provided in accompanying documentation

## Data Quality, Usage, and Limitations
- Use of quality information: Always consult accompanying ECN_BA_qtext.csv for site-specific quality notes when analyzing data
- Methodological notes:
  - Bat detection via transect-based surveys and bat detectors
  - Surveys conducted four times per year during defined date windows; surveys not conducted in heavy rain or strong winds
  - Linking results to environmental change has limitations; cross-referencing with other monitoring programmes can mitigate these limitations
- Limitations for governance:
  - Data owners may require acknowledgement and citation; potential embargoes or updates governed by ECN protocols
  - Data from multiple systems and formats necessitates clear metadata and controlled vocabularies (species, habitat, and site codes)

## Access, Contact, and Citations
- Primary contact: ecn@ceh.ac.uk
- Data dissemination: Data uploaded to relevant portals; site managers document survey details and quality
- Citation expectations: Acknowledge ECN data usage; provide one reprint of any publication citing the data

## Governance and Stewardship Considerations
- Metadata completeness: Ensure SITECODE, SDATE, TRANSECT, BATLOC_ID, FIELDNAME, VALUE, ACTS, ACTH, ACTF are consistently populated
- Standards alignment: Maintain alignment with ECN protocols and harmonized site/species/habitat code mappings
- Data updates: Implement clear update processes to reflect new survey data and quality notes while preserving provenance
- Interoperability: Use shared codes for sites, species, and habitats to facilitate cross-dataset discovery and reuse
- Attribution and impact: Track dataset usage to gauge value and support funding justifications; request reprints as specified
- Storage and sharing: Ensure data are stored with stable identifiers and accessible metadata; monitor embargoes and sharing permissions across portals