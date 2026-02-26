# Supporting documentation for 'Alpine grassland soil microbial and biogeochemical data from a climate change and shrub expansion experiment in Tyrol, Austria, July 2019' deposited in the Environmental Information Data Centre repository

## Overview
- Describes field experiments and multi-omic across-site data collection in Tyrol, Austria (July 2019), focusing on alpine grassland soil microbial communities and biogeochemical cycling under shrub expansion and climate-related manipulations.
- Data span environmental measurements, soil chemistry, microbial biomass and community structure, enzyme activities, soil respiration, PLFA profiles, and DNA-based microbial communities (16S for bacteria, ITS2 for fungi).
- Two interconnected data streams: broadscale landscape experiment and Snow_Veg_manipulation experiment, with raw sequencing data deposited to ENA.

## Field Sites and Experimental Design
- Field sites: three Nardus stricta-dominated alpine grassland locations in the Oetztal Alps (Obergurgl, Soelden, Vent). Podzol soils; mean annual temperature around 3.2 °C (4.0 °C in 2019) and precipitation around 885 mm (1106 mm in 2019).
- Broadscale experiment (2017): three vegetation treatments on 2 m × 2 m plots within 9 blocks per site; treatments are shrub-invaded, grass-control, and shrub removal. Initially 81 plots; instrument failures reduced usable plots to 68 (n ≈ 21–24 per treatment).
- Vent snow/vegetation manipulation experiment: 48 plots in 8 blocks; fully crossed with three vegetation treatments and two snow treatments (snow removal vs snow cover) to disentangle effects on soil microbial communities and N cycling.
- Plot spacing: at least 1 m apart; shrub removal performed by removing whole plants/roots where feasible; no significant shrub regrowth observed.

## Field Sampling and Sample Handling
- Soil sampling: 22–24 July 2019; 5 random cores per plot (2 cm diameter × 10 cm depth); cores pooled per plot; vegetation removed; subsamples taken for molecular analyses and preserved in DNA/RNA shield solution.
- Immediate field lysis and subsequent storage: lysed in field, stored at -80 °C, shipped to CEH (UK) for molecular analyses; additional soil subsamples stored at 4 °C for biogeochemical analyses.
- Measurements accompany sampling: vegetation surveys and site aspect/slopes recorded.

## Biogeochemical Cycling and Microbial Biomass
- Inorganic N and DON: NH4+-N, NO3--N, DON quantified from extractions (1 M KCl for inorganic N; water for DON) using a segmented flow analyser.
- Mineralisation: 14-day incubation at 25 °C to determine net NH4+-N and NO3--N mineralisation.
- Dissolved organic carbon (DOC) and soil pH measured; gravimetric soil moisture and bulk density determined for stock calculations.
- Microbial biomass C and N: chloroform-fumigation method with 0.5 M K2SO4 extractions; corrections with KEC and KEN factors applied.
- Stock calculations: soil total C and N determined by elemental analysis; stocks derived from C or N percentages and bulk density.

## Soil Extracellular Enzyme Assays
- Eight enzymes assayed: GLC, CBH, XYL (cellulose/xylan degradation), NAG (chitin), PHO (phosphatase), URE (urease), POX and PER (phenol oxidase and peroxidase for lignin/polyphenol degradation).
- High-throughput colorimetric assays with substrate-specific p-nitrophenol or L-DOPA-based readouts; enzyme activities standardized per soil mass and corrected for background color.
- Activities also reported relative to microbial biomass C to reflect enzyme investment per unit microbial biomass.

## Soil Respiration
- CO2 flux measured in the Snow_Veg_manipulation experiment using a soil respiration chamber connected to an IRGA; measurements taken over 2 minutes per collar.

## PLFA Analyses (Soil Microbial Biomass)
- Phospholipid fatty acids used to infer microbial community structure (fungi, GP bacteria, GN bacteria, actinomycetes).
- Specific PLFA markers assigned to microbial groups; total PLFA and microbial biomass estimates computed; ratios (fungi/bacteria, GP/GN) calculated.

## DNA Extraction and Amplicon Sequencing
- DNA extracted with ZR soil microbe kit with additional lysis step; quality-filtered and stored at -20 °C prior to downstream analysis.
- Amplicon sequencing targets: 16S rRNA (bacteria) and ITS2 (fungi).
- 2-step Illumina PCR protocol used with barcoded Illumina adapters; libraries normalized and sequenced on MiSeq (V3 chemistry).
- Sequence processing: DADA2 in R for quality filtering, dereplication, chimera removal, and ASV generation; taxonomic assignment against Greengenes (16S) and UNITE (ITS).
- Data volumes: broadscale ~1.94 million bacterial and ~1.08 million fungal reads post-filtering; manipulative ~1.38 million bacterial and ~0.59 million fungal reads; rarefaction depths specified per dataset.
- Data normalization: rarefaction performed to even depths to facilitate downstream comparisons.

## Data Structure and Accessibility
- Broadscale data files:
  - Broadscale_Soil_micro_env.csv: metadata and abiotic/biogeochemical/PLFA/enzyme data per plot (over multiple soil parameters, pH, moisture, N forms, DON, TOC, microbial biomass, etc.).
  - Broadscale_16S_seq_table and Broadscale_ITS_seq_table: OTU/ASV abundance tables by sample; cross-referenced via plot_ID to Broadscale_Soil_micro_env.csv.
  - Broadscale_16S_taxa and Broadscale_ITS_taxa: taxonomic information for OTUs/ASVs.
  - Snow_Veg_manipulation_Soil_micro_env.csv: metadata and analogous soil/biogeochemical/biomass/enzyme/respiration data for the snow-vegetation manipulation experiment.
  - Snow_Veg_manipulation_16S_seq_table and Snow_Veg_manipulation_ITS_seq_table: sequencing data for the manipulative experiment, with cross-linking to Snow_Veg_manipulation_Soil_micro_env.csv.
  - Snow_Veg_manipulation_16S_taxa and Snow_Veg_manipulation_ITS_taxa: taxonomic details for the manipulative dataset.
- Data provenance: raw sequencing data deposited or staged for deposition at the European Nucleotide Archive (ENA); metadata fields documented to enable data discovery and cross-linking.
- Documentation: explicit metadata fields described (plot_ID, date, site, location, vegetation treatment, coordinates, elevation, soil chemistry, moisture, respiration, enzyme activities, PLFA biomarkers, microbial biomass, and sequencing sample IDs).

## Data Quality, Provenance, and Reuse
- Comprehensive protocols documented for field sampling, preservation, processing, and each analytical assay (biogeochemistry, enzymes, PLFA, respiration, DNA extraction, sequencing, and data processing).
- Data are organized to support cross-site and cross-treatment analyses, with explicit cross-references between environmental data and molecular data via sample/plot identifiers.
- Sequencing data have established processing pipelines (DADA2) and taxonomic references; depth normalization (rarefaction) applied to ensure comparability.
- Raw sequence data deposition forthcoming at ENA; study funded by NERC with multiple institutional collaborators; field access and acknowledgments noted.

## Access, Use, and Governance
- Data are structured to enable reuse for comparative analyses of soil microbiomes, enzyme activities, and biogeochemical cycling under shrub expansion and snow/vegetation manipulations.
- Data products include both abiotic/biogeochemical metadata and derived microbial community data (ASVs/OTUs, PLFA, enzyme activities) suitable for integration with broader environmental data repositories and cross-study syntheses.
- Researchers seeking data may reference the Environmental Information Data Centre repository entry and ENA submissions; detailed metadata supports traceability and reproducibility.

## Acknowledgements and References
- Funded by UK Natural Environment Research Council (NERC NE/N009452/1); additional support and fellowships acknowledged.
- Fieldwork and collaboration across Alpine Research Center Obergurgl and partner ski resorts; gratitude extended to field teams and access coordinators.