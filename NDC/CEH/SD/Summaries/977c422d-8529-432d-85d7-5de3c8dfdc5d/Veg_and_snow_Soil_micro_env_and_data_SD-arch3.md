# Supporting documentation for 'Alpine grassland soil microbial and biogeochemical data from a climate change and shrub expansion experiment in Tyrol, Austria, July 2019' deposited in the Environmental Information Data Centre repository

## Overview
- Describes the field experiments, sampling, and laboratory analyses that produced the Alpine grassland soil microbial and biogeochemical data.
- Outlines the study design (vegetation and snow/vegetation manipulations), data types collected, data processing methods, and data structure files.
- Establishes the basis for monitoring environmental health indicators and informing policy decisions through multi-omic, biogeochemical, and soil-function metrics.
- Notes data availability, data formats, and provenance to support transparency and re-use.

## Study locations and context
- Landscape-scale experiment at three Nardus stricta–dominated alpine grassland sites in the Oetztal Alps, Tyrol, Austria.
- Invasion by native ericaceous dwarf-shrubs (Calluna vulgaris and Vaccinium spp.) and shrub expansion as climate-related context.
- Soil type: shallow podzol; site elevations 2279–2472 m; mean annual temp ~3.2°C (1981–2010) with 2019 being ~4.0°C; precipitation ~885 mm (1981–2010) and ~1106 mm in 2019.
- Datafiles with 'Broadscale' in their filename pertain to the landscape-scale experiment; 'Snow_Veg_manipulation' data pertain to the snow and vegetation manipulation site.

## Experimental design and treatments
- Vegetation treatments (2 m × 2 m plots, randomized blocks):
  - shrub-invaded
  - grass-control (non-invaded control)
  - shrub removal
- Total plots: 81 across sites; instrument failures reduced usable plots to 68 (Obergurgl and Soelden affected). Shrub removal randomly allocated within shrub-invaded plots.
- Vent site includes a Snow_Veg manipulation experiment (48 plots) fully crossed with the three vegetation treatments:
  - snow removal vs snow cover
  - replicated across 8 blocks
- Sampling and measurements were conducted across these treatment combinations to disentangle effects of shrub expansion and snow cover on soil microbial processes and biogeochemistry.

## Field sampling and sample handling
- Soil sampling: July 22–24, 2019; five random soil cores per plot (2 cm diameter, 10 cm depth); cores pooled per plot.
- Sub-samples prepared for molecular analyses and preserved in DNA/RNA shield; immediate field lysis; samples stored at −80°C and shipped to UK for molecular work.
- Soil processing: sieving (4 mm), storage at 4°C, shipping for extracellular enzyme and biogeochemical analyses.
- Ancillary data: vegetation surveys; plot aspect and slope measured prior to sampling.

## Measurements and analyses

### Biogeochemical cycling and microbial biomass
- Plant available nitrogen: NH4+-N and NO3−-N (1 M KCl extraction) and DON (water extraction).
- Mineralisation: 14-day incubation at 25°C; NH4+-N and NO3−-N release measured.
- Dissolved organic carbon (DOC): water extraction and TOC analysis.
- Soil pH (1:2.5 soil:water) and gravimetric soil moisture.
- Microbial biomass C and N: chloroform-fumigation extraction with K2SO4; application of EC/EN correction factors (KEC = 0.45, KEN = 0.54).
- Soil carbon and nitrogen stocks calculated from C/N percentages and bulk density.

### Soil extracellular enzyme assays
- Eight enzymes: GLC, CBH, XYL, NAG, PHO, URE, POX, PER.
- Substrates and protocols described; activities measured as product formation (absorbance-based assays) and corrected for colouration.
- Enzyme activity also normalised to microbial biomass C to assess investment per microbial unit.

### Soil respiration
- CO2 flux measured with soil respiration chamber and IRGA; measurements over 2 minutes per collar.

### PLFA analyses
- Phospholipid fatty acid analysis to estimate fungal, Gram-positive, Gram-negative bacteria, and actinomycete groups.
- Biomarker sets and calculations for total PLFA, bacterial abundance, fungal:bacterial ratios, and GP:GN ratios.

### DNA extraction and sequencing
- DNA extracted with a Zymo kit, with additional lysis step for improved yield.
- Bacterial (16S rRNA) and fungal (ITS2) communities profiled via 2-step Illumina PCR with tagged primers; libraries prepared and sequenced on MiSeq (V3 chemistry).
- Sequence processing with DADA2 in R; ASV tables generated; taxonomic assignment using Greengenes (16S) and UNITE (ITS).
- Rarefaction standardized across samples to comparable depths.

## Data structure and content

### Broadscale data files
- Broadscale_Soil_micro_env.csv: metadata and soil abiotic, PLFA, and enzyme data with columns for plot, site, vegetation treatment, location, soil chemistry (N, C, pH), moisture, microbial biomass, DON/DIN/DIN, DOC, DTN, DON, DTOC, bulk density, and enzyme activities (nagr, phor, glcr, cbhr, xylr, perr, poxr, urer) among others.
- Broadscale_16S_seq_table and Broadscale_ITS_seq_table: OTU and ASV tables for bacteria and fungi; raw sequencing data deposited to ENA; taxonomic mappings in Broadscale_16S_taxa and Broadscale_ITS_taxa.
- Snow_Veg_manipulation_Soil_micro_env.csv: metadata and soil abiotic, PLFA, enzyme activities, and soil respiration for the snow-vegetation manipulation experiment; includes snow, vegetation, soil moisture, nutrient pools, microbial biomass, pH, bulk density, and enzyme activities; downstream sequencing tables Snow_Veg_manipulation_16S_seq_table and Snow_Veg_manipulation_ITS_seq_table with corresponding taxonomic files.

### Snow_Veg_manipulation data files
- Snow_Veg_manipulation_16S_seq_table and Snow_Veg_manipulation_ITS_seq_table: OTU/ASV abundance per sample; sample naming aligns with Snow_Veg_manipulation_Soil_micro_env.csv.

## Data access, processing, and quality
- Raw sequence data deposited or in process at the European Nucleotide Archive (ENA).
- Data processed with standard, high-throughput methods (DADA2 for ASVs; Greengenes and UNITE databases for taxonomy).
- Replicate measurements and technical replicates provided for enzyme assays and other analyses; data include QA steps such as blank corrections and substrate colouration corrections.
- Data files include extensive metadata to support re-use and integration with policy-focused monitoring frameworks.

## Governance, openness, and reuse
- Emphasis on data openness, metadata richness, and sharing of underlying data to support transparent monitoring and policy evaluation.
- Datasets are organized with clear variable meanings and documentation to enable cross-site comparability and longitudinal analyses.
- Data structure files link environmental conditions, microbial community data, and functional measurements to specific plots and treatments.

## Limitations and considerations for monitoring
- Instrument failure led to exclusion of several plots; cross-site manipulations and snow-vegetation interactions may limit generalizability to other systems.
- Enzyme assays and molecular data provide proxies of function and structure, which should be interpreted in the context of potential methodological biases (e.g., extraction efficiency, PCR biases).
- Temporal snapshot (July 2019) represents a specific seasonal window; longitudinal monitoring would strengthen policy-relevant inferences.

## Relevance for monitoring frameworks and policy decisions
- Demonstrates a multi-layered environmental health monitoring approach, combining:
  - Abiotic soil chemistry and nutrient pools
  - Microbial biomass and community structure (PLFA, 16S/ITS)
  - Microbial functional potential (extracellular enzyme activities)
  - Soil carbon and nitrogen stocks
  - Soil respiration as a flux metric
- Supports policy-relevant metrics for climate-change responses and shrub expansion impacts on soil health and ecosystem functioning.
- Provides a transparent data workflow, from field sampling to high-throughput sequencing and data processing, with clearly defined data products and metadata to facilitate policy analysis, benchmarking, and evidence-based decision making.