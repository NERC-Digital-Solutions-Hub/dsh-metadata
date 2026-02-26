# UK Environmental Change Network (http://www.ecn.ac.uk) Vegetation: Woodland (VW)

- Overview
  - Dataset originator: ECN Data Centre, Centre for Ecology and Hydrology
  - Dataset owners: UK Environmental Change Network (ECN) programme, funded by UK government departments/agencies
  - Focus: woodland vegetation data collected under ECN protocol
  - Access points: ECN Data Centre (data.ecn.ac.uk) and Environmental Information Platform
  - Publication attribution: acknowledge data use; request one reprint of any publication citing the data

- Data Governance and Stewardship
  - Commitment to good data management: metadata capture, standardized field codes, consistent structures across sites
  - Data sharing and reuse governance to monitor usage and value
  - Stakeholders: government bodies supporting ECN; ongoing data contribution and network coordination
  - Challenges for data stewards: timely receipt from sites; aligning metadata across protocols; integrating legacy and current systems; interoperability with evolving standards

- Data Model, Structure, and Storage
  - Core storage model: two Oracle tables per site
    - D1VW_xxx: site core data
    - D2VW_xxx: plot/field data
  - Site coding: T08 (Wytham) and T09 (Alice Holt) with date ranges 1993–2012 and 1994–2011 respectively
  - Data structure aligns with ECN metadata framework; core fields include identifiers, dates, species, measurements, and data values
  - Site-specific fields and codes: SITECODE, SYEAR, PLOTPID, CELLID, TREEID, STEMID, TREE_SPEC, FIELDNAME, VALUE; additional dates for dominance, height, DBH, seeds, etc.
  - Metadata and protocol documentation: accompany data to aid interpretation and reuse

- Cadence, Scope, and Updates
  - Field sampling cadence: woodland plots surveyed on a nine-year cycle; DBH measurements every three years
  - Scope: woodland sites with associated coarse-grain vegetation datasets
  - Potential for future updates and extensions as new measurement cycles occur
  - Importance of consulting quality metadata when interpreting updates and changes over time

- Quality, Metadata, and Documentation
  - Quality information accompanies each dataset; measurement methods and plot definitions documented
  - Quality codes and metadata enable users to assess data reliability and limitations
  - Standard ECN quality codes (see list), plus a catch-all 999 for unusual events with accompanying narrative
  - Protocols and metadata standards designed to support robust interpretation and interoperability

- Species and Field Codes: Dictionaries and Crosswalks
  - Extensive species code dictionary mapping Latin names to cross-referenced concepts (including synonyms and cross-references to other taxonomic concepts)
  - Codes cover broad taxonomic groups (trees, shrubs, forbs, bryophytes, lichens, etc.) and life stages (canopy, subcanopy, seedlings)
  - Cross-references facilitate interoperability when merging with other datasets
  - Fieldname taxonomy includes terms for saplings, canopy, diameter at breast height (DBH), height, seedling surveys, shrub layer, and more
  - Example entries illustrate many-to-one mappings and synonym handling (e.g., Salix cinerea subspecies oleifolia variants mapped to current accepted names)

- Data Quality, Documentation, and Usability Notes
  - Quality and methodological documentation provide guidance on data handling and interpretation
  - Long-term datasets may be updated or extended; users should reference accompanying quality information for each dataset
  - Data users are encouraged to use the dictionaries to translate codes into meaningful biological information
  - Emphasis on provenance: track data origin, site coordinates, temporal coverage, and data lineage for reproducibility

- Practical Notes for Data Stewards and Users
  - Use the protocol and quality information to interpret plot-level and tree-level data
  - Refer to site metadata for exact site coordinates and date ranges
  - Consult species and field code dictionaries to translate codes into biological information
  - Acknowledge ECN data usage in outputs; provide reprints when possible
  - When integrating datasets, leverage the extensive species dictionaries and standardized quality codes to ensure consistency across sites and time