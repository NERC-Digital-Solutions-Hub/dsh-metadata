# NERC Soil Biodiversity Programme: Joint Sampling Event 2000

- Context and aims
  - Part of the NERC Soil Biodiversity Thematic Programme (established 1999) focused on intensive study at Sourhope, Scotland, to understand soil biodiversity, ecosystem processes, and functional roles of soil biota.
  - The programme funded 24 projects examining soil structure, carbon and nitrogen cycles, microfauna/ flora, and meso-/macro-fauna.
  - A joint sampling event (27–28 July 2000) coordinated multiple project groups to collect baseline measurements at the Sourhope field experiment site, enabling linkages across biomass, vegetation, and soil properties.

- Datasets available from the Joint Sampling Event (2000)
  - Root Cores Dataset (JT_SAMPLING_2000_ROOTS.csv)
    - Purpose: Biomass data for roots, shoots, and litter from soil cores.
    - Sampling details: 27–28 July 2000; Sourhope Rigg Foot Field Experiment Site; sub-plots S T U V across main plots (excluding Control 2).
    - Data structure: SUID, Sub_sample_ID, Sampling_Date, Treatment_Type, Block, Main_plot, Sub_plot, X_Cell, Y_Cell, Height, Width, Breadth, Litter_DW, Root_DW, Vol_litter, Vol_core, DWTSHDENS, DWTDENSLITT, DWTDENSROOT, etc.
    - Origin and access: MLURI (Macaulay/LUI); Ross, J.; Dawson, L.; dataset creation 26-2-2001.
  - Vegetation Survey Dataset (JT_SAMPLING_2000_VEG.csv)
    - Purpose: Vegetation species abundance for soil blocks, with abundance classes.
    - Sampling details: same spatial framework as Root Cores; includes treatment types per block.
    - Data structure: SUID, Sampling_Date, Treatment_Type (Control 1, Lime, Nitrogen, Nitrogen+Lime, Biocide), Block, Main_plot, Sub_plot, X_Cell, Y_Cell, Species, Abundance.
    - Abundance mapping: classes linked to % cover (e.g., not present to 100%), reference to Stace (1997).
    - Origin and access: MLURI; Buckland, S.; dataset creation 5-10-2000.
  - Soil Survey Dataset (JT_SAMPLING_2000_SOIL.csv)
    - Purpose: Soil profile descriptions by horizon with pH and moisture values.
    - Methods: pH measured in soil-water suspension following Sourhope field handbook protocols; moisture measured with Thetaprobe and calibrated to PC_Moisture values.
    - Sampling details: same site and sub-plot structure as other datasets; horizon-type descriptors per horizon and depth ranges.
    - Data structure: SUID, Sampling_Date, Treatment_Type (Nitrogen+Lime, Lime, Nitrogen, Biocide, Control 1), Block, Main_plot, Sub_plot, X_Cell, Y_Cell, Horizon_type, Horizon_subreg, Depth_upper, Depth_lower, Moisture_voltage, PC_Moisture, pH_H2O.
    - Origin and access: University of Stirling / MLURI; Bruneau, P.; dataset creation 27-9-2000.
  - Additional notes
    - Data dictionaries and dataset metadata accompany each file, detailing variable descriptions, units, and coding (e.g., SUID, Block/Main_plot/Sub_plot, X/Y_Cell).
    - Cross-referencing basis: Scott et al., 2003 for plot design; references to standard soil and vegetation methodologies (e.g., Hodgson & Avery, 1974).

- Data provenance, quality, and access
  - Provenance: Datasets generated during the joint sampling event as part of the NERC Soil Biodiversity Programme; multiple originators (MLURI, University of Stirling) with named contact persons.
  - Quality control: Numeric range checks, formatting checks, and logical integrity checks; data were subjected to QA procedures but without warranty of accuracy by NERC.
  - Access and reuse: Available as supporting information via the EIDC catalogue; dataset creation dates and contacting individuals provided; emphasis on clear documentation for reuse in monitoring and analysis.

- Metadata, standards, and governance implications for monitoring frameworks
  - Comprehensive metadata conventions demonstrated: explicit SUIDs, hierarchical plotting identifiers (Block, Main_plot, Sub_plot, X_Cell, Y_Cell), and detailed field sampling metadata.
  - Cross-dataset integration: aligned sampling framework across biomass, vegetation, and soil properties at the same time/space reference points, enabling integrated ecological monitoring analyses.
  - Measurement standardization: documented laboratory and field procedures (oven-drying, pH measurement, moisture reading, horizon delineation) to support reproducibility and comparability.
  - Data governance considerations: multiple data owners, clear dataset originators, and explicit data quality statements; potential governance lessons include ensuring metadata completeness, consistency across datasets, and transparent liability/usage terms.
  - Relevance for monitoring framework authors: illustrates the importance of linking biological biomass, vegetation surveys, and soil chemistry/physical properties within a single coordinated sampling event; exemplifies how to structure multi-domain environmental data for decision-support, with explicit data dictionaries and provenance.

- Limitations and contextual notes
  - Temporal and spatial scope: data from a single site and a single 2000 sampling event; broader monitoring requires additional timepoints and sites.
  - Accessibility constraints: while available via EIDC, users should review the accompanying metadata and data dictionaries to ensure appropriate use and interpretation.
  - References and compliance: datasets reference standard field methods and literature (e.g., Scott et al., 2003; Stace, 1997; Hodgson & Avery, 1974) to support methodology context.

- Useful references and contacts
  - Scott, J. et al. 2003. SOURHOPE FIELD DATA HANDBOOK (supporting information via EIDC catalogue).
  - Stace, C. 1997. New flora of the British Isles.
  - Hodgson, J. M., & Avery, B. W. 1974. Soil survey field handbook.
  - Dataset originators and contacts: Macaulay/LUI (MLURI), University of Stirling; named contacts for each dataset (e.g., Ross, J.; Dawson, L.; Bruneau, P.).
  - Data access reference: NERC Soil Biodiversity Programme data records and EIDC catalogue.