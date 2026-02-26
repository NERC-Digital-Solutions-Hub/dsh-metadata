# Data overview

- dataset of metadata and measurements from an experiment imposing four climatic disturbances on soils from 30 European grassland sites, plus a control.
- aims to capture microbial community responses and soil functioning under disturbance and recovery, using multi-omics and soil-physiology data.
- includes European Nucleotide Archive accession numbers for molecular data.

## Experimental design and sampling regime

- grassland network across Europe: 10 locations covering a wide range of climates; 30 replicate sites (3 per country) across 7 soil types.
- sampling horizon: soils from 0–15 cm (organic horizon), collected per site and pooled per replicate.
- microcosm setup: 20 pots per replicate site, standardised to 100 g dry soil per pot.
- disturbances (14 days) and recovery: five treatments after acclimation (Ct control; D drought at 10% WHC; Fd flooding at 100% WHC; Fz freeze at -20°C with 60% WHC; H heat at 35°C with 60% WHC).
- disturbance end and recovery: measurements at end of disturbance and at 1 day (S2), 8 days (S3), and 26 days (S4) after disturbance end; initial baseline sampling (S1) taken before final adjustments for some treatments.
- sample scope: 600 microcosms (10 countries × 3 replicate sites × 5 treatments × 4 sampling times); 10 Russian samples at S2 excluded due to insufficient soil.

## Measurements and data types

- soil microbiology and function
  - whole-genome metagenomics (shotgun) on a subset of samples
  - bacterial (16S rRNA V4-V5) and fungal (ITS2) amplicon sequencing
  - substrate-induced respiration (MicroResp) profiles
  - enzymatic potential activities: acetyl esterase, β-glucosidase, phosphatase, leucine aminopeptidase (MUB/AMC substrates)
  - soil carbon and nitrogen pools: total C and N; dissolved organic/inorganic N and C
  - dissolved nutrients: DON, inorganic N (NH4-N, NO3-N)
- gas flux measurements
  - greenhouse gas emissions: CO2, N2O, CH4
  - measurement via 500 mL headspace jars; gas chromatography; fluxes normalised to soil dry weight
- additional soil properties
  - pH (initial samples)
  - soil moisture (via WHC measurements)
- data scope
  - 620 samples with associated metadata; 30 initial samples plus 590 microcosm samples

## Molecular data processing and analysis

- amplicon data processing
  - primers: 16S rRNA V4-V5 (bacteria) and ITS2 (fungi)
  - sequencing via Illumina MiSeq (2x, V3 chemistry)
  - data processing with DADA2 to generate ASV tables and taxonomies
  - bacterial taxonomy using SILVA (SSU r132); fungal taxonomy using UNITE dynamic database
  - minimum sequencing depth filter: samples with fewer than 2,000 reads excluded
- metagenomics
  - whole-metagenome sequencing on 308 samples (initial ES1/ES3 excluded; 28 initial samples plus 28 sites × 2 times × 5 treatments)
  - library prep: TruSeq PCR-free; NovaSeq 2x150 bp
  - functional annotation with MG-RAST SEED Subsystems
- DNA extraction and QC
  - extraction: DNeasy PowerSoil Pro Kit
  - quality checks: gel check, 260/280 ratios, fluorometric quantification
  - DNA stored at -20°C until sequencing
- final data scope (quality-filtered)
  - 574 samples used for DNA analyses after exclusions (e.g., low-yield or low-quality sequences; Spain replicate sites 1 and 3 exclusions)

## Data structure and file descriptions

- Disturbance_data.csv
  - 91 columns
  - 620 samples (rows)
  - fields include: sample provenance (site, replicate, country, description), treatment, measured metrics (GHG fluxes, enzymes, respiration, soil properties), and European Nucleotide Archive accession numbers
- Disturbance_metadata_header_description.csv
  - detailed description of each of the 91 column headers
- data completeness and caveats
  - NA used to denote missing information
  - some measures available only on the initial field samples or only on lab-manipulated samples
  - certain assays (e.g., enzymes, whole-genome metagenomics) performed only on subset of sites and time points

## Quality control, exclusions, and caveats

- sampling exclusions
  - 10 Russian samples at S2 removed due to insufficient soil
- molecular data exclusions
  - DNA yield insufficient for Spain replicate sites 1 and 3; additional exclusions for low-quality sequences
- resulting data scope
  - 620 samples described in the data headers
  - 574 samples retained for DNA analyses after quality filtering
  - 308 samples subjected to whole-metagenome sequencing (before exclusions)

## Potential data uses for data support work

- cross-site comparisons of microbial community structure (bacteria and fungi) and function under drought, flood, freeze, and heat disturbances
- linking amplicon and metagenomic data with measured soil processes (GHG fluxes, respiration, enzyme activities) to identify drivers of soil resilience
- building self-serve data products (dashboards, queries) enabling exploration of disturbance effects across climates and soil types
- meta-analyses or case studies of disturbance-recovery dynamics in European grassland soils, with rich metadata for contextual understanding (climate, soil type, geographic location)