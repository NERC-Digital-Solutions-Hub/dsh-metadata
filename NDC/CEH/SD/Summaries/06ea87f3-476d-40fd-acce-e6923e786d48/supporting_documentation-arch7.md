# Overview of the data being described

## Study design and samples
- Data come from physiology and RNA-seq experiments aimed at identifying genes changing expression in Drosophila melanogaster after exposure to the parasitoid wasp Leptopilina boulardi.
- Population: outbred D. melanogaster established from a 372 isofemale wild-ccaught line from Cambridgeshire, UK, in Oct 2017.
- Treatments (late second/early third instar larvae): four groups injected with wasp homogenate (40? 20 female L. boulardi homogenised in 200 μl paraffin), four groups injected with paraffin-only (oil), and four untreated controls.
- Timepoint: 24 hours post manipulation.
- Tissues analyzed: hemocytes and fat body.
- Sampling: RNA extracted from both tissues; 100 larvae pooled for hemocytes and 8 larvae for fat body per sample.
- Conditions/temperature: flies maintained at 25°C; injections at room temperature.
- Sequencing: 50 bp single-end reads on HiSeq4000 (Cancer Research UK Cambridge Institute, June 2019).

## Data generation and processing
- Read processing: Trimmomatic used to trim bases with quality below 20 in 4 bp windows.
- Alignment: reads mapped to D. melanogaster reference (r6.28, Flybase) using STAR; mapped reads with MAPQ ≥ 10 retained.
- Counting: featureCounts used to obtain gene-level counts.
- Filtering and normalization: genes with at least 10 mapped reads across the 12 libraries per tissue; counts normalized with trimmed mean of M-values (TMM).
- Tissue-specific filtering: for fat body, removed genes enriched in salivary glands and male germ cells using FlyAtlas2 data.
- Differential expression: edgeR and limma used; significant genes at FDR-adjusted P < 0.05.
- Enrichment analyses: GO enrichment performed, results refined with REVIGO.

## Datasets and file structure
- Total data: 13 tables (one .txt and twelve .csv).
- Read counts: read_count_mq10.txt — tab-separated; contains gene-level counts for the 24 samples (12 libraries per tissue) with gene metadata (Geneid, Chr, Start, End, Strand, Length) followed by sample columns.
- Library metadata: Library_details.csv — sample identifiers, Tissue, Treatment, plus library preparation parameters.
- Mapping metrics: Mapping_metrics.csv — STAR-derived quality and mapping metrics per sample (Tissue, Treatment, Library_name, Library_ID, Sample_name, Fastq file size plus 19 mapping metrics).
- Fat body enriched terms: Fatbody_GO.csv — significantly enriched GO/KEGG/InterPro terms for 29 upregulated fat-body genes; includes database, term, ontology, ID, P-value, and enriched gene list.
- Hemocyte enrichments: Hemocytes_GO.csv — GO/Pathway/InterPro enrichments for 2,156 upregulated and 1,731 downregulated hemocyte genes; includes trend, database, term, ontology, ID, P-value, enriched gene list, and GO category metrics.
- Detected genes: detected_genes.csv — genes detected in both tissues after filtering low read support and tissue-specific cross-filtering.
- Differential expression: differentially_expressed_genes.csv — DE genes by tissue and comparison; columns include FB_ID, logFC, AveExpr, t-statistic, PValue, adj.P.Val, and B (log-odds).
- Venn analyses: Wasp_specific-Venn.csv (genes unique to wasp homogenate vs control) and Wasp_and_Injury-Venn.csv (genes common or differentially expressed in both comparisons).
- Phenotype data: Oil_Melanization_Phenotype_Characterization.csv and Oil_Injection_Insect_Species_Phenotypes_V3.csv — counts of D. melanogaster larvae melanizing injected paraffin oil droplets under various treatment conditions and across 44 insect species, respectively.
- Validation data: Fat_body_qPCR_Confirmation.csv — Ct values for 11 target genes across treatments (oil, oil+wasp homogenate, unchallenged).
- Treatment controls: ProteinaseK_Treatment_post_autoclave_2021_05.csv — melanization counts under combinations of wasp homogenate treatments (non-autoclaved/autoclaved, with/without proteinase K).

## Key analyses and outputs
- Tissue- and treatment-specific differential expression: significant DE genes identified per tissue under wasp homogenate vs control and related comparisons.
- GO and pathway enrichment: functional categories enriched among upregulated/downregulated gene sets, with redundancies reduced by REVIGO.
- Data provenance and reproducibility: clearly documented sample metadata, sequencing platform, processing steps, normalization, and statistical criteria (e.g., FDR thresholds).

## Quality, standards, and limitations
- Data include a mix of sequencing, mapping, expression, and functional enrichment metrics, with explicit filtering criteria (minimum counts, MAPQ thresholds, FDR cutoff).
- Fat body gene filtering removes genes with tissue-specific expression to reduce confounding signals.
- Single-end 50 bp reads may limit some analyses compared with paired-end data, but standard for the reported workflow.
- All data are organized into a consistent set of 13 tables, facilitating integrative analyses across tissues, treatments, and downstream functional interpretation.

## Reproducibility and provenance
- Sample origin, experimental conditions, library preparation details, sequencing platform, and analysis pipelines are thoroughly described.
- Data are structured to allow re-analysis of differential expression and enrichment, with explicit gene identifiers (FlyBase IDs) and sample annotations.

## GIS-focused notes and potential data products
- Although the dataset is not spatially geolocated, GIS specialists can:
  - Integrate experimental metadata (population origin, treatment, tissue) with map-based dashboards to document study design spatially alongside results.
  - Create multi-layer visualizations of tissue- and treatment-specific expression patterns mapped to functional categories or GO terms.
  - Link gene-level results to anatomical gene-expression atlases and reference maps of Drosophila tissues to produce spatially informed data products.
  - Develop provenance-aware data catalogs that track sample origin, experimental conditions, and analytic steps for geospatial data governance.