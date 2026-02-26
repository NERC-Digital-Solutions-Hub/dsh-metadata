# Overview of the data being described

- Objective and scope
  - Describes data from physiology experiments and an RNA-seq experiment to identify genes changing expression in Drosophila melanogaster after exposure to the parasitoid wasp Leptopilina boulardi.
  - Focus on host immune and tissue-specific responses, comparing fat body and hemocytes.

- Biological material and experimental design
  - Outbred D. melanogaster population established from 372 isofemales wild-caught in Cambridgeshire, UK (October 2017).
  - Four treatment groups per experiment:
    - Wasp homogenate (20 female L. boulardi homogenised in 200 μl paraffin)
    - Paraffin/oil only (oil)
    - No manipulation (control)
  - Timepoint: 24 hours post-manipulation.
  - Tissues sampled: hemocytes pooled from 100 larvae; fat bodies dissected from 8 third instar larvae.
  - Conditions: 25°C for flies; injections at room temperature.
  - Sequencing: RNA-seq with 50 bp single-end reads on a HiSeq4000 (Cancer Research UK Cambridge Institute, June 2019).

- Data processing and analysis workflow
  - Quality control and trimming with Trimmomatic (Q < 20, 4 bp sliding window).
  - Read mapping to D. melanogaster reference (r6.28, Flybase) using STAR; reads with MAPQ ≥ 10 counted with featureCounts.
  - Filtering: genes with at least 10 mapped reads across 12 libraries per tissue; normalization with trimmed mean of M-values (TMM).
  - Tissue-specific filtering: remove fat body genes enriched in salivary glands and male germ cells using FlyAtlas2 data.
  - Differential expression testing: edgeR and limma; significant genes with FDR P-value < 0.05.
  - Functional analysis: Gene Ontology enrichment, followed by reduction with REVIGO.
  
- Data assets and file structure
  - The dataset comprises 13 tables/files (one .txt and twelve .csv):
    - read_count_mq10.txt: gene-level read counts following featureCounts; columns include Geneid, Chr, Start, End, Strand, Length, plus 24 sample columns.
    - Library_details.csv: sample metadata including library_ID, Tissue, Treatment, plus library preparation conditions.
    - Mapping_metrics.csv: mapping and quality metrics for 12 hemocyte and 12 fat body samples; includes sample identifiers and STAR-derived metrics.
    - Fatbody_GO.csv: significantly enriched GO terms, KEGG/Reactome pathways, and InterPro entries for 29 upregulated fat body genes (vs. control); columns include database, term, ontology, ID, P-value, Enriched Gene IDs.
    - Hemocytes_GO.csv: GO/Pathway/InterPro enrichments for 2,156 upregulated and 1,731 downregulated hemocyte genes; includes Trend, P-values, Enriched Gene IDs, and GO-specific columns.
    - detected_genes.csv: genes detected in both tissues after filtering for low read support and tissue-specific exclusions; used for downstream analyses.
    - differentially_expressed_genes.csv: differential expression results for each comparison; nine columns (Tissue, Comparison, FB_ID, logFC, AveExpr, t, PValue, adj.P.Val, B) plus interpretation fields.
    - Wasp_specific-Venn.csv: genes differentially expressed only in wasp homogenate vs control (not in oil vs control); includes FB_ID, logFC, Trend, and expression estimates.
    - Wasp_and_Injury-Venn.csv: genes differentially expressed in both wasp homogenate and oil vs control comparisons; includes logFC_Wasp, logFC_Oil, Trend, and expression estimates.
    - Oil_Melanization_Phenotype_Characterization.csv: melanization outcomes for larvae injected with paraffin oil across five treatments.
    - Oil_Injection_Insect_Species_Phenotypes_V3.csv: melanization outcomes for larvae with homogenates from 44 insect species (plus specific D. melanogaster-related controls); organism source details included.
    - Fat_body_qPCR_Confirmation.csv: Ct values for 11 target genes across oil, oil + wasp homogenate, and unchallenged conditions.
    - ProteinaseK_Treatment_post_autoclave_2021_05.csv: melanization outcomes under four treatments involving wasp homogenate conditions and enzyme treatment variations.
  
- Reproducibility, standards, and references
  - Genome reference: D. melanogaster r6.28 (Flybase).
  - Alignment and analysis tools: Trimmomatic, STAR, featureCounts, edgeR, limma, REVIGO; GO enrichment via Flymine.
  - Data organization adheres to a structured, multi-file dataset with explicit sample and tissue metadata to facilitate reuse and cross-study comparisons.

- Data quality, accessibility, and governance considerations
  - Clear quality filtering steps (read quality, mapping quality, expression thresholds) to ensure robust differential expression results.
  - Tissue-specific filtering to reduce confounding from non-target tissues.
  - GO and pathway enrichment data linked to the gene lists and differential expression results for interpretability.
  - Comprehensive metadata for library preparation, sample identity, and tissue type to support discoverability and replication.

- Potential uses for data leaders
  - Integrate with broader data ecosystems to monitor data quality and lineage across multi-tissue RNA-seq experiments.
  - Assess the completeness and consistency of metadata to enable co-ownership of data products and align with user needs (policy or partner analyses).
  - Leverage the structured differential expression and enrichment outputs to inform data cataloging, metadata standards, and future data collection planning.
  - Use the cross-tissue and cross-treatment design to inform governance around dataset expansion, reproducibility, and cross-study comparability.