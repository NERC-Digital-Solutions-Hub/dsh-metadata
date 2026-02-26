# ECN Wytham Exclosures Dataset

- Purpose and governance
  - ECN Wytham vegetation data are collected to produce comparable, up-to-date datasets for environmental change research, with clear data governance and acknowledgment requirements.
  - Dataset Originator: ECN Data Centre, Centre for Ecology and Hydrology; Owners: UK Environmental Change Network programme; funded by multiple UK government departments/agencies.
  - Governance focuses on standard operating procedures to ensure site comparability; data usage is monitored by data owners.

- Data content and structure
  - Scope: vegetation data from Wytham deer exclosure plots (exclosures vs controls) using ECN coarse-grain and woodland protocols.
  - Datasets include:
    - ECNWythamExclosures_species_present: vegetation presence data by plot, cell, and species code (VEG_SPEC) with quality indicators (Q1–Q3).
    - ECNWythamsExclosures_tree_data: tree data by TreeID, StemID, species, and measured variables.
  - Data fields exemplified: SITECODE, SYEAR, PLOTPID, CELLID, FIELDNAME, VALUE; TREEID, STEMID, TREE_SPEC, FIELDNAME, VALUE.
  - Supporting metadata and documentation: plot_info.csv, cell_info.csv, quality_info.csv (site managers assign QC codes; 999 for unusual events), quality text (ECN_VF_qtext.csv), explanatory site codes/features, and crosswalks for species codes to Latin names.

- Metadata, documentation, and references
  - Usage notes, data interpretation examples, and crosswalks to map species codes to Latin names (with extensive cross-references to taxonomic schemes).
  - Publications and DOIs linked to data products:
    - ECN coarse-grain vegetation data: Rennie et al. 2016
    - ECN woodland vegetation data: Rennie et al. 2017

- Access, use, and publication
  - Datasets are uploaded to ECN data portals and catalogues.
  - Users must acknowledge ECN data usage and submit a reprint of any publication citing the data.
  - Documentation emphasizes provenance, recording methods, and data quality to enable reproducibility.

- Data quality and standardisation
  - Protocol-driven data collection to support cross-site comparability; adherence documented.
  - Quality metadata: QC codes (Q1–Q8); unusual events documented via quality text (ECN_VF_qtext.csv).
  - Data updates: processes exist to manage updates and respect sharing limitations.
  - Crosswalks and coding tables (species, site codes) support interoperability and accurate interpretation.

- Data stewardship responsibilities (Data Stewards perspective)
  - Ensure data meet governance standards: standard protocols, complete metadata, and clear quality indicators.
  - Guide data creators/sharers on metadata requirements, quality codes, and documentation needs.
  - Manage data availability, embargoes, and disclosure risk; provide provenance and quality information.
  - Oversee data ingestion into portals/catalogues; maintain linkage to site documentation (plot/cell/quality files).
  - Document workflow and transformations; maintain traceability to source protocols.
  - Promote proper data acknowledgment by publishers and ensure reprint submissions as proof of usage.

- Particular challenges and mitigations
  - Incomplete understanding of user needs; mitigated with clear data dictionaries, usage notes, and crosswalks; ongoing documentation.
  - Timely data delivery; relies on site managers and standardized protocols.
  - Meeting metadata standards; enforce standard fields and provide context files.
  - Interoperability across systems/formats; centralized ECN protocols and crosswalks reduce heterogeneity; extensive coding tables aid interoperability.
  - Large/legacy datasets; use curated formats, stepwise uploads, and downloadable CSV templates.
  - Complex species coding; maintain/update crosswalks (VESPAN/BRC) and provide searchable dictionaries.

- Key takeaways for Data Stewards
  - The ECN Wytham Exclosures dataset is governed by explicit protocols, site metadata, and quality codes to support reusable, comparable data for environmental research.
  - Usage requires acknowledgment and publication reprint submission; rich documentation and crosswalks enable reuse and interoperability.
  - Governance includes ongoing dataset updates, preserved provenance, and rich metadata via multiple supporting files (plot, cell, quality, and species dictionaries).
  - Species and site mapping tables enhance discoverability and accurate interpretation across studies.

- Annex: Explanatory information highlights
  - Species codes: extensive mappings between coded taxa (e.g., Schistidium strictum) and Latin names, with multiple cross-references and alternative taxonomic concepts.
  - Quality codes: comprehensive list (e.g., 100 = no information; 101 = no sample taken; 126/127 = river/lake states; 999 = unusual event) to accompany data and provide context for data quality and potential limitations.