# Substrate utilisation profiles for saprotrophic fungi and moisture content data from soil sampled in an upland grassland experiment at Sourhope, Scotland, 2001 [NERC Soil Biodiversity Programme] - Supporting Information

## Executive summary
- Describes data from the NERC Soil Biodiversity Programme focusing on saprotrophic fungi in an upland grassland at Sourhope, Scotland, 2001.
- Combines substrate utilisation profiles (BIOLOG) of soil fungi and soil moisture data to understand decomposition roles of decomposer fungi amid high species richness.
- Includes methods for isolating fungi, characterization of functional capabilities, and detailed data dictionaries for four CSV datasets.
- Provides context on field site, treatments, and the overarching aim to link fungal diversity with key soil ecological processes.

## Data assets and contents
- Datasets provided
  - Dataset 1105: Percentage Soil Moisture Content (P2111_PERCENT_SOIL_MOISTURE.csv)
    - Variables include ROWNO, SUID, SAMPLE_DATE, BLOCK, MAIN_PLOT, TREATMENT, HORIZON, WEIGHT_BOAT, WEIGHT_SOIL, TOTAL_DRYWEIGHT1/2, DRYWEIGHT_SOIL, PERCENTAGE_MOISTURE.
  - Dataset 1130: Substrate utilisation assay, using BIOLOG SF-N2 microplates (P2111_BIOLOG_RESULTS.csv)
    - Includes SPECIESID, REPLICATE, TIME, ISOLATE_TYPE, BIOLOGCELLID, OPTICAL_DENSITY.
  - Dataset 1131: Details of the BIOLOG SF-N2 microplates (P2111_BIOLOG_INFORMATION.csv)
    - Includes BIOLOGCELLID, SUBSTRATE, SUBSTRATE_TYPE.
  - Dataset 1132: Details of Species examined using the BIOLOG SF-N2 microplates (P2111_BIOLOG_SPECIES.csv)
    - Includes SPECIESID, SPECIES_NAME.
- Data structure context
  - Four CSV files cover soil moisture measurements, BIOLOG-based functional assays, and the associated substrate/species metadata.

## Data collection and processing (Methods)
- Field site and experimental design
  - Sourhope field experiment, upland grassland at 309 m a.s.l., mean temp 7.8°C, mean annual precipitation 952 mm.
  - Soil type: brown forest; vegetation dominated by Agrostis capillaris, Festuca rubra, Nardus stricta, Anthoxanthum odoratum, Poa pratensis.
  - Experimental treatments: Control, Lime (CaCO3), Nitrogen (NH4NO3), Lime + Nitrogen.
- Fungal isolation and culture
  - Isolated microfungi and basidiomycetes from soil, standing-dead plant material, and basidiomata using Warcup soil plating methods.
  - Representative isolates chosen from horizons (LF, H, A) and treatments to form a cross-section of the fungal community.
  - Basidiomata collected and germinated on PDA with antibiotics for identification.
- Functional characterization
  - Utilised a two-step approach:
    1) Substrate utilisation on semi-defined solid media for key substrates (cellulose, lignin, pectin, starch, chitin).
    2) BIOLOG SF-N2 microplates to profile carbon utilisation across 95 low molecular weight substrates.
  - Standardization
    - Inoculum density standardized using carageenan matrix to achieve consistent optical density; plates incubated at 15°C for up to 28 days.
    - BIOLOG readings taken up to 25 days (590 nm absorbance) using a plate reader; total activity used as a metric for functional diversity.
  - Taxonomic breadth
    - 12 isolates selected (6 abundant, 6 occasional; plus functionally unique representatives) spanning 20 anamorphic fungi, 10 Basidiomycota, 6 Zygomycota, 2 Ascomycota.
- Analytical approach and findings (summarized)
  - Found high functional redundancy in cultivable decomposers, but infrequent taxa contributed meaningfully to decomposition, with broader substrate utilisation and sometimes greater activity.
  - Co-inoculation of abundant and occasional taxa inferred slight positive effects on decomposition and cellulose degradation, with some negative effects on lignin degradation likely due to competition.
  - Occasional taxa potentially enhanced temporal resilience of decomposition; uncultured taxa not captured may further contribute to functional diversity.

## Data governance, quality, and usage notes
- Quality and documentation
  - Data sets are subject to quality assurance procedures; however, the issuing body (NERC) does not warrant the accuracy or fitness for a specific use and disclaims liability for data misuse.
- Metadata and discoverability
  - Datasets come with structured metadata descriptions for each field (e.g., data types, units, and sampling context).
  - References provided for deeper methodological and contextual understanding (see below).
- Accessibility and reuse
  - Data linked to published work (Deacon et al. 2006; related field data handbook) to aid context and reproducibility.
  - Users are encouraged to consult the Sourhope Field Data Handbook 2003 and related papers for additional data structure and site-specific details.

## Findings and implications for data strategy
- Ecosystem insight
  - Functional redundancy exists, but infrequent taxa contribute disproportionately to decomposition; diversity may enhance resilience of soil processes.
- Data products and collaboration
  - Rich, multi-omic-like data (culture-based functional assays and substrate profiles) support cross-site comparisons and synthesis across networks studying soil biodiversity and function.
- Governance considerations for Data Leaders
  - Importance of clear metadata schemas (dataset descriptions, field definitions, units, time points) to improve discoverability and reusability.
  - Need for standardized inoculum and assay protocols to enable cross-study comparability.
  - Emphasis on data provenance, proper caveats (QA status, liability), and cross-referencing with primary publications for methodological transparency.

## Access and references
- Primary publication context: Deacon, L.J., et al. 2006. Diversity and function of decomposer fungi from a grassland soil. Soil Biology and Biochemistry, 38(1), 7-20.
- Supporting materials: SOURHOPE FIELD DATA HANDBOOK 2003 (via EIDC catalogue record).
- Related work: Usher, M.B., et al. 2006. Understanding biological diversity in soil: the UK's Soil Biodiversity Research Programme. Applied Soil Ecology, 33(2), 101-113.
- Disclaimer: NERC cannot warrant the accuracy of the data and holds no liability for their use.