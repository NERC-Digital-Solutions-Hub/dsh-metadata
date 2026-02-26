# Antibiotic resistance genes found in soils across the entire Scottish landscape

- Aim and scope
  - Dataset collates the relative concentration of nearly 300 antimicrobial resistance (AMR) genes found in soils across Scotland.
  - Provides a map-friendly view of AMR gene abundance relative to total bacterial content.

- Spatial extent and sampling design
  - Based on the National Soils Inventory of Scotland (NSIS2).
  - Sampling conducted 2006–2009 at 183 soil locations distributed across a 20 km grid covering all of Scotland.

- Fieldwork and data provenance
  - Developed by Charles Knapp (University of Strathclyde) (2016–2018), in collaboration with James Hutton Institute, Institute of Urban Environment (Chinese Academy of Sciences), and Newcastle University.
  - Part of the NERC AMR in the Real World grant (NE/N019776/1).

- Analytical methods
  - Community DNA extracted from soils using a modified CTAB method; DNA stored at -80°C.
  - High-throughput AMR gene analysis conducted by sending 500–2000 ng DNA to the Institute of Urban Environment (CAS, Xiamen, China).
  - Quantitative PCR performed on the Applied Biosystems OpenArray platform using curated primers.
  - Detection threshold set at threshold cycle (Ct) of 37.

- Nature of recorded units
  - Results are relative gene abundances derived from the ΔΔCt method.
  - 16S rRNA levels quantified to estimate total bacterial content.

- Data structure and content
  - Main dataset comprises high-throughput qPCR assay results with:
    - 16S rRNA and ARDB gene names
    - Corresponding antibiotic classifications (e.g., Aminoglycoside, Beta-Lactamase, MLSB, Multidrug, Tetracycline, etc.)
  - Comprehensive mapping between ARDB genes and antibiotic classes; extensive table listing genes such as aac variants, bla variants, erm variants, tet variants, and many others.
  - Includes multiple gene-level entries per sample, reflecting diverse resistance determinants.

- Data quality and standards
  - Data compiled under a defined project framework with cross-institution collaboration.
  - Normalization to total bacterial content via 16S rRNA provides comparability across samples.

- GIS relevance and usage notes
  - Enables spatial visualization of AMR gene abundances across Scotland.
  - Suitable for overlay with environmental variables (soils, land-use, climate) to explore drivers or patterns of AMR gene distribution.
  - Can be integrated with NSIS2 soil archive data for temporal or gradient analyses if additional sampling is available.

- References
  - Lilly A, Bell JS, Hudson G, Nolan AJ, Towers W. 2011. National Soil Inventory of Scotland 2007-2009: Profile description and soil sampling protocols.
  - Livak KJ, Schmittgen TD. 2001. Analysis of relative gene expression using real-time qPCR (2(-ΔΔCt) method).
  - Liu B, Pop M. 2009. ARDB - Antibiotic Resistance Genes Database.
  - Looft T, et al. 2012. In-feed antibiotic effects on swine microbiome.
  - Zhu Y-G, et al. 2013. Diverse AMR genes in Chinese swine farms.