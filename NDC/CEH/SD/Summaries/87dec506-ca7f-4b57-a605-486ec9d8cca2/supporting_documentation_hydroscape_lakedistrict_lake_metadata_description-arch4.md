# File Uploaded to EIDC: hydroscape_lakedistrict_core_metadata.csv

- Overview
  - Metadata CSV uploaded to EIDC detailing core sediment data for Hydroscape Lakeland District lakes.
  - Captures identifiers, location, lake metadata, core-site classification, measurement data, corer types, collection date, internal coding, and 210Pb dating status.

- Key fields and data dictionary highlights
  - WBID: Waterbody Identification number; links to lakes index (CEH reference).
  - Hydroscape: Name of the Hydroscape region used.
  - Lake Name: Name of the lake.
  - General_location_of_core: Core site classification (deep, littoral, intermediate).
  - OSGB36_E / OSGB36_N: UK Ordnance Survey grid coordinates (Eastings, Northings; OSGB36 datum).
  - Water_depth_at_core_site_(m): Water depth from surface to sediment at core site; measured by handheld echo sounder; littoral depth confirmed with Secchi depth method.
  - Secchi_disc_depth_(m): Mean Secchi depth from three measurements; taken at the deepest lake position.
  - Core_length_and_type: Core length in metres; lists corer types with literature references (Tapper, Big Ben, Livingstone, Renberg).
  - Date_core_collected: Fieldwork and core collection date (dd/mm/yyyy).
  - UCL_Code: Internal UCL code used on bags/database.
  - UCL_Sample_ID: Internal unique ID for the entire sample core (Amphora system).
  - 210 Pb-dated_Y_N_for_Hydroscape: Indicates if the core was dated by 210Pb (Yes/No).

- Methods and data provenance
  - Water depth: measured with a handheld echo sounder from a boat.
  - Littoral depth confirmation: Secchi depth used to verify littoral areas.
  - Secchi depth: three measurements averaged to yield mean depth.
  - Core types: references provided for each corer design used (Tapper, Big Ben, Livingstone, Renberg).

- Data quality, standards, and metadata considerations
  - Coordinates provided in OSGB36, enabling cross-referencing with UK datasets.
  - Internal sample identifiers (UCL_Code, UCL_Sample_ID) ensure traceability of samples and bags.
  - Descriptions include measurement methods and corer references to support reproducibility.
  - Clear status field for 210Pb dating, aiding dating strategy planning and data interpretation.

- Implications for data strategy and governance
  - Facilitates data discovery and cross-lake comparisons through standardized fields (IDs, coordinates, core-site classification, measurement values).
  - Supports assessment of data suitability, gaps, and prioritization for future collection (e.g., depth and dating status).
  - Enhances provenance and reproducibility with explicit methods and references.
  - Aids coordination with partners and integration into the broader Hydroscape data ecosystem.

- Next steps and quality actions (for Data Leaders)
  - Ensure consistent metadata documentation across similar datasets to improve discoverability.
  - Maintain units, coordinate systems, and naming conventions aligned with data standards.
  - Validate completeness of fields (e.g., ensure 210Pb dating status is available for all cores).
  - Plan for updates and versioning, linking to external lakes indices and related datasets.