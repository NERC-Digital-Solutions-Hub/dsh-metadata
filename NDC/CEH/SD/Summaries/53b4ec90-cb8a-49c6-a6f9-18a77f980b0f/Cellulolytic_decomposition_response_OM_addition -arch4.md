# Cellulolytic decomposition of Welsh upland rivers in response to organic matter addition

- Study aim and design
  - Investigates how added leaf litter affects cellulolytic decomposition in upland streams.
  - BACI (before-after-control-impact) design: each stream has an upstream reference zone and a downstream experimental (manipulated) zone, with 20–50 m separation to ensure independence.
  - Timeline:
    - Before period (T1): ~61–65 days, Nov 2012–Jan 2013; no manipulation; both zones treated equally.
    - After period (T2): ~57–62 days, Jan–Mar 2013; experimental zone receives leaf litter throughout.
  - Manipulation details: one tonne bags of oak, birch, and alder litter distributed proportionally to experimental zones; additional leaf litter (630 kg wet weight) added on Feb 12 and Mar 5, 2013 after storm events to maintain leaf litter levels.

- Data collection and measurements
  - Experimental units: six cotton strips placed randomly in each reach (experimental sites) before and after manipulation.
  - Processing:
    - Strips recovered at end of T1 and T2, frozen at -20°C.
    - In lab: rinsed, oven-dried to constant mass at 65°C, and tensile strength measured with a Hounsfield machine (25 kN load cell, 40 mm gap).
    - One breaking-strain estimate per strip; three untreated control strips used to account for transport/wash losses.
  - Related references noted for methodology (e.g., Jenkins et al. 2013).

- Data structure and content
  - Data are flatbed CSV files comprising 10 columns:
    - site_code: sampling site identifier
    - region: stream basin
    - date: sampling date
    - time: whether sample was collected Before or After manipulation
    - landuse: basin land-use
    - reach: Experimental or Control site
    - replicate: replicate code (A–F)
    - exposure: days exposed
    - breaking_strain: tensile strength (Newtons)
    - %_loss: percent loss of tensile strength relative to control
  - Purpose: capture cellulolytic decomposition measurements across sites, periods, and treatments.

- Ancillary data and metadata
  - Supporting site description file: DURESS_CU_site_description.csv with 10 fields (Site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey, Catchment).
  - Data format: CSV; explicit note that data consist of 10-column records; links to references and context provided.
  - References and context: includes citations to related ecological studies; links to external sources referenced in the dataset (not guaranteed to persist).

- Data quality and governance notes
  - Calibration: none reported.
  - Quality control: none reported beyond inclusion of untreated control strips.
  - Metadata and standards: basic dataset schema documented (columns and units), but no explicit QA/QC procedures or data standards described.
  - Data accessibility: described as part of a data catalogue with potential external links; note that some linked resources may not persist.

- Relevance for data-leadership and data-system considerations
  - Demonstrates end-to-end data lifecycle: experimental design, field sampling, laboratory measurement, data structuring, and ancillary metadata.
  - Highlights importance of clear metadata (structure, units, replication, timing) for data discoverability and reuse.
  - Illustrates potential governance gaps (absence of formal QA/QC, calibration details, and explicit data standards) that Data Leaders should address to improve data quality, interoperability, and long-term discoverability.