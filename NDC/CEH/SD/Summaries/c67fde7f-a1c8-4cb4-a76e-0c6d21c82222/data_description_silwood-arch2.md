# Wild rodents social networks and the microbiome

- Purpose and scope
  - Integrated dataset combining field trapping data, social network/space-use data from PIT-tag loggers, kinship/genotyping data, and gut microbiome profiles from wild wood mice.
  - Primary aim: study how social contacts influence gut microbiome transmission in a wild setting.

## Study site and field data collection

- Location and duration
  - 2.47 ha mixed woodland plot (Nash's Copse) at Imperial College Silwood Park, UK.
  - Field period: November 2014 to December 2015.
- Trapping and processing
  - Rodents trapped approximately fortnightly; multiple species captured (Apodemus sylvaticus, Apodemus flavicollis, Myodes glareolus, Sorex araneus).
  - Traps: 122 Sherman live traps baited with peanuts, apple, bedding; opened at dusk and collected at dawn.
  - Processing at first capture: species ID, sex, weight/age, PIT-tag insertion for permanent ID, ear punches for host genotyping.
  - Faecal samples collected within 8 hours of trapping, stored at -80°C for microbiome analysis.
  - Field hygiene: sterilization between captures; traps washed between sessions; continuous rotation design to ensure coverage.
- Social and space-use data collection
  - Nine custom-built PIT-tag loggers distributed across the trapping grid.
  - Loggers recorded presence of tagged individuals every 0.3 seconds; loggers rotated among fixed territorial plot regions to ensure even coverage.
  - Loggers rotated mostly 3.5 times per week; timing restricted to 10:00–14:00 to minimize nocturnal activity biases.
  - Rotation design: territories consisted of contiguous grid cells; precise logger position within a cell randomized during each rotation.
  - Data filtering: excluded data from nights with no trapping or limited logging; removed corrupt tag reads; after cleaning, data from 83 of 93 tagged mice were retained.
- Data products and visualization
  - Figures detailing logging area/territories, the logger device, and logging effort across grid cells accompany the data (not reproduced here).

## Kinship, genetics, and pedigree

- Genotyping
  - Ear tissue genotyped at eleven microsatellite loci (initial set of twelve with one discarded due to deviation from Hardy–Weinberg equilibrium).
  - Methods: DNA extraction, multiplex PCR, capillary sequencing, and genotype scoring with COLONY-friendly quality checks.
  - Quality metrics provided for each locus (allele counts, heterozygosity, Hardy–Weinberg deviations, null alleles, scoring error).
- Pedigree reconstruction
  - Pedigree inferred using COLONY 2.0, accounting for polygamy and potential inbreeding.
  - Conflicts with field data (age/temporal trapping) identified and resolved; 11 impossible mother-pup and 4 impossible father-pup pairs removed.
  - Resulting pedigree: 17 mother–pup, 14 father–pup, 13 full-sibling, and 26 half-sibling relationships.
  - Kinship matrices produced as dyadic distances (e.g., parent-offspring and full-siblings = 0.5; half-siblings = 0.125).

## Gut microbiota profiling and sequencing

- Sample collection and scope
  - 239 faecal samples from 75 individual wood mice (≈90% of monitored individuals), averages about 3.2 samples per mouse (range 1–9).
- Laboratory workflow
  - DNA extraction and PCR amplification of the ~240 bp V4 region of the 16S rRNA gene.
  - Rigorous controls: extraction controls, no-template controls, and mock community standards included to monitor contamination and accuracy.
  - Two-step, dual-indexing library preparation and 2x250 bp Illumina MiSeq sequencing.
- Bioinformatics and quality control
  - DADA2 pipeline used for sequence inference and ASV determination; trimming to remove primers/adapters and low-quality tails.
  - Taxonomy assigned with GreenGenes; a single low-quality sample removed.
  - Diversity and completeness assessments conducted with iNEXT; rarefaction curves indicated plateau around 2,500–4,000 reads.
  - Singleton ASVs removed; contaminant-like taxa (non-gut bacteria such as Cyanobacteria, certain Mitochondria/other orders) filtered out.
  - Data normalized to relative abundances within each sample.
- Outputs and interpretation
  - ASV table with taxonomic assignments and sample metadata.
  - Diversity metrics and sample completeness used to support robust comparisons across individuals and social network contexts.

## Data integration, quality assurance, and accessibility

- Data provenance and standardised processing
  - Data collected from multiple linked sources (field observations, logger-based social interactions, genetic relatedness, microbiome sequences) with clear provenance and processing steps.
  - Standard QA steps documented: controlled sampling batches, randomization, sequencing/analysis pipelines, and explicit data cleaning rules.
- Dataset structure and storage
  - Datasets include: silwood_rodent_trapping_data.csv, silwood_rodent_capture_data.csv, and silwood_logger_data.csv (as representative outputs).
  - Datasets are designed for integration across individuals (IDs, PIT-tags), spatial positioning (grid cells, logger territories), temporal data (dates, times, Julian dates), genetic relationships, and microbiome profiles.
- Reusability and access considerations
  - Data are structured to enable cross-domain analyses (ecology, behavioral networks, host–microbiome interactions, population genetics).
  - Emphasis on storing and linking underlying data to outputs, facilitating scrutiny of environmental health indicators and policy-relevant performance over time.

## Relevance to environmental monitoring and analysis

- Demonstrates how combined field monitoring, individual-level tracking, genetic relatedness, and microbiome profiling can reveal mechanisms of microbe transmission in wild populations.
- Provides a template for standardized, multi-source environmental data integration with robust QA and documentation for downstream policy and research use.
- Offers datasets suitable for exploring social network effects on microbial ecology, host movement and space-use, and population structure in environmental monitoring contexts.