# Alpine grassland soil microbial and biogeochemical data from a climate change and shrub expansion experiment in Tyrol, Austria, July 2019

## Overview
- Landscape-scale experiment across three Nardus stricta–dominated alpine grassland sites in the Ötztal Alps, Tyrol, Austria.
- Investigates shrub expansion by native ericaceous dwarf-shrubs (Calluna vulgaris and Vaccinium spp.) with three vegetation treatments: shrub-invaded, grass-control, and shrub removal.
- At the Vent site, a snow and vegetation manipulation experiment was added to study effects on soil microbial communities, biogeochemical cycling, and plant–microbial competition for nitrogen; treatments cross snow cover (removal vs. snow) with vegetation treatments.
- Fieldwork and sampling conducted July 2019; data cover soil chemistry, microbial biomass, enzyme activities, microbial community structure, and soil organic matter dynamics.

## Field sites and experimental design
- Sites and coordinates:
  - Obergurgl: 46.844833 N, 11.023783 E
  - Soelden: 46.978367 N, 10.972217 E
  - Vent: 46.863217 N, 10.896800 E
- Soil type: shallow podzol; elevation 2279–2472 m; mean annual temperature ~3.2–4.0 °C; mean annual precipitation ~885–1106 mm (2019)
- Plot layout:
  - 2 m × 2 m plots in randomized blocks; 81 plots total (27 per vegetation treatment) across sites.
  - Exclusions due to equipment failures reduced usable plots to 68 (n per treatment: shrub-invaded 23, grass-control 24, shrub removal 21).
  - Plot spacing: ≥1 m; vegetation surveys and slope/aspect measurements recorded.

## Treatments and manipulations
- Vegetation treatments (2017):
  - Shrub-invaded
  - Grass-control (non-invaded)
  - Shrub removal (within shrub-invaded plots; shrubs removed by excavating plants or cutting at bases; roots removed where possible)
- Snow/vegetation manipulation (Vent site; 2018–2019):
  - Snow removal vs. snow cover (snow control)
  - Fully crossed with the three vegetation treatments in 8 blocks (8 replicates per combination)

## Field sampling and measurements
- Soil sampling:
  - Dates: July 22–24, 2019
  - Method: five random soil cores per plot (2 cm diameter, 10 cm depth); cores pooled and homogenised; vegetation/litter removed; samples preserved for DNA/RNA analyses.
- Abiotic and chemical measurements:
  - Soil moisture, bulk density, pH (1:2.5 soil/water), total C and N, soil C:N, dissolved organic carbon (DOC), dissolved inorganic N (NH4+, NO3−), DON, DIN, DTN, DON, DTOC
  - Plant-available N calculated from extractions (1 M KCl for NH4+/NO3−; water for DON)
  - Mineralisation potential: 14-day incubation at 25 °C with NH4+/NO3− measured
- Microbial biomass and activity:
  - Microbial biomass C and N via chloroform fumigation–extraction (KEC and KEN corrections applied)
  - Microbial biomass stocks combined with soil bulk density to estimate mg C or N per cm³ soil
- Soil extracellular enzyme assays (eight enzymes):
  - GLC (β-glucosidase), CBH (cellobiohydrolase), XYL (β-xylosidase), NAG, PHO, URE, POX (phenol oxidase), PER (peroxidase)
  - Substrate-specific colorimetric assays with appropriate buffers; enzymatic activities expressed as nmol product g⁻¹ dry soil h⁻¹; correction for soil colouration; peroxidase activity corrected by subtracting POX where necessary; additional normalization to microbial biomass C
- Soil respiration:
  - CO₂ flux measured with a soil respiration chamber and IRGA over 2 minutes
- PLFA analyses (phospholipid fatty acids):
  - Biomarkers for fungi, Gram-positive and Gram-negative bacteria, and actinomycetes; abundance reported as nmol g⁻¹ soil
  - Used to derive microbial community composition and compute fungal-to-bacterial and GP:GN ratios
- DNA extraction and microbial community profiling:
  - DNA extraction using Zymo kit with enhanced lysis
  - Bacterial and fungal community profiling via Illumina sequencing of 16S rRNA and ITS2 regions
  - Two-step PCR with Illumina adapters and sample-specific barcodes; libraries normalised and sequenced on MiSeq (V3 chemistry)
  - Data processing with DADA2 in R: quality filtering, ASV inference, chimera removal; taxonomic assignment using Greengenes (16S) and UNITE (ITS)
  - Rarefaction to even sequencing depth (broadscale: 16S 12,630; ITS 2,358; manipulative: 11,776 and 6,646 respectively)
- Data provenance and linking:
  - Sequencing sample IDs linked to a combined environmental data file
  - Raw sequence data deposited or pending deposition at the European Nucleotide Archive (ENA)

## Data structure and files (ENVIS/ETC)
- Broadscale_Soil_micro_env.csv
  - Metadata, soil abiotic data, PLFA, soil extracellular enzyme activities
  - Columns include: plot_ID, date, site, location/block, veg treatment, coordinates, elevation, aspect, slope, soil chemistry (N, C, C:N, PN), moisture, DNH4, DNO3, DIN, DTN, DON, DTOC, ENH4, ENO3, EIN, ETN, EON, MicBN, MicBC, MicCN, pH, urer, nagr, phor, cbhr, xylr, glcr, perr, poxr, i-C15:0, a-C15:0, several C16/17/18/19 PLFAs
- Snow_Veg_manipulation_Soil_micro_env.csv
  - Metadata, soil abiotic data, PLFA, soil extracellular enzyme activities, and soil respiration for snow-vegetation manipulation
  - Similar columns to Broadscale file plus snow treatment and combined location/plot fields
- Broadscale_16S_seq_table and Broadscale_ITS_seq_table
  - OTU/ASV abundance tables for bacteria (16S) and fungi (ITS), post-rarefaction
- Snow_Veg_manipulation_16S_seq_table and Snow_Veg_manipulation_ITS_seq_table
  - OTU/ASV abundance tables for bacteria and fungi in snow/vegetation manipulation experiment
- Broadscale_16S_taxa and Broadscale_ITS_taxa; Snow_Veg_manipulation_16S_taxa and Snow_Veg_manipulation_ITS_taxa
  - Taxonomic assignments corresponding to the sequence tables
- ENA deposition note
  - Raw sequence data are or will be deposited in ENA

## Data processing and analysis notes
- High-throughput sequence data processing:
  - 2-step Illumina PCR protocol with tagged primers
  - Demultiplexed, quality-filtered, merged reads; ASV inference with DADA2
  - Taxonomic assignment against Greengenes (16S) and UNITE (ITS)
  - Phyloseq used for downstream analysis
- Data normalization and comparisons:
  - Rarefaction to specified depths to account for sequencing depth differences
  - Enzyme activities normalized to microbial biomass (µmol product g⁻¹ soil per hour per unit biomass)
- Metadata integration:
  - Environmental metadata linked to microbial data via sample/plot IDs
  - Slope, aspect, elevation, and other site characteristics captured to facilitate correlations with microbial and biogeochemical responses

## Purpose and potential analyses
- Enables investigations of:
  - How shrub expansion and snow manipulation influence soil nutrients, microbial biomass, enzyme activities, and respiration
  - Shifts in microbial community structure (bacteria vs fungi, Gram-positive/negative balance, actinomycetes)
  - Relationships between microbial community composition, enzymatic potential, and biogeochemical cycling (N and C fluxes)
  - Correlations between environmental gradients (elevation, pH, moisture) and soil microbial / enzyme responses
- Provides a rich, multi-ecosystem dataset suitable for correlational and predictive analyses to infer impacts of shrub encroachment and snow changes on alpine soil processes

## Access and acknowledgements
- Data deposited in Environmental Information Data Centre repository; ENA deposition ongoing or completed for raw reads
- Funded by UK NERC and supported by Alpine Research Center Obergurgl; field teams and ski-resorts provided access and support