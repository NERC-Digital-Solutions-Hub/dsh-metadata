# Overview of the data being described

- Purpose and scope
  - Provides a comprehensive dataset from physiology and RNA-seq experiments to identify genes with expression changes in Drosophila melanogaster after exposure to the parasitoid wasp Leptopilina boulardi.
  - Combines gene expression data with functional enrichment and multiple phenotype datasets to enable correlation of transcriptional responses with phenotypic outcomes.

- Experimental design and sampling
  - Population: outbred D. melanogaster established from a 372 isofemale wild-ccaught population from Cambridgeshire, UK (October 2017).
  - Treatments (four biological replicates per group; three treatments total): 
    - Wasp homogenate (20 female L. boulardi homogenised in 200 μl paraffin)
    - Paraffin only (oil)
    - Untouched control
  - Tissues and sampling:
    - 24 hours post manipulation, hemocytes pooled from 100 larvae; fat bodies dissected from 8 third instar larvae.
  - Conditions: flies maintained at 25°C; injections performed at room temperature.

- Sequencing and data processing
  - RNA sequencing: 50 bp single-end reads on a single lane of HiSeq4000 (Cancer Research UK Cambridge Institute, June 2019).
  - Read processing: Trimmomatic to trim bases with quality < 20 (4 bp sliding window).
  - Alignment: mapped to D. melanogaster reference (r6.28, Flybase) using STAR.
  - Read counting: featureCounts; minimum mapping quality 10.
  - Filtering: genes with at least 10 mapped reads across the 12 libraries per tissue.
  - Normalization: TMM (trimmed mean of M-values).
  - Tissue-specific filtering: remove fat-body genes enriched in salivary glands and male germ cells using FlyAtlas2.
  - Differential expression: edgeR and limma; FDR-adjusted P-value < 0.05 deemed significant.
  - Enrichment analyses: GO enrichment and pathways (Flymine); redundancy reduced with REVIGO.

- Key findings (datasets produced)
  - Hemocytes show broad transcriptional changes: 2,156 upregulated and 1,731 downregulated genes in wasp homogenate vs control.
  - Fat body shows a smaller, specific set: 29 upregulated genes enriched in wasp homogenate vs control.
  - Enrichment results:
    - Fat body: GO/Pathways/Interpro enriched categories for upregulated genes (Flymine-derived) with significance P < 0.05; REVIGO used to refine results.
    - Hemocytes: GO/Pathways/Interpro enriched categories for both up- and downregulated genes; redundancy reduced with REVIGO.
  - Data filtering and analysis outputs:
    - 'detected_genes' list used for downstream differential expression and enrichment analyses.
    - 'differentially_expressed_genes' contains DE results with Tissue, Comparison, FB_ID, logFC, AveExpr, t, PValue, adj.P.Val, and B (log-odds).
    - 'Wasp_specific-Venn' identifies genes unique to wasp homogenate vs control (not differentially expressed in oil vs control).
    - 'Wasp_and_Injury-Venn' identifies genes common to both wasp homogenate vs control and oil vs control comparisons, with logFC values and expression estimates.
  - Additional datasets (phenotypes and confirmations):
    - Oil_Melanization_Phenotype_Characterization: counts of larvae melanizing an injected paraffin oil droplet across five treatments.
    - Oil_Injection_Insect_Species_Phenotypes_V3: melanization counts across 44 insect species (including D. melanogaster, several drosophilids, and wasp-derived/other species).
    - Fat_body_qPCR_Confirmation: Ct values for 11 target genes under oil, oil+wasp, and unchallenged conditions.
    - ProteinaseK_Treatment_post_autoclave_2021_05: melanization counts across four conditions involving wasp homogenate variants and treatments (autoclaved vs non-autoclaved, PK-treated, etc.).

- Data structure and accessibility
  - Total of 13 data tables:
    - One tab-delimited file: read_count_mq10 (gene-level read counts per sample; columns include Geneid, Chr, Start, End, Strand, Length, followed by 24 sample columns).
    - Twelve comma-separated CSV files:
      - Library_details: sample metadata and library preparation conditions.
      - Mapping_metrics.csv: STAR-derived mapping quality metrics per sample.
      - Fatbody_GO: enriched GO terms, pathways, and Interpro terms for fat body upregulated genes.
      - Hemocytes_GO: enriched GO terms, pathways, and Interpro terms for hemocyte DE genes (up/downregulated).
      - detected_genes: genes detected after filtering for both tissues.
      - differentially_expressed_genes: DE gene list with detailed statistics.
      - Wasp_specific-Venn: DE genes unique to wasp homogenate vs control.
      - Wasp_and_Injury-Venn: DE genes shared between wasp homogenate and oil vs control.
      - Oil_Melanization_Phenotype_Characterization: phenotypic counts for oil-related treatments.
      - Oil_Injection_Insect_Species_Phenotypes_V3: species-level melanization phenotypes.
      - Fat_body_qPCR_Confirmation: qPCR Ct values for 11 genes.
      - ProteinaseK_Treatment_post_autoclave_2021_05: melanization phenotype data under various treatments.
  - Data accessibility emphasis: datasets organized with clear metadata and functional annotations to support discoverability and reuse.

- Relevance and use for analysts
  - Enables identification of tissue-specific transcriptional responses to parasitoid exposure and disentangling effects of parasitoid-derived cues vs. injury.
  - Supports replication and meta-analysis through standardized workflows (Trimmomatic, STAR, featureCounts, edgeR/limma, Flymine, REVIGO).
  - Provides integrated datasets linking gene-level expression with functional enrichment and phenotypic outcomes (melanization assays across treatments and species).
  - Offers a rich resource for cross-study comparisons in host-parasite interactions, immune responses, and evolutionary genetics.

- Key considerations and potential limitations
  - Single-end 50 bp sequencing may limit certain analyses (e.g., isoform resolution) compared to paired-end data.
  - Pooling of hemocytes (100 larvae) and limited fat body sampling (8 larvae) may influence variability and detection power.
  - Tissue-specific filtering to remove fat body genes enriched in salivary glands and male germ cells relies on external expression atlases (FlyAtlas2) and may affect gene inclusion.
  - Timepoint is fixed at 24 hours post-treatment; results reflect this specific window and may differ at other times.

- Overall takeaway
  - The dataset provides a comprehensive, multi-layered view of D. melanogaster responses to wasp exposure, combining robust differential expression analysis with functional enrichment and diverse phenotypic assays, suitable for data-driven hypothesis testing and cross-dataset integration in host-parasite research.