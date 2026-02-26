# SOURHOPE FIELD DATA HANDBOOK 2003

- Purpose and scope
  - Documents soil profiles and vegetation data for Rigg Foot (Sourhope), focusing on Blocks 4 and 5, with accompanying ECOTRON plots.
  - Supports long-term biodiversity and soil-vegetation research within archiving and data-sharing contexts.

- Data assets and structure (block-level summary)
  - Block 4
    - Soil profiles include horizons LF, FH, H, Ah, Abg, B sg, C gx (depths from 0 to ~95 cm or more), with detailed soil descriptions (color, structure, roots, stones).
    - Horizon-level soil analyses: measurements such as weight, %N, %C, C:N ratio, Ca, Na, K, Mg, %Moisture loss, LOI, pH (H2O) and pH (CaCl2).
    - Auger samples (4A–4F) with corresponding soil chemistry data and physical properties.
    - Vegetation surveys for plots (e.g., PLOT 4A–4D) including species counts and presence/absence data across subplots.
  - Block 5
    - Site details: grid NT8544019520; altitude ~315 m; slope ~5°; Imperfect drainage; major soil subgroup described as Brown forest soil with gleying; rock types include undifferentiated intermediate igneous and andesite.
    - Soil profiles: horizons LF, FH, H, Ah, AB, Bg, BCg, Cg with color descriptors, mottling, structure, root presence, and abundance of igneous stones; depth ranges up to 100 cm.
    - Horizon-level soil analyses: weight, %N, %C, C:N, Ca, Na, K, Mg, %Moisture loss, %LOI, pH (H2O) and pH (CaCl2).
    - Auger samples (5A–5F) with comparable metrics to Block 4 (N, C, C:N, Ca, Na, K, Mg, moisture loss, LOI, pH).
    - Vegetation surveys for plots (PLOT 5A–5F) with subplots, species totals, and presence/absence data.
  - ECOTRON PLOT
    - Soil analysis: weight, %N, %C, C:N, Ca, Na, K, Mg, %Moisture loss, %LOI, pH(H2O), pH(CaCl2).
    - Vegetation surveys with subplot-level species counts and totals.

- Data types, collection methods, and scope
  - Soil data
    - Ground-truth horizon descriptions (color, texture, mottling, structure) and depth ranges per block.
    - Chemical and physical properties measured per horizon and per auger sample.
    - Long-term storage and archiving for soil samples (e.g., -80°C storage for certain samples in Block 4 context).
  - Vegetation data
    - Quadrats or subplot-based surveys per main plot; species lists, presence/absence with potential abundance details; track vegetation community composition.
  - Data provenance and linkage
    - Data organized by block and plot, with metadata linking horizons, subplots, plots, and sampling events.
    - ECOTRON and main field plots integrated into the same data framework for cross-site analyses.

- Data quality, limitations, and harmonization notes
  - Horizon nomenclature and depth definitions vary across blocks, requiring harmonization for cross-block analyses.
  - Some datasets show incomplete or missing values (represented by placeholders), indicating uneven sampling coverage across plots and horizons.
  - Early sampling coverage is limited in some blocks (e.g., partial subplot sampling), so results are indicative rather than exhaustive for entire sites.
  - Variable presence and density of roots, stones, and mottling across horizons necessitate careful interpretation when comparing blocks.

- Data governance, availability, and reuse considerations for Data Leaders
  - Provenance and storage
    - Data tied to MLURI infrastructure with long-term archival; soil samples archived with associated metadata.
  - Discoverability and metadata
    - Rich multi-horizon, multi-plot metadata already captured but would benefit from:
      - A unified data dictionary mapping plots, subplots, blocks, horizons, and depth ranges.
      - Standardized coding for horizon names and measurement units across blocks.
      - Protocol documentation for measurement methods and units to ensure interoperability with external datasets (e.g., ECN, Micronet).
  - Data quality and gaps
    - Acknowledgement of incomplete subplot sampling and horizon-name inconsistencies; plan for systematic, comprehensive sampling and harmonization in future iterations.
  - Practical implications for data leadership
    - Demonstrates a complex, multi-dimensional data ecosystem (plots, subplots, horizons, vegetation, soils, long-term archives) suitable for interoperability, quality control, and biodiversity-vegetation analyses.
    - Opportunities to formalize metadata standards, harmonize horizon nomenclature, and build centralized data access that links vegetation, soils, and environmental context from ECN.
  - Endnotes and supplementary resources
    - References to methodological outputs (e.g., Twinspan, Association analyses) and Appendices with block-level data for meta-analytic cross-site work.

- Practical takeaways for Data Leaders
  - The Sourhope dataset exemplifies a layered data architecture (plots, subplots, horizons, quadrats, soil cores, long-term archives) ideal for testing data interoperability, quality assurance, and cross-domain biodiversity questions.
  - Key opportunities:
    - Formalize metadata standards and a unified data model to enable cross-block and cross-site reuse.
    - Harmonize horizon naming and units across blocks to improve cross-study comparisons.
    - Design scalable data pipelines that integrate vegetation and soil data with environmental context from ECN and related networks.
    - Develop a centralized data portal to improve discoverability, provenance tracking, and reuse by internal teams and external collaborators.

- Notable concrete data points (illustrative)
  - ECOTRON PLOT soil example: %N 0.59; %C 8.22; C:N 13.83; Ca 2.76 meq/100g; pH(H2O) 4.79; pH(CaCl2) 3.82.