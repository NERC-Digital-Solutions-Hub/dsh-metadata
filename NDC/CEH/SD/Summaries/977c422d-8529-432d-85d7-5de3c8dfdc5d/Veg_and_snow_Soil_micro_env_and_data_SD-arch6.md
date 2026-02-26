# Supporting documentation for 'Alpine grassland soil microbial and biogeochemical data from a climate change and shrub expansion experiment in Tyrol, Austria, July 2019' deposited in the Environmental Information Data Centre repository

- Overview
  - A landscape-scale study at three alpine grassland sites in the Oetztal Alps, Tyrol, Austria, examining shrub expansion and snow/vegetation interactions on soil microbial communities and biogeochemical cycling.
  - Data types span abiotic soil chemistry, microbial biomass and community structure, enzyme activities, soil respiration, lipid biomarkers (PLFA), and DNA-based microbial community profiling (16S and ITS2) with linked environmental metadata.
  - Raw sequencing data deposited to public repositories; processed data organized for broadscale and snow-vegetation manipulation experiments.

- Field sites and experimental design
  - Sites: three Nardus stricta–dominated grasslands in Obergurgl, Soelden, and Vent.
  - Treatments (landscape-scale): shrub-invaded, grass-control (non-invaded), and shrub removal; plots 2 m x 2 m in randomized blocks (81 plots across sites; 68 analyzed after instrument failures).
  - Vent snow/vegetation manipulation: 48 plots with factorial design crossing snow removal vs snow cover with three vegetation treatments, arranged in 8 blocks; outputs include how snow and shrub expansion affect soil microbes and N cycling.
  - Plot spacing and establishment details; shrub removal protocol (plant extraction and root removal where possible).

- Field sampling and primary data collected
  - Soil sampling: July 22–24, 2019; 2 cm diameter, 10 cm depth cores from five random locations per plot; soils pooled per plot; vegetation litter removed.
  - Sub-sampling for molecular work: ~200 mg per sample preserved in DNA/RNA shield, field-lysis performed, samples stored at -80°C and shipped to UKCEH for molecular analyses.
  - Vegetation surveys and site measurements (aspect and slope) were conducted prior to soil sampling.

- Biogeochemical cycling and microbial biomass measurements
  - Plant available inorganic N (NH4+-N, NO3−-N) and DON measured from soil extracts (1 M KCl and water) using a segmented flow analyser.
  - Mineralisation rates measured by 14-day incubation at 25°C.
  - Dissolved organic carbon (DOC) and soil pH measured; soil water content and bulk density determined; soil C and N stocks calculated.
  - Microbial biomass C and N determined via chloroform-fumigation-extraction with EC/baseline corrections (KEC = 0.45 for C, KEN = 0.54 for N).

- Soil extracellular enzyme assays
  - Eight enzymes assessed: GLC, CBH, XYL, NAG, PHO, URE, POX, PER; substrates and assay protocols described, including colorimetric or fluorometric readouts.
  - Enzyme activities expressed as nmol product per g dry soil per hour (or µmol for POX/PER), with corrections for soil colour and cofactors.
  - Peroxidase activity corrected by subtracting POX from PER due to overlapping substrates.

- Soil respiration and PLFA analyses
  - CO2 flux measured in the snow/vegetation manipulation experiment with soil respiration chambers and IRGA over 2 minutes per plot.
  - PLFA analyses used to characterize fungal, GP- and GN-bacterial, and actinomycete biomarkers; results in nmol g soil−1 and used to infer microbial community structure and biomass.

- DNA extraction and microbial community profiling
  - DNA extracted with Zymo kit, with an enhanced lysis step; DNA stored for downstream sequencing.
  - Bacterial and fungal community structure analyzed via amplicon sequencing of 16S rRNA and ITS2, respectively.
  - Two-step Illumina PCR protocol with barcoded adapters; libraries normalised and sequenced on MiSeq (V3 chemistry).
  - Data processing via DADA2 in R: quality filtering, ASV inference, chimera removal; taxonomic assignment with GreenGenes v13.8 (16S) and UNITE v7.2 (ITS).
  - Rarefaction performed to even depths (broadscale: 16S to 12,630; ITS to 2,358; manipulative: 11,776 for 16S; 6,646 for ITS).
  - OTU/ASV tables linked to sample metadata; raw sequences deposited or to be deposited in ENA; taxonomic information stored in corresponding taxa files.

- Data structure and files (core datasets)
  - Broadscale_Soil_micro_env.csv: metadata and soil abiotic, PLFA, enzyme activity, and related measurements for landscape-scale data. Key columns include plot_ID, site, location, veg treatment, latitude/longitude, elevation, aspect, slope, soil C/N, moisture, DNH4, DNO3, DON, DTOC, pH, bulk density, MicBN/MicBC, microbial C/N, and enzyme activities (nagr, phor, cbhr, xylr, glcr, perr, poxr, urer) plus PLFA biomarkers.
  - Broadscale_16S_seq_table and Broadscale_ITS_seq_table: ASV/OTU abundance tables (bacteria and fungi) aligned to Broadscale_Soil_micro_env.csv via sample/plot IDs; raw sequence data referenced for ENA deposition.
  - Broadscale_16S_taxa and Broadscale_ITS_taxa: taxonomic assignments for the ASVs/OTUs.
  - Snow_Veg_manipulation_Snow_... (Snow_Veg_manipulation_Soil_micro_env.csv): metadata, abiotic soil data, PLFA, enzymes, and soil respiration for the snow-vegetation manipulation experiment; includes bulk density, pH, soil carbon/nitrogen, moisture, and respiration.
  - Snow_Veg_manipulation_16S_seq_table and Snow_Veg_manipulation_ITS_seq_table: OTU/ASV tables for bacterial and fungal taxa in the snow-vegetation manipulation experiment; sample names link to Snow_Veg_manipulation_Soil_micro_env.csv.
  - Snow_Veg_manipulation_16S_taxa and Snow_Veg_manipulation_ITS_taxa: taxonomic information for Snow_Veg manipulation data.
  - Snow_Veg_manipulation_Soil_micro_env.csv, Snow_Veg_manipulation_16S_seq_table, Snow_Veg_manipulation_ITS_seq_table: same structure as above but for the snow/vegetation manipulation dataset.
  - Data structure notes: files include sample IDs, site/plot associations, measurement units, and references to ENA for raw sequences.

- Data processing pipelines and methodological notes
  - Sequencing and analysis: 2-step Illumina PCR; barcode- and adapter-tagged libraries; SequalPrep normalisation; sequencing on MiSeq with PhiX control; sequence processing via DADA2 in R; taxonomic assignment against Greengenes (16S) and UNITE (ITS).
  - Enzyme assays: photometric assays with substrate hydrolysis rates; corrections for soil colour and background; for NAG, PHO, GLC, CBH, XYL specifics described; POX and PER measured using L-DOPA substrate with time-point readings; URE via ammonia production colorimetric method.
  - PLFA: extraction and analysis using established lipid biomarkers to estimate fungal vs bacterial and actinomycete communities; results expressed as nmol g soil−1.
  - Microbial biomass and C/N calculations: standard fumigation-extraction with EC/EN correction factors; bulk density and soil C/N stocks computed from oven-dried soil measurements.
  - Data linkage: environmental metadata linked to sequencing data via plot_ID or equivalent sample identifiers; raw sequence data to ENA; processed data files contain explicit cross-references to sample IDs.

- Quality, limitations, and notes for data use
  - Instrument failure reduced the initial plot set (8 plots excluded at Obergurgl; 5 at Soelden), resulting in 68 usable plots.
  - Sequencing depth and rarefaction were standardized to ensure comparability across samples; caution advised when interpreting low-abundance taxa.
  - Enzyme activity data are normalized to microbial biomass where indicated to reflect investment in enzymes relative to microbial abundance.
  - Methodological references are provided for each assay, enabling reproduction or method validation.

- Accessibility and reuse
  - Data hosted in the Environmental Information Data Centre repository with detailed metadata and documentation.
  - Raw sequence data are deposited or in the process of deposition to the European Nucleotide Archive (ENA).
  - Structured data files (broadscale and snow/vege manipulation datasets) are organized for integration across abiotic, biogeochemical, enzymatic, PLFA, and sequencing domains, enabling cross-domain analyses and dashboards.

- Potential data products and use cases for data support
  - Self-serve dashboards or tables combining soil chemistry, enzyme activities, microbial biomass, PLFA signatures, and microbial community composition across sites and treatments.
  - Cross-site comparisons of shrub expansion and snow manipulation effects on N cycling and microbial functional potential.
  - Linkages between environmental drivers (pH, C/N, moisture) and microbial functional genes inferred from 16S/ITS profiles.
  - Longitudinal or cross-experiment analyses leveraging consistent data structures to explore ecosystem responses to climate-related shrub expansion.

- Acknowledgments and references
  - Dataset accompanied by extensive methodological references (enzyme assays, PLFA, DNA extraction and sequencing, and data processing with DADA2, Greengenes, UNITE).
  - Funding and collaboration acknowledgments noted; data collection supported by NERC and related institutional partners.