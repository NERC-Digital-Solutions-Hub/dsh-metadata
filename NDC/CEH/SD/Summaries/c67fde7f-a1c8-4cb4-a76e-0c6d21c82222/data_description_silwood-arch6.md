# Wild rodents social networks and the microbiome

- An integrated dataset combining trapping records, social tracking, kinship, and gut microbiome profiles for wild wood mice at Silwood Park (Nov 2014–Dec 2015) to study how social contacts influence gut microbe transmission.
- Full data scope includes both target and non-target rodent species captured in a 2.47 ha woodland plot, with all associated field and laboratory processing details.

## Study design and data scope

- Field site: Nash's Copse, Silwood Park, UK; longitudinal rodent sampling within a fixed 2.47 ha area.
- Data types collected:
  - Field capture and trapping data (species, sex, age, mass, health indicators, trap details).
  - Social tracking data via custom PIT-tag loggers to infer proximity and contact networks.
  - Genetic relatedness data from ear tissue for kinship and pedigree reconstruction.
  - Gut microbiome data derived from fecal samples (16S rRNA gene V4 region sequencing).
- Data span: trapping and tracking across roughly one year; microbiome sampling across corresponding period.

## Field data collection and trapping

- Trapping: 122 Sherman traps, baited, set at dusk and collected at dawn; fortnightly to every 2–4 weeks.
- Processing: species identification, sexing, weight, age, PIT-tagging, ear punches for genotyping; fecal samples collected and stored for microbiome analysis.
- Handling and sanitation: sterilization of sampling equipment; traps washed and autoclaved between sessions.
- Logger deployment: nine custom PIT-tag loggers distributed across the grid to record mouse presence with high temporal resolution; rotation plan ensures even spatial coverage.
- Logger rotation: every ~3.5 days on average (2–7 per week), between 10:00–14:00; precise logger positions randomized within each territory to prevent clustering; data filtered to maintain uniform spatial coverage.
- Data cleaning: removal of corrupt logger reads; analysis focused on consistent nights; after cleaning, 83 of 93 tagged mice were represented in logger data.

## Tracking and logger data

- Logger data structure: time-stamped records of individual presence per logger and grid location; includes logger area and precise coordinates.
- Coverage: rotating territories to ensure even spatial sampling; logging nights tracked as Julian days for longitudinal analyses.
- Data quality steps: filtering steps documented (e.g., removal of nights with low activity or incomplete reads) to produce a robust dataset for downstream network analyses.

## Kinship and genotyping

- Genotyping: ear tissue genotyped at 11 microsatellite loci (initially 12; one locus discarded due to deviation from Hardy–Weinberg equilibrium).
- Methods: DNA extraction, PCR multiplexing and sequencing, allele scoring, and quality checks (COLONY, Micro-Checker) to assess errors and null alleles.
- Pedigree reconstruction: COLONY used to infer parental and sibship relationships, accounting for polygamy and genotyping error; cross-validated against trapping data and timelines to remove impossible pairs.
- Resulting pedigree: 17 mother–pup pairs, 14 father–pup pairs, 13 full-sibling pairs, 26 half-sibling pairs.
- Kinship distances: dyadic matrices created by converting kinship values to distance-like measures (e.g., parent-offspring and full siblings assigned 0.5; half-siblings and cousins 0.125).

## Gut microbiota profiling and sequencing

- Sample set: 239 fecal samples from 75 individual mice (approximately 3.2 samples per mouse; 1–9 samples per mouse).
- DNA extraction: standardized kits with randomization across plates to minimize batch effects.
- PCR and sequencing: 16S rRNA V4 region amplified; dual-indexed libraries prepared and sequenced on Illumina MiSeq (2x250 bp); inclusion of extraction and PCR controls and mock communities for quality assessment.
- Library prep and QC: index-based pooling, size selection, and library quality checks performed; mock community profiling confirmed pipeline accuracy.
- Bioinformatics: DADA2 pipeline for ASV inference; quality trimming informed by data; taxonomic assignment using GreenGenes; removal of non-gut taxa and low-read samples; singleton removal to reduce contaminants.
- Diversity and normalization: proportional abundance normalization within samples; iNEXT used to assess sample completeness and rarefaction curves; diversity estimates stabilized around 2,500–4,000 reads per sample.
- Outputs: ASV abundance table, taxa assignments, and diversity metrics for downstream analyses.

## Datasets and data formats

- silwood_rodent_trapping_data.csv: trap-date based records; columns cover trap setup/collection, site, grid, weather, rat presence, trap outcomes, species, sex, body metrics, tagging history, and ID mappings.
- silwood_rodent_capture_data.csv: per-capture event data; includes grid location, individual ID, PIT tag, species, sex, age, trapdate, and spatial coordinates.
- silwood_logger_data.csv: per-logger record data; timestamps, mouse ID and PIT tag, logger ID, grid location, territory, coordinates, sex and species, and sampling batch metadata.
- Additional metadata: pcr_plate, extraction_plate, read_depth, diversity metrics, DNA concentration, and various quality indicators for downstream QC.

## Quality control and reproducibility

- Kinship and genotyping: rigorous checks for Hardy–Weinberg deviations and genotyping errors; removal of inconsistent relationships informed by capture timing.
- Logger data: systematic filtering to ensure even spatial coverage; robust handling of missing or corrupt reads; final dataset represents 83/93 tagged mice.
- Microbiome data: randomization across extraction plates; inclusion of controls and mock communities; removal of low-count samples and non-gut taxa; normalization and diversity analyses validated with iNEXT.

## Potential analyses and practical applications

- Social network analysis: using logger data to construct contact networks and study how social structure relates to microbial sharing.
- Kinship-informed microbiome analysis: leveraging the pedigree to partition microbiome similarity by relatedness versus social association.
- Multilayer data integration: linking trapping events, space use (grid coordinates and logger territories), and kinship with microbiome composition for comprehensive ecosystem insights.
- Public data products: the dataset enables replication of kinship-based models and network metrics, with potential for dashboards or reports to support policy or conservation decisions.

## References and provenance

- Raulo et al., 2021: detailed field protocol for trapping and PIT-tag logger procedures.
- Godsall et al., 2014; Godsall et al., 2015; Wilson et al. references for microsatellite loci and pedigree analysis context.