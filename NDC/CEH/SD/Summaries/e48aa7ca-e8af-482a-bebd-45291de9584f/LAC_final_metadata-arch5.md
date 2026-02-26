# LAC Project Datasets

- A multi-proxy lake sediment dataset compilation describing seven CSV datasets (LAC_Ruppert_1cm_dataset.csv, LAC_Ruppert_2cm_dataset.csv, LAC_WBP_dataset.csv, LAC_Nor1_dataset.csv, LAC_Nor3_dataset.csv, LAC_AT2_1cm_dataset.csv, LAC_AT2_2cm_dataset.csv) with detailed authorship, affiliations, sampling design, analytical methods, and data formats.
- Datasets cover cores from Alaska (Ruppert and Woody Bottom Pond), Norway (NOR1, NOR3), and Greenland/Greenland-adjacent sites (AT2) with overlapping objectives and harmonized measurement approaches.

- Authorship and provenance
  - Each dataset lists the contributing researchers and their affiliations (multiple UK universities and Canadian/ Malaysian affiliates), enabling clear attribution and contact points.
  - Linkages between datasets and project team support reproducibility and accountability.

- Scope and purpose for Data Stewards
  - Purpose: to ensure datasets meet governance standards, are easily discoverable, and remain usable by others. Includes metadata on sampling regime, analytical methods, and quality control.
  - Datasets are intended for long-term storage, sharing via standard formats (CSV), and cross-proxy integration (LOI, diatoms, isotopes, XRF, macrofossils, pollen, pigments, etc.).

- Experimental design and sampling regime
  - 1 sediment sequence per lake, collected from the deepest site using overlapping drives; cores are subdivided into 1 cm and 2 cm resolution segments (with 2 cm used for certain proxies like macrofossils, chironomids, and cladocera; XRF at 200–400 μm resolution).
  - Distinct sequences are merged where necessary to create continuous running-depth profiles.
  - Subsampling and cross-core linkage are documented to allow running-depth alignment across datasets.

- Proxies and analytical workflow (high-level)
  - LOI (loss on ignition) for dry weight, organic matter, and carbonate content; used for density calculations and correlation of overlapping sections.
  - Diatoms: preparation and counts with species-level identification where possible; abundances and concentrations reported.
  - Biogenic silica (BSi): extraction and measurement via ICP-MS; multiple samples per depth interval; quality controls with reference standards.
  - Isotopes: δ13C and δ15N; C and N percentages; standardized with reference materials and quality checks.
  - XRF: element counts with normalization by total counts; 1 cm bin averages for key elements (Ca, Fe, Ti, Zr) to align with other proxies.
  - Macrofossils, Chironomids, Cladocera: detailed taxonomic or abundance data with standardized preparation and counting protocols; fluxes and concentrations calculable when combined with sedimentation rates.
  - Pigments: HPLC-based quantification of chlorophylls and carotenoids to characterize algal communities.
  - Pollen: standard preparation and counting; results expressed as percentages against depth.
  - Metadata fields and data interpretation notes accompany each proxy to support reproducibility.

- Data structure and format
  - Data stored as comma-separated values (CSV) with explicit column headers.
  - Example running-depth fields: Running_top_cm, Running_bot_cm; sample identifiers (SubID); proxy-specific columns (e.g., LOI, DW_%, LOI550_%dw, WetDensity_gcc, DryDensity_gcc, BulkDensity_gcc).
  - Proxies include extensive taxonomic lists (Diatoms, Cladocera, Chironomidae) and geochemical/pigment/pollen columns with defined units (e.g., %abundance, mg/kg, nmol/g, ‰ for isotopes).
  - Abbreviations and units table (Table 2) standardizes column names and units; isotopic data reported in per mille (δ13C, δ15N), concentrations in SI units, and macrofossil data as counts or abundance scores.

- Quality control and data integrity
  - Ongoing checks for detection limits, data entry errors, and cross-validation against previous cores at the same locations.
  - Use of blanks, reference standards, and comparisons between overlapping core sections to ensure consistency.
  - Taxonomic identifications linked to published identification keys and regional references; uncertain IDs flagged with cf or unID notation and documented in metadata.

- Data governance and stewardship considerations
  - Provenance: detailed authorship, affiliations, and project context enable traceability and credit allocation.
  - Harmonization: standardized sampling resolutions and measurement protocols facilitate cross-core integration, while still documenting site-specific nuances.
  - Interoperability: CSV format with clearly defined column headers and units supports reuse in common analytical pipelines; normalization and conversion practices are described (e.g., XRF normalization, diatom concentration calculations).
  - Updates and maintenance: data management plan referenced for ongoing quality checks and cross-core validation; metadata-rich design supports future updates and dataset extension.
  - Access and licensing (implied): data are stored in a standardized, shareable format with explicit methodological metadata, promoting discoverability and re-use within the scientific community.

- References and documentation
  - Methods and proxies draw on established literature and standard references for diatoms, Cladocera, Chironomidae, pollen, pigments, LOI, isotopes, and XRF.
  - Documentation includes detailed protocols for laboratory preparation, data processing, and quality control, enabling reproducibility and audit trails.

- End-user guidance for Data Stewards
  - Ensure ongoing alignment with the project’s data management plan and cross-proxy harmonization efforts.
  - Maintain clear links to authors and affiliations for data provenance inquiries.
  - Preserve full methodological context (sample depths, resolutions, core running depths) to facilitate re-use and integration in future studies.
  - Monitor for potential interoperability issues due to legacy formats or proxy-specific idiosyncrasies, and apply standardized conversion where appropriate.