# Antibiotic resistance genes found in soils across the entire Scottish landscape

## Summary
- A dataset of the relative abundance of nearly 300 antimicrobial resistance (AMR) genes found in soils across Scotland.
- Based on DNA extracted from soils collected under the National Soils Inventory of Scotland (NSIS2) sampling program.
- NSIS2 sampling occurred from 2006 to 2009 at 183 locations arranged on a 20 km grid across Scotland.
- AMR genes span major antibiotic classes (e.g., aminoglycosides, beta-lactams, fluoroquinolones, MLSB, tetracyclines, vancomycin, sulphonamides) and include many resistance traits (e.g., efflux pumps, integrons).
- Results are presented as relative gene abundances (genes per total bacteria), using 16S rRNA levels to estimate total bacterial abundance.

## Provenance and quality
- Dataset developed by Charles Knapp (University of Strathclyde) during 2016–2018.
- Collaborative contributions from James Hutton Institute, Institute of Urban Environment (Chinese Academy of Sciences), and Newcastle University.
- Supported under the NERC AMR in the Real World grant NE/N019776/1.
- Data are a collated product of NSIS2 field sampling and subsequent high-throughput molecular analysis.

## Fieldwork
- Based on soils from the NSIS2 collection effort, maintained by the James Hutton Institute.
- NSIS2 profile descriptions and soil sampling protocols referenced for context and replicability (Lilly et al. 2011; NSIS infrastructure link).

## Analytical methods
- DNA extracted from soils using a modified CTAB method; DNA stored at -80°C.
- 500–2000 ng of DNA freeze-dried and sent to the Institute of Urban Environment, CAS (Xiamen) for high-throughput analysis.
- Quantitative PCR performed on the Applied Biosystems OpenArray platform using pre-designed primers (from Zhu et al. 2013; Looft et al. 2012).
- Detection threshold set at Ct = 37.

## Nature of recorded units
- Recorded units are relative gene abundances calculated by the ΔΔCt method (Livak & Schmittgen, 2001).
- 16S rRNA levels quantified to provide a surrogate measure of total bacterial abundance.

## Details of data structure
- Primary data columns include a comprehensive table of high-throughput qPCR assays and their ARDB (Antibiotic Resistance Genes Database) mappings, with corresponding antibiotic classifications.
- Data structure links each AMR gene (ARDB gene name) to its antibiotic class and provides the measured relative abundance.
- The ARDB mapping table includes thousands of gene entries across multiple resistance categories (e.g., aminoglycoside, beta-lactamase, MLSB, tetracycline, vancomycin, multidrug, etc.).

## References
- Lilly A, Bell JS, Hudson G, Nolan AJ, Towers W. 2011. National Soil Inventory of Scotland 2007-2009: Profile description and soil sampling protocols. NSIS_2 Technical Bulletin, James Hutton Institute.
- Livak KJ, Schmittgen TD. 2001. Analysis of relative gene expression data using real-time quantitative PCR and the 2(-DeltaDeltaC(T)) method. Methods 25(4): 402-408.
- Liu B, Pop M. 2009. ARDB - Antibiotic Resistance Genes Database. Nucleic Acids Research.
- Looft T, et al. 2012. In-feed antibiotic effects on the swine intestinal microbiome. PNAS.
- Zhu Y-G, et al. 2013. Diverse and abundant antibiotic resistance genes in Chinese swine farms. PNAS.