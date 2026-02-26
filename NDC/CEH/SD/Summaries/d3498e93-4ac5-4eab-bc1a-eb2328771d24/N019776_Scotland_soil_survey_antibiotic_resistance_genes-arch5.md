# Antibiotic resistance genes found in soils across the entire Scottish landscape

## Overview
- Provides a landscape-scale dataset of relative abundances for nearly 300 antimicrobial resistance (AMR) genes in soils across Scotland.
- Based on DNA previously extracted from soils in the National Soils Inventory of Scotland (NSIS2); sampling occurred 2006–2009 at 183 locations on a 20 km grid.
- For each soil sample, AMR gene content across major antibiotic classes was assessed; results are expressed as relative gene abundances per total bacteria.

## Provenance and custodianship
- Developed by Charles Knapp (University of Strathclyde) with collaborators from James Hutton Institute, Institute of Urban Environment (Chinese Academy of Sciences), and Newcastle University.
- Data compiled under the NERC AMR in the Real World grant NE/N019776/1.
- Data custody involves multiple institutions with defined roles in field sampling, analytic processing, and data assembly.

## Fieldwork
- Draws from the NSIS2 soil sampling program managed by the James Hutton Institute.
- NSIS2 samples were collected across Scotland (183 sites) using a 20 km grid framework.
- Background protocols and site descriptions available via NSIS archives and Lilly et al. 2011.

## Analytical methods
- Community DNA extracted from soils using a modified CTAB method; stored at -80°C.
- 500–2000 ng of DNA sent to Institute of Urban Environment, CAS (Xiamen) for high-throughput AMR gene analysis.
- Quantitative PCR performed on the OpenArray platform using previously designed primers (Zhu 2013; Looft 2012).
- Detection threshold set at a cycle threshold (Ct) of 37.

## Units and data structure
- Results expressed as relative gene abundances derived from the ΔΔCt method (Livak & Schmittgen 2001).
- 16S rRNA gene quantified to provide a surrogate for total bacterial load.
- Data structure centers on high-throughput qPCR assays with corresponding ARDB (Antibiotic Resistance Genes Database) annotations and antibiotic classifications (e.g., aminoglycoside, beta-lactamase, MLSB, tetracycline, vancomycin, etc.).
- The dataset includes extensive, gene-by-gene mappings (ARDB gene name, antibiotic class, and class-specific labels), enabling detailed cross-referencing of detected AMR genes.

## Data quality and validation
- Methodology emphasizes standardized field sampling (NSIS2) and consistent laboratory protocols (CTAB DNA extraction, OpenArray qPCR, established primer sets).
- Provenance includes collaboration across multiple institutions, reinforcing methodological rigor.
- References to foundational work (NSIS sampling protocol, qPCR analysis methods) support reproducibility and traceability.

## Access, reuse, and governance
- Dataset is anchored to NSIS2 and associated institutions, with provenance and methods documented for future reuse.
- Clear documentation of analytical workflow and gene-class mappings facilitates secondary analyses and interoperability with AMR gene databases.
- Reuse should acknowledge the multidisciplinary collaboration and the NSIS2 framework; consult the cited references for methodological specifics.

## Limitations and caveats
- Abundances are relative, not absolute counts; interpretation should consider normalization to total bacterial load (via 16S rRNA) and the delta-delta Ct framework.
- Dependence on predefined primer sets and ARDB mappings; uncharacterized or novel AMR genes may be missed.
- Data reflect a historical sampling window (2006–2009) and may not capture recent shifts in AMR gene distributions without updated sampling.

## References
- Lilly A, Bell JS, Hudson G, Nolan AJ, Towers W. 2011. National Soil Inventory of Scotland 2007-2009: Profile description and soil sampling protocols. NSIS_2. James Hutton Institute.
- Livak KJ, Schmittgen TD. 2001. Analysis of relative gene expression data using real-time quantitative PCR and the 2(-Delta Delta C(T)) method. Methods.
- Liu B, Pop M. 2009. ARDB - Antibiotic Resistance Genes Database. Nucleic Acids Research.
- Looft T, et al. 2012. In-feed antibiotic effects on the swine intestinal microbiome. PNAS.
- Zhu Y-G, et al. 2013. Diverse and abundant antibiotic resistance genes in Chinese swine farms. PNAS.