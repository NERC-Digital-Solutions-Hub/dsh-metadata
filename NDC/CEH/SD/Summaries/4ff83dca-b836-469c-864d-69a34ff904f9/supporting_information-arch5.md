# Data overview

- The dataset contains metadata and measurements from an experiment imposing four climatic disturbances (drought, flooding, freezing, heat) on soils from 30 European grassland sites, plus a control, followed by a recovery period. It includes whole-genome metagenomics, bacterial and fungal sequencing, microbial enzymatic activities, substrate-induced respiration, and carbon and nitrogen fluxes. European Nucleotide Archive accession numbers for molecular data are provided.
- Key data outputs include site descriptions, treatments, measurements, and accession numbers, organized for discovery and reuse.

## Experimental design and sampling

- 30 replicate sites across 10 European countries, selected to span diverse climates and soil types (Haplic Cambisols, Podzols, Kastanozems, Luvisols, etc.).
- Climate data sourced from WorldClim (1960–1990 baseline) to capture wide MAP and MAT variation.
- Sampling executed May–August 2018; three replicate sites per country, with seven plots per replicate, and soil cores collected to form 30 homogenized samples per site.
- Microcosms established (20 pots per replicate) and subjected to five treatments for 14 days: Control, Drought, Flood, Freeze, Heat.
- Sampling at four timepoints after disturbance end: S1 (immediate), S2 (1 day), S3 (8 days), S4 (26 days); total of 600 microcosms produced (later excluding 10 Russian samples due to insufficient soil).
- In-field and lab measurements include moisture, nutrients, and gas fluxes; DNA-based analyses conducted on selected samples.

## Microcosm procedure and harvest

- Acclimation: 7 days at 18°C, 60% WHC.
- Disturbance period: 14 days with defined moisture/temperature settings per treatment.
- Sampling: at S1–S4, with gas flux measurements in sealed jars and subsequent soil subsampling for moisture, nutrients, and DNA; additional soil stored for MicroResp and enzymatic assays.

## Measurements and functional assays

- Greenhouse gas fluxes (CO2, N2O, CH4) calculated as mg gas per g dry soil per hour, adjusted for headspace and temperature.
- Substrate-induced respiration (MicroResp) measured with several carbon substrates to estimate microbial respiration rates.
- Enzymatic activity assays for acetyl esterase, β-glucosidase, phosphatase, and leucine-aminopeptidase using MUB/AMC substrates.
- Dissolved organic/inorganic carbon and nitrogen quantified from water extracts; pH measured; total soil C and N determined by high-temperature combustion.

## DNA sequencing and analysis

- DNA extracted from 250 mg of soil; quality assessed before sequencing.
- Bacterial and fungal communities characterized by amplicon sequencing:
  - 16S rRNA gene (V4–V5) with standard Earth Microbiome Project primers.
  - ITS2 region for fungi.
  - Sequencing performed on Illumina MiSeq (2x300 bp) with a 2-step Nextera approach.
  - Data processed with DADA2 to generate ASVs; taxonomies assigned using SILVA (bacteria) and UNITE (fungi).
- Functional gene composition determined by whole-metagenome sequencing (28 initial samples plus 28 replicate sites × 2 times × 5 treatments = 308 samples; later notes indicate 574 samples analyzed after exclusions).
- Functional annotation via MG-RAST using SEED Subsystems (M5nr).
- Some DNA samples from Spain (n=42) and certain other samples were excluded due to insufficient yield or low-quality sequences, resulting in 574 total DNA samples used in analyses.

## Data structure and accessibility

- Two CSV files:
  - Disturbance_data.csv: 91 columns, 620 samples (includes provenance, treatments, measurements, and ENA accession numbers).
  - Disturbance_metadata_header_description.csv: detailed description of the 91 column headers.
- NA denotes missing data; missingness reflects baseline information, subsetted assays, or site-specific measurement availability.
- Molecular data accession numbers provided; metadata supports re-use and traceability of initial and microcosm samples.

## Data quality, limitations, and exclusions

- Exclusions: 10 Russian samples at S2 due to insufficient soil; several Spain samples due to DNA yield issues; some samples with low-quality sequences excluded.
- Some assays (e.g., enzymatic activity, whole-genome metagenomics) were performed on subsets of sites or at specific time points, resulting in partial coverage across the full dataset.

## Governance, use, and stewardship considerations

- Aligns with data stewardship aims: comprehensive metadata, standardized measures, and accessioned molecular data to enable discovery, reuse, and integration with other datasets.
- Clear documentation of sampling design, treatments, timepoints, and measurement methods supports reproducibility and interoperability across systems.
- Data uploaded to appropriate data portals and catalogues; ongoing updates and caveats regarding limitations (e.g., incomplete coverage, excluded samples) should be tracked and communicated to data users.
- Considerations for future users include the distinctions between INITIAL field samples and lab microcosm manipulations, varying coverage across assays, and the use of multiple reference databases for taxonomy and function.