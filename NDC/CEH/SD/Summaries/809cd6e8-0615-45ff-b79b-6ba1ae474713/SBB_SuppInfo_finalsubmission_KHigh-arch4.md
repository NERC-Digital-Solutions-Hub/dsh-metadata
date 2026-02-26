# New approaches using mass spectrometry to investigate changes to cytokinin and abscisic acid (ABA) concentrations in soil in the presence of earthworms with or without plants

- Purpose and scope
  - Investigates how soil phytohormone (cytokinins: zeatin, iP; auxin: IAA; ABA; adenosine Ade) concentrations change in the presence of earthworms and/or plants, using mass spectrometry across soil and hydroponic systems.
  - Includes biochemical analyses (phytohormone levels), biology activity (FDH soil assay), plant biomass, soil chemistry (pH), and molecular biology (gene expression related to ABA synthesis and abiotic stress).

- Data availability and accessibility
  - All data are available from the EIDC data catalogue (High et al., 2019).
  - Data types span chemical measurements (phytohormone concentrations), enzymatic activity (FDH), plant biomass, soil moisture, pH, and molecular data (gene expression).

- Data provenance, collection, and metadata
  - Experimental design includes four conditions in both hydroponic and soil matrices: earthworms present/absent and plants present/absent.
  - Two systems used: hydroponic solution (with Sinapis alba) and soil (sandy loam Eutric Cambisol) with multiple replicates.
  - Detailed sample preparation and purification protocols:
    - Soil: 24-hour extraction with 15:4:1 methanol:water:formic acid; four time points tested; 24 h chosen to minimize degradation; internal standards added for each experiment.
    - Hydroponics: straightforward extraction; internal standards added for calibration.
  - Cleanup and separation:
    - Solid phase extraction using MCX cartridges, yielding three fractions (acidic compounds; cytokinin ribosides; cytokinin bases); Fraction 2 archived for future use.
  - Instrumentation and analysis:
    - Identification by FT-ICR-MS for accurate mass and empirical formula determination.
    - Quantification by MRM on a TSQ Endura triple quadrupole with LC separation, using isotopically labelled internal standards.
    - HPLC separation on a 2.6 μm C18 core-shell column with specified gradient timings.
  - Molecular biology data:
    - Primer design guided by Brassica napus genes; qPCR used to quantify ABA synthesis genes (NCED3, NCED5) and abiotic-stress genes (CIPK6, NHX1, RD29A); normalization to AtActin7; ΔΔCt method used for fold-change calculations.
    - In silico validation against earthworm genomes to confirm primer specificity; exploration of potential phytohormone biosynthesis genes in earthworms.

- Data quality, standards, and validation
  - Internal standards (isotopically labelled phytohormones) integrated for every analysis to enable accurate quantification and standardization across runs.
  - Calibration and method optimization performed to establish precursor–product transitions for MRM; explicit collision energy settings provided.
  - Quality controls include repeated extraction time-point testing, assessment of potential degradation (IAA noted to decay during extraction), and reporting of limits of detection (LOD) in supplementary data.
  - Data processing tools noted (Compass Data Analysis for FT-ICR-MS processing; TSQ Endura for MRM; HPLC with specified parameters).

- Data lifecycle and processing workflow
  - Sample handling and extraction are meticulously documented to enable reproducibility and re-use.
  - Data integration includes linking phytohormone concentrations (soil and hydroponic), FDH activity, plant biomass, pH, and molecular data to understand system-wide responses.
  - Supplementary information (Tables S5–S6) provides primer sequences and gene targets; additional tables (Tables 1–4) document concentrations, biomasses, FDH activity, and pH results.

- Data analysis and interpretation
  - Statistical design includes two-way ANOVA to analyze effects of plants and earthworms, with Holm-Sidak post hoc tests for interactions where appropriate; normality checks guide method choice.
  - Recognizes non-normal distribution in hydroponic phytohormone data but treats data with ANOVA due to robustness for interaction effects.
  - Molecular results summarized via qPCR using ΔΔCt for relative expression, normalized to an internal control gene.

- Data products, outputs, and reuse
  - Quantified phytohormone concentrations (IAA, ABA, zeatin, iP, Ade) with internal-standard calibration data; FDH activity measurements; plant biomass (fresh/dry) and hydroponic pH values.
  - Molecular data include expression levels for ABA biosynthesis and stress-responsive genes, enabling cross-study comparisons of ABA-related responses.
  - Data are prepared for reuse in broader data ecosystems through the EIDC catalogue, supporting cross-partner data sharing and secondary analyses.

- Challenges, limitations, and lessons for data strategy
  - Complexity of soil matrix necessitated rigorous cleanup and multiple extraction steps; a potential source of variability requiring thorough documentation for reproducibility.
  - IAA decay during extraction highlighted the need for robust handling and transparency about detection limits and data treatment (detected/undetected categories).
  - Primer validation across species (plant and invertebrate genomes) underscores the importance of provenance and cross-species checks in data products and analyses.
  - The study integrates multi-modal data (chemical, biological, molecular) requiring careful metadata management to enable effective cross-domain queries and reuse.

- Relevance to Data Leaders
  - Demonstrates end-to-end data governance: from experimental design and data collection to processing, analysis, and sharing via a data catalogue.
  - Highlights the importance of standardized workflows, internal standards, and detailed metadata to ensure data quality and interoperability across partners and studies.
  - Emphasizes data availability and reproducibility, with explicit references to data archives (EIDC) and supplementary materials for transparency.
  - Provides a model for cross-domain data integration (chemistry, biology, molecular biology) in environmental and plant-science research, aligning with data-system thinking and community data sharing goals.