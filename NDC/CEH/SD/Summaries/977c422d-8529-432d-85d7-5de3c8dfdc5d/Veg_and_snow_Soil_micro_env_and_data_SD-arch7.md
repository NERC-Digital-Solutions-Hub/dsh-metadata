# Alpine grassland soil microbial and biogeochemical data from a climate change and shrub expansion experiment in Tyrol, Austria, July 2019

- Field sites and location
  - Landscape-scale experiment across three Nardus stricta–dominated alpine grassland sites in the Oetztal Alps, Tyrol, Austria
  - Sites: Obergurgl (46.844833, 11.023783), Soelden (46.978367, 10.972217), Vent (46.863217, 10.896800)
  - Soil: shallow podzol
  - Climate context at closest station (Obergurgl, ZAMG): mean annual temperature 3.2°C (4.0°C in 2019); mean annual precipitation 885 mm (1106 mm in 2019)
  - Elevation: 2279–2472 m; soil pH 4.8–5.1; soil C:N 16.9–18.5

- Experimental design and treatments
  - Vegetation treatments on 2 m x 2 m plots in randomized blocks
  - Treatments: shrub-invaded, grass-control (non-invaded), shrub removal
  - Initial: 81 plots across 9 blocks per site; shrub removal allocated within shrub-invaded plots
  - Plot spacing: at least 1 m apart
  - Instrument-related exclusions: 8 Obergurgl plots and 5 Soelden plots excluded; remaining: 68 plots (n = 23, 24, 21 per treatment across sites)
  - Vent snow-vegetation manipulation: 48 plots (2 m x 2 m) cross of three vegetation treatments with two snow conditions
  - Snow treatments: snow removal vs snow cover (8 blocks; five snow-removal dates in 2018–2019)

- Field sampling and sample handling
  - Soil sampling: July 22–24, 2019; five random soil cores per plot (Ø 2 cm, depth 10 cm)
  - Processing: cores pooled per plot; vegetation/litter removed; sub-samples for molecular analyses preserved in DNA/RNA shield; field lysis performed; lysed soil stored at −80°C and shipped to UK CEH for molecular analyses
  - Additional analyses: soil sieving (4 mm), vegetation surveys, plot aspect and slope measured
  - Data files with Broadscale data contain accompanying metadata for plots, locations, and environmental variables

- Biogeochemical cycling and microbial biomass
  - Plant available inorganic N (NH4+-N, NO3−-N) and dissolved organic N (DON) measured by extraction (KCl and water) and analysed on a segmented flow analyser
  - Mineralisation rates: 14-day incubation at 25°C
  - Dissolved organic carbon (DOC) via water extraction; soil pH (1:2.5), soil moisture by gravimetric method
  - Microbial biomass C and N via chloroform fumigation-extraction (KEC and KEN corrections)
  - Soil carbon and nitrogen stocks calculated from bulk density and total C/N measurements on oven-dried soil

- Soil extracellular enzyme assays
  - Eight enzymes assessed: GLC, CBH, XYL, NAG, PHO, URE, POX, PER
  - Assays for GLC, CBH, XYL, NAG, PHO using p-nitrophenyl substrates; POX and PER via L-DOPA oxidation
  - URE activity via ammonium production from urea
  - Enzyme activities expressed per g dry soil per hour; also normalized to microbial biomass C

- Soil respiration
  - CO2 flux measured with a soil respiration chamber and IRGA
  - Measurements taken on sealed collars over 2 minutes

- PLFA analyses
  - Phospholipid fatty acid analysis to estimate fungal, Gram-positive, Gram-negative bacteria, and actinomycete abundance
  - PLFA markers used to derive total PLFA, bacterial/fungal biomarkers, and community ratios
  - Data reported as nmol g soil−1

- DNA extraction and microbial community profiling
  - DNA extracted with ZR Soil Microbe kit with added homogenization step
  - Bacterial (16S rRNA) and fungal (ITS2) community profiling via Illumina MiSeq
  - Two-step PCR with barcoded Illumina adapters; libraries normalized and sequenced
  - Rarefaction and quality control performed; ASVs generated with DADA2
  - Taxonomy assigned with Greengenes (16S) and UNITE (ITS)
  - Sequencing depth after rarefaction: ~12,630 (16S) / 2,358 (ITS) for broadscale; ~11,776 (16S) / 6,646 (ITS) for manipulative
  - Raw sequence data deposited at ENA; taxonomic information stored in Broadscale_16S_taxa and Broadscale_ITS_taxa (bacteria and fungi)

- Snow and vegetation manipulation experiment data
  - Metadata and measurements for snow-veg plots include: date, location, plot, veg treatment, snow treatment, soil moisture, inorganic and DON/DOC pools, microbial biomass, pH, bulk density
  - PLFA and enzyme activity data included alongside soil abiotic and biotic measurements
  - Snow_Veg_manipulation_16S_seq_table and Snow_Veg_manipulation_ITS_seq_table provide microbial sequence data for this experiment
  - Related environmental data file Snow_Veg_manipulation_Soil_micro_env.csv compiles plot-level environmental and soil chemistry metrics
  - Related environmental data file Snow_Veg_manipulation_16S_seq_table and Snow_Veg_manipulation_ITS_seq_table contain OTU/ASV abundances; raw sequences deposited at ENA; taxonomic data in Snow_Veg_manipulation_16S_taxa and Snow_Veg_manipulation_ITS_taxa

- Data structure and accessibility
  - Broadscale_Soil_micro_env.csv: metadata plus soil abiotic, PLFA, enzyme activities, and related measurements
  - Snow_Veg_manipulation_Soil_micro_env.csv: metadata plus soil abiotic, PLFA, enzyme activities, and respiration data for snow-vegetation manipulations
  - Broadscale_16S_seq_table and Broadscale_ITS_seq_table: OTU/ASV abundance tables per sample
  - Broadscale_16S_taxa and Broadscale_ITS_taxa: taxonomic information for OTUs/ASVs
  - Snow_Veg_manipulation_16S_seq_table and Snow_Veg_manipulation_ITS_seq_table: OTU/ASV abundance tables for snow-veg experiment
  - Snow_Veg_manipulation_16S_taxa and Snow_Veg_manipulation_ITS_taxa: taxonomic information for snow-veg OTUs/ASVs
  - Data processing tools: R (phyloseq, DADA2) used for sequence data analysis
  - All raw sequence data are deposited at ENA

- Acknowledgements
  - Funded by UK NERC (NE/N009452/1); IC supported by Ramon Areces Foundation and UK BBSRC; field work support from Alpine Research Center Obergurgl; collaboration with local ski resorts for access

- GIS-relevant notes for data use
  - Spatial scope includes three well-defined high-elevation sites with precise coordinates and elevation data
  - plot-level metadata includes aspect, slope, elevation, location blocks, and vegetation/snow treatments enabling spatial analyses and map-based visualization
  - Data layers include abiotic soil properties, microbial biomass, enzyme activities, respiration, PLFA markers, and microbial community composition (16S/ITS)
  - Data linkage across files via sample IDs (plot_ID, Sample_ID_for_sequencing) facilitates integration for GIS-based mapping and spatial analysis of biogeochemical and microbial variables