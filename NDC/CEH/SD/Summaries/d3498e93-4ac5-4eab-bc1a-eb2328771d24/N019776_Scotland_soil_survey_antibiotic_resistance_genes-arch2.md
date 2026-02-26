# Antibiotic resistance genes found in soils across the entire Scottish landscape

## Overview
- A dataset compiling the relative abundance of nearly 300 antimicrobial resistance (AMR) genes found in soils across Scotland.
- Based on soils from the National Soils Inventory of Scotland (NSIS2); 183 locations on a 20 km grid, sampled 2006–2009.
- Includes AMR genes across major antibiotic classes and resistance mechanisms (e.g., aminoglycosides, beta-lactams, fluoroquinolones, MLSB, tetracycline, vancomycin, sulphonamide, efflux pumps, integron genes).

## Data scope and units
- Units: relative gene abundances (gene copies per total bacteria), calculated using ΔΔCT from qPCR and normalized to 16S rRNA levels.
- Provides a surrogate measure of total bacterial abundance for normalization.
- Data cover a broad spatial extent across Scotland, enabling landscape-scale assessment of AMR gene distribution in soils.

## Fieldwork and analytical methods
- Field source: NSIS2 soil sampling coordinated by the James Hutton Institute; detailed protocols available via NSIS and related publications.
- DNA preparation: total community DNA extracted from soils using a modified CTAB method; DNA stored at -80°C.
- High-throughput analysis: 500–2000 ng DNA freeze-dried and submitted to Institute of Urban Environment, Chinese Academy of Sciences (Xiamen) for qPCR analysis using the OpenArray platform.
- Primers and targets: qPCR assays designed with established primers; Ct detection limit set at 37.
- Data processing: relative abundances calculated via the Livak (2^-ΔΔCT) method, using 16S rRNA as the normalizing standard.

## Data structure and content
- Core dataset columns include:
  - 16S rRNA levels
  - ARDB gene identifiers and names
  - Antibiotic/classification mappings (e.g., aminoglycoside, beta-lactam, MLSB, Multidrug, etc.)
- Extensive table linking ARDB gene entries to their antibiotic class and nomenclature, enabling standardized interpretation of gene abundances.
- Includes a wide range of resistance determinants (e.g., bla-type beta-lactamases, tet genes, erm genes, sul genes, qac efflux determinants, vancomycin-associated genes, integrases, transposases, and more).

## Provenance and collaboration
- Dataset developed 2016–2018 by Charles Knapp (University of Strathclyde) in collaboration with:
  - James Hutton Institute
  - Institute of Urban Environment, Chinese Academy of Sciences
  - Newcastle University
- Supported by the NERC AMR in the Real World grant NE/N019776/1.
- Fieldwork and analytical workflows reference established NSIS2 sampling protocols and published methods (e.g., Zhu et al. 2013; Looft et al. 2012; Livak & Schmittgen 2001).

## Relevance for environmental monitoring
- Demonstrates a scalable approach to monitor AMR gene content in soils over large landscapes.
- Standardized methods (DNA extraction, OpenArray qPCR, normalization to 16S) support comparability over time and across regions.
- Data can underpin environmental health indicators and policy performance related to AMR in terrestrial ecosystems.

## Data quality, accessibility, and reuse
- Quality assured through collaboration with established institutions and adherence to validated protocols.
- Data are structured for integration with other environmental datasets (e.g., land use, soil type, farming practices) to enhance interpretability and policy relevance.
- The dataset emphasizes underlying data accessibility and transparency, aligning with monitoring objectives to enable reuse by researchers and policymakers.

## Considerations and limitations
- Relative abundances reflect gene copy number per total bacteria, not absolute concentrations.
- Ct threshold (37) defines detection limits; low-abundance genes may be near detection limits.
- Cross-lab comparability requires careful methodological alignment if integrated with other datasets or time points.