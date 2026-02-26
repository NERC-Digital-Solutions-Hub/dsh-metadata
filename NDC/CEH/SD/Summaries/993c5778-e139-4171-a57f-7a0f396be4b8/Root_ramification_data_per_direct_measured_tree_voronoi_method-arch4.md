# DATA HEADER INFORMATION for: Root_ramification_data_per_direct_measured_tree_voronoi_method.csv Please also see Manual_2_Belowground_Root_Survey, page 10.

- Overview
  - Describes a dataset that records target tree root architecture by tagging and measuring each coarse root (up to 1 cm diameter) branching for every target tree.
  - Focuses on direct measurement using a Voronoi method to associate ramification with excavation context.

- Provenance and acknowledgments
  - Programme: ESPA; Project: P4GES.
  - DOI: https://doi.org/10.5285/993c5778-e139-4171-a57f-7a0f396be4b8
  - Data products derived with acknowledgement required for Laboratoire des Radio Isotopes, Université d'Antananarivo.

- Data content and structure
  - Zone and site metadata
    - ZOI (Zone of Interest): Categorical; examples include ZOI2: Andasibe, ZOI3: Anjahamana.
    - Site: Text string code for the collection location.
  - Target and sampling identifiers
    - Local name: Vernacular/ local name of the inventoried species.
    - DBH Class: Categorical (L: Large, M: Medium, S: Small) representing trunk diameter class at breast height.
    - Code_target_tree: Text string code linking to site, species name, and diameter class.
  - Ramification measurements (per ramification)
    - Number of ramification: Numeric; counts ramification from the north.
    - DiH / DiV: Horizontal and vertical diameters at the beginning of each ramification (cm).
    - DfH / DfV: Horizontal and vertical diameters at the end of each ramification (cm).
    - DfM: Mean diameter at end of ramification, computed as (DfH + DfV) / 2 (cm).
    - Total_weight: Weight of each ramification (g).
    - Total_length: Length of each ramification (cm).
    - Orientation: Categorical; indicates direction or context:
      - Vor: ramification from the Voronoi triangle where the root was excavated.
      - PV: taproot (vertical root sinking into ground).
      - N, S, E, W: cardinal directions.
      - NA: not available (ramification direction not visible or blocked).
  - Data types and units
    - Most fields are numeric (with cm, g, numeric counts) or categorical strings as described.
    - DfM, DiH/DiV, DfH/DfV, Total_length in centimeters; Total_weight in grams.

- Measurements and methodology
  - Measurements performed with calipers or Vernier calipers.
  - Ramifications classified by orientation and linked to the excavation context via Voronoi methodology or taproot classification (PV).

- Metadata and data quality considerations
  - Explicit definitions for each field are provided (names, meanings, units, and data types), aiding discoverability and consistent interpretation.
  - Orientation codes distinguish excavation context (Vor) from root type (PV) and directional information (N/S/E/W) or missing data (NA).
  - The dataset references an accompanying manual (Manual_2_Belowground_Root_Survey, page 10) for methodological details.

- Access, use, and provenance notes
  - DOI provided for citation and traceability.
  - Data products require acknowledgment of the Laboratory of Isotopes or related institutions.
  - Intended for analyses of root architecture and relationships to site/DBH classes, enabling cross-site comparisons within the ESPA/P4GES framework.

- Relevance for data strategy and governance (Data Leaders perspective)
  - Rich, highly granular root-architecture data with clear metadata, enabling advanced data discovery and reuse.
  - Well-defined data dictionary supports standardization across datasets and improves interoperability.
  - Provenance, project context, and acknowledgment requirements support proper governance and collaboration across networks.
  - The explicit linking of records to site, zone, and Code_target_tree facilitates integration with broader ecological or forest datasets.