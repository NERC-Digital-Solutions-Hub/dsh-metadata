# Overview of the data being described

- Context: RNA-seq and physiology experiments in Drosophila melanogaster to identify genes changing expression after exposure to parasitoid wasp Leptopilina boulardi. An outbred population from Cambridgeshire (2017) was used; samples collected from fat body and hemocytes after treatment.
- Experimental design:
  - Treatments: wasp homogenate (L. boulardi), oil (paraffin), and untreated control.
  - Replicates: four groups per treatment; total 12 libraries per tissue (hemocytes and fat body).
  - Sampling: 24 hours post manipulation, hemocytes pooled from 100 larvae; fat bodies dissected from 8 third-instar larvae.
  - Sequencing: 50 bp single-end reads on HiSeq4000 (June 2019).
- Data processing pipeline:
  - Read trimming with Trimmomatic (quality < 20 in 4 bp windows).
  - Mapping to D. melanogaster reference (r6.28) via STAR; mapping quality filter (MAPQ ≥ 10).
  - Gene counting with featureCounts.
  - Gene filtering: exclude fat body genes enriched in salivary glands/male germ cells using FlyAtlas2.
  - Differential expression: edgeR and limma; significance threshold FDR-adjusted P < 0.05.
  - Functional analysis: GO enrichment with FlyMine; results simplified with REVIGO.
- Data organization: dataset comprises 13 files (one text file and twelve CSV files) detailing read counts, metadata, quality metrics, differential expression, and functional enrichment, plus phenotype data from related assays.

## Data files included

- read_count_mq10.txt
  - Tab-delimited file with gene-level read counts (first columns: Geneid, Chr, Start, End, Strand, Length) and 24 sample columns; output from featureCounts.

- Library_details.csv
  - Sample metadata for RNA-seq library preparation: library_ID, Tissue, Treatment (3 factors) and six library preparation condition columns.

- Mapping_metrics.csv
  - STAR mapping metrics for 12 hemocyte and 12 fat body samples; includes Tissue, Treatment, Library_name, Library_ID, Sample_name, Fastq file size plus 19 additional mapping metrics.

- Fatbody_GO.csv
  - Significantly enriched GO terms, KEGG/Reactome, and InterPro terms among 29 fat body genes upregulated by wasp homogenate vs control; columns include Enrichment Database, Term, Ontology, ID, P-value, Enriched Gene.

- Hemocytes_GO.csv
  - GO/Pathway/InterPro enrichments for 2,156 upregulated and 1,731 downregulated genes in hemocytes; includes Trend (up/down), Enrichment Database, Term, Ontology, ID, P-value, Enriched Gene, plus three columns assessing uniqueness/dispensability for GO categories.

- detected_genes.csv
  - Genes detected in both tissues after filtering (low read support, poor alignment, and fat-body genes expressed in male germ cells/salivary glands).

- differentially_expressed_genes.csv
  - DE gene table for each comparison; columns include Tissue, Comparison, FB_ID, logFC, AveExpr, t, PValue, adj.P.Val, and B (log-odds of differential expression).

- Wasp_specific-Venn.csv
  - Genes unique to the wasp homogenate vs control comparison (not differentially expressed in oil vs control); includes FB_ID, logFC, Trend, and expression estimates (counts per million) per sample.

- Wasp_and_Injury-Venn.csv
  - Genes common to both wasp homogenate and oil comparisons; includes FB_ID, logFC_Wasp, logFC_Oil, Trend, and sample expression estimates.

- Oil_Melanization_Phenotype_Characterization.csv
  - Counts of D. melanogaster larvae melanizing an injected paraffin oil droplet across five treatments (oil, oil + wasp infection, oil + wasp homogenate, oil + male homogenate, oil + fly homogenate).

- Oil_Injection_Insect_Species_Phenotypes_V3.csv
  - Melanization counts for larvae injected with oil plus homogenates from 44 insect species (including Drosophilid species, specific strains, and Cambridge-collected specimens).

- Fat_body_qPCR_Confirmation.csv
  - Ct values for 11 target genes from qPCR across oil, oil + wasp homogenate, and unchallenged conditions (24 h prior extraction).

- ProteinaseK_Treatment_post_autoclave_2021_05.csv
  - Melanization counts for oil-injected droplets across four treatments: wasp homogenate non-autoclaved, wasp homogenate autoclaved, with/without proteinase K treatment.

## How the data can be used

- Cross-tissue and cross-condition analyses:
  - Compare transcriptional responses between fat body and hemocytes to identify tissue-specific vs shared responses to wasp exposure.
  - Integrate differential expression results with GO/Pathway enrichments to interpret functional themes (immune response, metabolism, signaling).
- Data integration and quality control:
  - Use read counts (read_count_mq10) with mapping metrics (Mapping_metrics.csv) to assess data quality and normalize appropriately.
  - Leverage detected_genes and filtering steps to reproduce or extend the differential expression analyses.
- Downstream applications for the Data Support archetype:
  - Build self-serve dashboards showing top DE genes by tissue and treatment, with associated GO terms and pathways.
  - Create reproducible pipelines that reproduce edgeR/limma results and link to enrichment outputs (Fatbody_GO, Hemocytes_GO).
  - Provide datasets for meta-analysis with related phenotypic assays (melanization phenotypes) to explore genotype-phenotype associations across treatments and species.
- Considerations:
  - Data originate from a controlled lab setup with three treatments and four replicates per treatment; ensure careful handling of batch effects and tissue-specific expression when combining data.
  - Different data types (RNA-seq, qPCR, phenotypic assays) are included, enabling multi-modal data products and cross-validation of gene expression results.