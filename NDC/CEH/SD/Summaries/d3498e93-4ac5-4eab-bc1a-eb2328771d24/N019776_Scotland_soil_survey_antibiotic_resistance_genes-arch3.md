# Antibiotic resistance genes found in soils across the entire Scottish landscape

- Purpose: A dataset collating the relative abundance of nearly 300 antimicrobial resistance (AMR) genes in soils across Scotland to assess AMR gene content at landscape scale.

- Provenance and collaboration:
  - Field sampling from the National Soils Inventory of Scotland (NSIS2), with NSIS2 sampling conducted 2006–2009.
  - Collaboration among Charles Knapp (University of Strathclyde), James Hutton Institute, Institute of Urban Environment (Chinese Academy of Sciences), and Newcastle University.
  - Supported under the NERC AMR in the Real World grant (NE/N019776/1).

- Sampling design and fieldwork:
  - 183 soil locations representing intersections of a 20 km grid across Scotland.
  - Soils were collected from NSIS2 sites; total sampling activity managed by the James Hutton Institute.

- Analytical methods:
  - DNA extraction from soils using a modified CTAB method; DNA stored at -80°C.
  - High-throughput AMR gene analysis: 500–2000 ng DNA per sample, freeze-dried and sent to Institute of Urban Environment (CAS, Xiamen, China).
  - Quantitative PCR performed on the Applied Biosystems OpenArray platform using pre-designed primers.
  - Detection limit set at cycle threshold (Ct) of 37.

- Nature of recorded units:
  - Results reported as relative gene abundances (gene copies per total bacteria), derived using the ΔΔCt method.
  - 16S rRNA quantified to provide a surrogate measure of total bacterial abundance.

- Data structure and content:
  - Main dataset organized with comprehensive table mappings between ARDB (Antibiotic Resistance Genes Database) entries and observed gene abundances.
  - Columns include 16S rRNA, ARDB gene, Antibiotic Classification, and extensive ARDB gene-specific entries (e.g., various aac, aad, bla, tet, erm, van, and many others with multiple name variants and classifications).
  - Includes entries for beta-lactamases, aminoglycoside resistance genes, tetracycline resistance genes, MLSB group genes, vancomycin resistance genes, efflux pumps, integrons, transposases, and other resistance determinants.
  - Table references and gene classifications follow established nomenclatures (ARDB) and include cross-references to multiple aliases for many genes.

- Data provenance, quality, and governance:
  - Provenance documented through collaboration and NSIS2 lineage; data produced under a defined grant with explicit field, extraction, and analytical workflows.
  - Methodological transparency via detailed description of sample processing, DNA extraction, qPCR setup, and detection thresholds.
  - Data structure designed to enable verification and reuse, with clear linkage between gene identifiers and antibiotic classes.

- Usage notes and considerations for monitoring frameworks:
  - Relative abundances depend on the ΔΔCt approach; comparisons require consistent reference baselines (total bacteria via 16S rRNA).
  - Metadata completeness is crucial for re-use; the dataset provides extensive methodological metadata and provenance to support data governance and openness.
  - The OpenArray-based approach offers high-throughput, replicate-rich measurements suitable for landscape-scale monitoring of AMR gene distribution in soils.
  - Potential applications include informing policy decisions on soil AMR risk, tracking spatial patterns, and guiding future data collection to fill gaps in metadata or underrepresented areas.

- References:
  - Lilly A, Bell JS, Hudson G, Nolan AJ, Towers W. 2011. National Soil Inventory of Scotland 2007-2009: Profile description and soil sampling protocols. NSIS_2 Technical Bulletin, James Hutton Institute.
  - Livak KJ, Schmittgen TD. 2001. Analysis of relative gene expression data using real-time qPCR and the 2(-ΔΔC(T)) method. Methods.
  - Liu B, Pop M. 2009. ARDB - Antibiotic Resistance Genes Database.
  - Looft T, et al. 2012. In-feed antibiotic effects on the swine intestinal microbiome.
  - Zhu Y-G, et al. 2013. Diverse and abundant antibiotic resistance genes in Chinese swine farms.