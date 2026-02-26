# LAC Project Datasets and Methodology

- Datasets included
  - LAC_Ruppert_1cm_dataset.csv
  - LAC_Ruppert_2cm_dataset.csv
  - LAC_WBP_dataset.csv
  - LAC_Nor1_dataset.csv
  - LAC_Nor3_dataset.csv
  - LAC_AT2_1cm_dataset.csv
  - LAC_AT2_2cm_dataset.csv

- Authorship and affiliations
  - Contributors from Geography and Environment, University of Southampton; Environmental Change Research Centre, UCL; School of Geography, University of Nottingham; Department of Geography, Loughborough University; Limnology Laboratory, University of Regina; and related campuses, reflecting a multi-institution collaboration across the UK, Canada, and Malaysia.

- Experimental design and sampling
  - One sediment sequence collected from the deepest part of each study lake using overlapping drives.
  - Cores obtained from diverse locations: Ruppert (Alaska), Woody Bottom Pond (Alaska), NOR1 (Camping Pond, Norway), NOR3 (Dalmutladdo, Norway), AT2 (Greenland).
  - Cores processed with standardized subsampling: continuous 1 cm and 2 cm sections; analyses performed at 1 cm (most) or 2 cm (macrofossils, chironomids, cladocera) resolution; XRF at higher (200–400 μm) resolution.
  - Subsampling performed in the UK; surface cleaning of cores prior to sectioning; running depth profiles created by correlating overlapping sections.

- Analytical methods and data types
  - Loss on Ignition (LOI) for organic matter, carbonate, and dry mass metrics; densities calculated.
  - Diatoms: quantitative counts (≥200 valves per sample), species-level identifications where possible; results expressed as % abundance and concentrations.
  - Biogenic silica (BSi): dissolved silica via alkaline digestion and ICP-MS; calibration and reference standards documented.
  - Isotopes: δ13C and δ15N (bulk sediment) with percent C and N; accuracy checked against standard references.
  - XRF: element counts with normalization to total counts; 1 cm binning for cross-dataset comparability.
  - Macrofossils: dense plant/animal remains; treated and sieved; abundance represented as individuals per 100 ml sediment or as abundance scores.
  - Chironomids and Cladocera: standard preparation, digestion, sieving, and identification protocols; counts converted to abundance and concentrations.
  - Pigments: HPLC analysis for chlorophylls and carotenoids; concentrations calculated using calibration standards.
  - Pollen: standard digestion and acetylation; counts converted to percentage abundance.
  - Data format: CSV files with detailed column definitions and units.

- Data processing, quality control, and governance
  - Data are quality assured with checks against detection limits; cross-checks against previous samples and sequences, and internal consistency checks during data entry.
  - Uncertain identifications flagged in metadata (e.g., “cf” designations) and with explicit notes in data sheets.
  - Metadata-driven data management: explicit data governance elements and data management plans referenced; calibration standards, blanks, and reference materials used in QA/QC.
  - Abbreviations and units provided for all columns; running depth and section depth clearly defined (Running_top_cm, Running_bot_cm).
  - Data stored as comma-separated values (CSV); column mappings and unit descriptions provided to facilitate reuse and interoperability.

- Format, units, and data content pointers
  - 1 cm and 2 cm resolution datasets (where applicable) with 1 cm-binned XRF data; depth-aligned data across cores.
  - Column categories include running depth headers, LOI metrics (DW%, LOI550%, carbonate), diatom metrics (counts, %abundance, concentrations), geochemistry (Biogenic Si, δ13C, δ15N, C:N, Fe/Mn/Ti/Zr metrics), macrofossil and invertebrate counts and fluxes, pigments (nmol/g organic mass), pollen (percentages, raw counts, marker pollen), and various taxa lists (diatoms, chironomids, cladocerans).
  - Data dictionaries and reference tables (e.g., Table 2 with column definitions) accompany the datasets to ensure reproducibility.

- Provisional references and methodological basis
  - Diatom preparation and counting protocols (Renberg; Krammer & Lange-Bertalot; related diatom literature).
  - Biogenic silica methodology and standard references (Conley & Schelske; Conley reference materials).
  - Isotope analysis setup and standards (BEIF facility, USGS/IAEA standards).
  - Pollen and macrofossil identification resources and taxonomic guides (Birks, Moore et al.; various regional flora/fauna references).
  - Data handling and analysis tools (TILIA/TILIA*GRAPH for pollen; standard QA procedures; ITRAX XRF core scanner references).

- Relevance to monitoring framework authors
  - Demonstrates end-to-end monitoring data workflow: from field sampling design, through multi-proxy laboratory analyses, to structured, well-documented data products.
  - Emphasizes data provenance, metadata completeness, and data quality assurance—key for governance, transparency, and reproducibility in monitoring frameworks.
  - Highlights collaboration across institutions to overcome data gaps and share best practices, a common challenge area for environmental health monitoring programs.
  - Provides a comprehensive example of data sharing readiness with explicit data formats, units, and column definitions to facilitate reuse in policy evaluation and decision-making contexts.