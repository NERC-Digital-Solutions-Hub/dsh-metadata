# Supporting documentation for 'Alpine grassland soil microbial and biogeochemical data from a climate change and shrub expansion experiment in Tyrol, Austria, July 2019' deposited in the Environmental Information Data Centre repository

## Purpose and scope
- Provides standardized, site-based environmental data (soil microbial, biogeochemical, and community data) from an alpine grassland experiment assessing climate change and shrub expansion effects.
- Enables monitoring of environmental health and policy performance over time; data are prepared for scrutiny and potential integration with other datasets.

## Field sites and experimental design
- Location: three Nardus stricta–dominated alpine grassland sites in the Oetztal Alps, Tyrol, Austria (Obergurgl, Soelden, Vent).
- Context: invasion by ericaceous shrubs (Calluna vulgaris and Vaccinium spp.).
- Site characteristics: shallow podzols; mean annual temperature ~3.2–4.0 °C; precipitation ~885–1106 mm; elevations 2279–2472 m; soil pH 4.8–5.1; soil C:N 16.9–18.5.
- Treatments:
  - Vegetation study: shrub-invaded, grass-control, shrub removal; 2 m x 2 m plots; randomized block design; 81 plots initially (27 per treatment) across sites; 68 plots used after instrument failures.
  - Vent snow-vegetation manipulation: 48 plots crossed with three vegetation treatments in 8 blocks; snow removal vs snow cover.
- Sampling timeframe: field sampling in July 2019.

## Field sampling and sample processing
- Soil sampling: five cores per plot (2 cm diameter, 10 cm depth); cores pooled per plot; vegetation/litter removed; subsamples preserved for molecular analyses in DNA/RNA preservation buffer, lysed in the field, and stored at -80 °C for UK analyses.
- Additional subsamples processed for extracellular enzyme and biogeochemical analyses; vegetation surveys and plot slope/aspect recorded.

## Biogeochemical cycling and microbial biomass
- Plant available inorganic N (NH4+, NO3−), dissolved organic nitrogen (DON); DON via water extraction; inorganic N via 1 M KCl extraction.
- Mineralisation: 14-day incubation at 25 °C.
- Dissolved organic carbon (DOC) via TOC analyzer; soil pH; soil moisture (gravimetric).
- Microbial biomass C and N via chloroform fumigation-extraction with EC factors (KEC = 0.45, KEN = 0.54).
- Soil bulk density and carbon/nitrogen stocks computed from core measurements and elemental analysis.

## Soil extracellular enzyme assays
- Eight enzymes measured: GLC, CBH, XYL (carbohydrate-active), NAG (chitin), PHO (phosphatase), URE (urease), POX, PER (phenol oxidase and peroxidase).
- Assay details provided; activities expressed per g soil and also relative to microbial biomass C.

## Soil respiration
- CO2 flux measured with a soil respiration chamber and IRGA; gas sampling over 2 minutes per plot.

## PLFA analyses
- Phospholipid fatty acid analysis to quantify fungal and bacterial groups (GP, GN) and actinomycetes; total PLFA and fungal:bacterial ratios calculated.

## DNA extraction and microbial community profiling
- DNA extracted with Zymo kit with added lysis step; eluates stored at -20 °C.
- Bacterial and fungal communities profiled via amplicon sequencing of 16S rRNA (bacteria) and ITS2 (fungi) using Illumina MiSeq; two-step PCR with barcoded adapters; libraries normalised and sequenced.
- Data processing with DADA2 in R to produce ASV tables; taxonomic assignment against Greengenes (16S) and UNITE (ITS); sequences rarefied to standard depths.

## Data structure and access
- Broadscale_Soil_micro_env.csv: metadata plus soil abiotic, PLFA, enzyme activities, respiration, etc. (fields include plot_id, site, veg treatment, elevation, pH, Soil_pct_C/N, DIN/DON, DTOC, MicBN/MicBC, microbial ratios, urER, nagr, phor, glcr, cbhr, xylr, perr, poxr, and PLFA markers).
- Broadscale_16S_seq_table and Broadscale_ITS_seq_table: OTU/ASV counts per sample; taxonomies in Broadscale_16S_taxa and Broadscale_ITS_taxa.
- Snow_Veg_manipulation_Soil_micro_env.csv: metadata and soil biogeochemistry, PLFA, enzymes, respiration for snow-vegetation experiments.
- Snow_Veg_manipulation_16S_seq_table and Snow_Veg_manipulation_ITS_seq_table: sequencing data for manipulative experiment; taxonomies in corresponding taxa files.
- Raw sequence data: deposited in the European Nucleotide Archive (ENA).
- Data storage and accessibility: datasets deposited in the Environmental Information Data Centre (EIDC) and underlying data available via ENA.

## Reuse, value and considerations for analysts
- Data follow standardized collection and QA procedures, suitable for cross-site temporal comparisons and monitoring of environmental health and policy performance.
- High value when combined with other environmental datasets (e.g., climate, land-use data) to assess shrub expansion and snow manipulation effects on soil microbial function and biogeochemistry.
- Underlying data and raw sequences enable independent validation and broader analyses.

## Acknowledgments and funding
- Funded by UK Natural Environment Research Council (NERC NE/N009452/1); additional support and collaborations acknowledged; field access and data deposition facilitated by participating institutions.