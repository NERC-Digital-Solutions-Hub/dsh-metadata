# UK Environmental Change Network (http://www.ecn.ac.uk) Vegetation: Coarse Grain (VC) Dataset

- Overview
  - ECN vegetation monitoring dataset; Data Centre as originator; owners are a consortium of UK government departments/agencies.
  - Usage acknowledgement requested and one reprint of any citing publication to be sent.

- Protocol and sampling design
  - Fifty plots per site (2m x 2m); species presence/values recorded in 25 subcells (40cm x 40cm) per plot.
  - Surveyed on a nine-year cycle; woodland plots collected under a separate woodland protocol.
  - Analysis should incorporate accompanying quality information.

- Data coverage and site details
  - Site codes (e.g., T01 Drayton, T02 Glensaugh, …, T12 Cairngorms) with coordinates provided.
  - Date ranges vary by site (roughly 1993–2012 for many; some diverge).

- Data structure and contents
  - Core vegetation data: D1VC_xxx tables (one per site) with SITECODE, SYEAR, PLOTPID, CELLID, FIELDNAME, VALUE.
  - Environmental data: D2VC_xxx tables with site attributes (e.g., PEDATE, LANDUSE, SLOPE, ASPECT, etc.).
  - Cell-level data: D3VC_xxx tables detailing cell-specific features.
  - Metadata and reference tables (M_DESC, M_REFFIELD); stored in Oracle with per-site tables to ease extraction and cross-site comparison.

- Coding, metadata, and data quality
  - Extensive code mappings for Land Use, Slope Form, physical features, and species codes; large dictionaries linking codes to names (Latin and EC concepts).
  - Quality information is essential for interpretation; metadata documents field names, codes, and data provenance.

- Data access and references
  - Protocol reference: http://www.ecn.ac.uk/measurements/terrestrial/v
  - ECN Data Centre: http://data.ecn.ac.uk (ecn@ceh.ac.uk)
  - Data portals host datasets and metadata; data use acknowledgements and publication copies requested.

- Considerations for analysts
  - Scale and coverage: coarse vegetation data with dense code dictionaries; local-scale analyses may be hampered by scale or missing local boundaries.
  - Data integration: harmonizing field names, reference codes, and cross-site year alignment required.
  - Data provenance and quality: track sources and use accompanying quality metadata to inform analyses.
  - Practical use: designed to identify correlations, build predictive models, and inform environmental-change decisions; outputs typically charts with clear conclusions.

- Text: Appendix Elements (Species codes and Quality Codes)
  - Species codes: extensive mappings linking numerous species names and synonyms (e.g., Salix species, Sphagnum taxa, Scabiosa, etc.) to standardized codes and alternate names; indicates broad synonymy and taxonomic mappings within the dataset.
  - Quality Codes: standardized ECN quality codes (100–999) describing data quality issues (e.g., no information, sample lost, partial loss, degradation, anomalous events); 999 reserved for unusual events with accompanying text.