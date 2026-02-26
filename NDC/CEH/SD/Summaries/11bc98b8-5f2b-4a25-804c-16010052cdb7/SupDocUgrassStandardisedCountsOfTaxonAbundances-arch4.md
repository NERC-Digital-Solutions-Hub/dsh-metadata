# U-GRASS (Understanding and enhancing soil ecosystem services and resilience in UK grass and croplands) UK grasslands:   Standardised   counts   of   bacteria,   fungi   and   micro eukaryotes   abundances   across   geo   linked   sampling   locations   on grassland, UK (2016)

- Executive summary
  - A dataset of standardised counts of taxon abundances for bacteria (16S), fungi (ITS), and microeukaryotes (18S) from soil samples.
  - Collected from 32 UK grassland sites with paired intensive/extensive management and contrasting low/high pH soils.
  - Sampling occurred in winter to spring 2015–2016; DNA was extracted and taxonomic marker genes were sequenced to assess microbial diversity and abundance.
  - Aimed to understand soil functional change under different management and climatic scenarios as part of the NERC U-GRASS Soil Security Programme.
  - Processing and deposition: field sampling and DNA work conducted at CEH; data exported as CSVs for deposition into the EIDC; associated with NERC grant NE/M017125/1.

- Data collection and study design
  - 32 grassland sites across the UK representing land-use contrasts (low vs. high intensity).
  - Soil cores (15x5 cm) collected along 100 m interfaces, every 25 m, yielding 5 paired samples per site.
  - Sampling window: Nov 2015–Feb 2016; samples stored at -20°C prior to analysis.

- Molecular methods
  - DNA extraction and quantification:
    - Extraction from 0.25 g field-moist soil using MoBio PowerSoil kit.
    - DNA quantified with Qubit fluorometer and Nanodrop.
  - Amplicon sequencing (Illumina MiSeq, V3 chemistry, 600 cycles):
    - 16S rRNA (bacteria) using Kozich et al. 2013 primers for V3–V4.
    - 18S rRNA (microeukaryotes) using Kozich et al. 2013 strategy with Baldwin et al. 2005 primers.
    - ITS (fungi) using Kozich et al. 2013 strategy with Ihrmark et al. 2012 primers (ITS2 region).
  - Bioinformatics:
    - Demultiplexing with Illumina Basespace; quality filtering, merging, and OTU clustering at 97% similarity.
    - Taxonomic assignment against GreenGenes (bacteria) and UNITE (fungi) with bootstrap threshold ≥ 0.8.
  - Diversity analysis:
    - R vegan package used to compute diversity metrics (Shannon, richness, evenness) after rarefaction.

- Data structure and files
  - UgrassStandardisedCountsOfTaxonAbundances.csv
    - 450 rows x 23 columns.
    - Key columns: latitude, longitude; Sample_ID_16S, Sample_ID_18S, Sample_ID_ITS; nanodrop and qubit DNA concentrations; Shannon’s index (sha_bac, sha_fun, sha_eu); richness and evenness metrics; richness at >1% and >0.001% abundance for bacteria, fungi, and microeukaryotes.
  - Taxonomy and Amplicon data files (per marker):
    - 16sTaxonomy.csv (33975 rows), 18sTaxonomy.csv (24110 rows), ItsTaxonomy.csv (35750 rows)
      - OTU_number with taxonomic assignments (kingdom to species) and bootstrap ≥ 0.8.
    - 16sAmpliconData.csv (33975 OTUs x samples), 18sAmpliconData.csv (24110 OTUs x samples), ItsAmpliconData.csv (35750 OTUs x samples)
      - Frequency tables of rarefied OTU counts; columns correspond to sample identifiers.
  - Associated outputs:
    - UgrassStandardisedCountsOfTaxonAbundances.csv (final cross-reference file for downstream analyses).
  - Data provenance:
    - Lab work conducted at CEH Wallingford and Rothamsted Research.
    - Sequences processed via in-house pipelines; data prepared for deposition into the EIDC.

- Data provenance, scope, and context
  - Project context: soil security, multifunctionality, and resilience under climate and land-use change; links to soil organic matter, carbon storage, nutrient cycling, and ecosystem services.
  - Research motivation: link soil biodiversity to functions and responses under different management across geographic contexts; evaluate how biodiversity components influence soil processes.
  - Collaboration and funding: NERC Soil Security Programme; project led by Griffiths, Puissant, Goodall; data prepared for public access via EIDC.

- Relevance for data leaders
  - Demonstrates end-to-end data lifecycle for a multi-omics soil microbiome study: field sampling, lab processing, sequencing, bioinformatics, and structured data packaging.
  - Provides a well-documented metadata schema (coordinates, sample IDs, sequencing metrics, diversity indices) enabling discoverability, interoperability, and reuse.
  - Multimodal data (counts, OTU tables, and taxonomy) supports cross-study integration and meta-analyses across networks.
  - Clear data lineage and provenance facilitate trust, reproducibility, and governance when sharing with partners and external communities.