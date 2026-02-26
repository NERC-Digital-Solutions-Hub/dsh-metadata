# Overview of the data being described

- Study organism and origin
  - Drosophila melanogaster outbred population established from 372 isofemale wild-caught flies from Cambridgeshire, UK, in October 2017
- Experimental design
  - Three treatments applied to late second/early third instar larvae:
    - Wasp homogenate: injections with 20 female Leptopilina boulardi homogenised in 200 μL paraffin
    - Oil control: injections with paraffin only
    - Control: no manipulation
  - Encapsulation rates measured for each treatment
  - 24 hours post manipulation, tissues collected: hemocytes from 100 larvae pooled; fat bodies from 8 third instar larvae
  - Maintenance conditions: 25°C; injections at room temperature
- RNA sequencing
  - RNA extracted from both tissues and subjected to 50 bp single-end sequencing
  - Sequencing platform: HiSeq4000, Cancer Research UK Cambridge Institute, June 2019

- Data generation and processing workflow
  - Read preprocessing: Trimmomatic, quality filter Q < 20 over 4 bp windows
  - Alignment: STAR to D. melanogaster reference r6.28 (Flybase)
  - Quantification: featureCounts with minimum mapping quality 10
  - Filtering: genes with fewer than 10 mapped reads across 12 libraries removed
  - Normalization: trimmed mean of M-values (TMM)
  - Tissue-specific filtering: fat body genes enriched in salivary glands or male germ cells removed using FlyAtlas2
  - Differential expression: edgeR and limma; FDR-adjusted P < 0.05 considered significant
  - Functional analysis: Gene Ontology (GO) enrichment using Flymine; redundancy reduced with REVIGO

- Data structure and files (13 tables total)
  - read_count_mq10.txt: gene-level read counts per sample after featureCounts; first columns contain gene metadata (Geneid, Chr, Start, End, Strand, Length); 24 sample columns follow
  - Library_details.csv: library_ID, Tissue, Treatment and six library preparation-related columns (RNA concentrations, PCR cycles)
  - Mapping_metrics.csv: mapping quality metrics for 12 hemocyte and 12 fat body samples; includes Tissue, Treatment, Library_name, Library_ID, Sample_name, Fastq file size and 19 STAR-derived metrics
  - Fatbody_GO.csv: enriched GO terms, KEGG/Reactome, and InterPro terms for 29 fat body upregulated genes (Flymine); columns include database, term, ontology, ID, P-value, enriched gene list
  - Hemocytes_GO.csv: enriched GO/Pathway terms for 2,156 upregulated and 1,731 downregulated genes in hemocytes; includes trend, database, term, ontology, ID, P-value, enriched genes, and uniqueness/dispensability indicators
  - detected_genes.csv: genes detected after filtering; used for differential expression and enrichment analyses
  - differentially_expressed_genes.csv: DE genes per tissue and comparison; columns include FB_ID, logFC, AveExpr, t, PValue, adj.P.Val, B, among others
  - Wasp_specific-Venn.csv: genes unique to wasp homogenate vs control; includes FB_ID, logFC, trend, and sample expression estimates
  - Wasp_and_Injury-Venn.csv: genes common to both wasp homogenate vs control and oil vs control comparisons; includes logFC_Wasp, logFC_Oil, trend, and sample expression estimates
  - Oil_Melanization_Phenotype_Characterization.csv: number of D. melanogaster larvae melanizing an injected paraffin oil droplet across five treatments
  - Oil_Injection_Insect_Species_Phenotypes_V3.csv: melanization data for larvae exposed to homogenates from 44 insect species (including lab-maintained Drosophilids and other species)
  - Fat_body_qPCR_Confirmation.csv: Ct values for 11 target genes across oil, oil+wasp homogenate, and unchallenged conditions
  - ProteinaseK_Treatment_post_autoclave_2021_05.csv: melanization data across four conditions involving wasp homogenate with/without autoclaving and Proteinase K treatment

- Notable analyses and outputs
  - Tissue- and treatment-specific differential expression results
  - GO/Pathway enrichment results with redundancy reduction
  - Venn analyses delineating genes unique to or shared between treatments
  - Phenotypic data tying molecular responses to melanization outcomes under various exposure conditions
  - qPCR confirmation and proteinase K/autoclave treatment effects as additional validation layers

- Relevance to environmental monitoring and data practices
  - Demonstrates a comprehensive, end-to-end data workflow suitable for environmental health monitoring: defined sampling, standardized sequencing and processing, rigorous QA/filtering, and clear data packaging
  - Uses standardized tools and methods (Trimmomatic, STAR, featureCounts, edgeR/limma, REVIGO) to enable reproducibility and comparability over time
  - Provides extensive metadata and multiple data layers (counts, mapping metrics, GO terms, differential expression, phenotypic assays), supporting data accessibility, reuse, and cross-study synthesis
  - Addresses data interoperability and value enhancement by organizing results into structured datasets for downstream analyses and cross-referencing with underlying data sources