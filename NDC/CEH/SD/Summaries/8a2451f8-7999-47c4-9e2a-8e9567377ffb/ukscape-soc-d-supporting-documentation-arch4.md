# Data description

- What and scope
  - Co-located aboveground and belowground measurements were recorded at five long-term grassland-to-woodland contrasts across England (2018–2021): Gisburn-1, Gisburn-2, Alice Holt, Wytham Woods, and Kielder Forest.
  - Four main datasets are provided (plus ancillary connectors): Aboveground net primary productivity (ANPP) and litter layer depth; soil chemical, physical, and biological properties for up to six depth increments (0–100 cm); soil hydraulic conditions (water release curves and unsaturated hydraulic conductivity); and earthworm counts and species IDs. In addition, extensive soil microbial data (amplicon sequencing for bacteria and fungi, plus metagenomes) are included.
  - Datasets are complemented by two connector/location files to enable linking across measurements. Raw microbial sequences are deposited in ENA (PRJEB66294).

- Project purpose and background
  - SOC-D (Soil Organic Carbon Dynamics) aims to understand biotic and abiotic controls on SOC, identify where UK soil carbon stocks are at risk, and identify opportunities to increase SOC via land management.
  - Key questions address SOC sensitivity to climate/land management, feedbacks with soil structure and biota, best metrics and modeling approaches for SOC dynamics, and UK regions at risk of SOC loss.

- Study design and sampling framework
  - Grassland-to-woodland contrasts chosen to explore SOC responses to planned woodland expansion and varying site conditions.
  - Each site includes two plots (grassland vs woodland) with grids 1–3 in grassland and 4–6 in woodland; nine sampling locations per plot (18 per contrast). Sampling locations within grids were randomized; GPS and a pre-defined sampling matrix captured distance to the contrast boundary and lateral distances.
  - Depths and soil layers sampled:
    - Common core scheme: 0–5 cm, 5–15 cm, 15–30 cm, 30–50/60 cm, 50/60–100 cm (variable by site; some sites use 0–15 cm topsoil split differently).
    - In some sites, topsoil was treated as 0–5 cm and 15–50/60 cm to align with national datasets.
  - Site details:
    - Gisburn-1: grazed grassland x conifer
    - Gisburn-2: ungrazed grassland x broadleaf
    - Alice Holt: grazed grassland x broadleaf
    - Wytham Woods: grazed grassland x broadleaf
    - Kielder Forest: unmanaged grassland x conifer

- Data collection and measurement methods
  - Aboveground productivity and litter
    - ANPP estimated from fresh leaf material collected in grids 2 (grassland) and 5 (woodland) in 2021; leaf dry matter content (LDMC) used as predictor via a regression model to produce mean ANPP with uncertainty (credible intervals).
    - Litter layer depth measured at three locations around each sampling point.
  - Soil physical, chemical, and biological properties (0–100 cm)
    - Core sampling and processing across five soil depth increments; a suite of common measurements (e.g., LOI, bulk density, pH, EC) and selective measurements (e.g., DOC, nitrate, CEC, base cations, enzymes) with site-specific limitations noted.
    - Detailed soil depth increments and lab workflows align with UK national datasets (Countryside Survey, GMEP, ERAMMP, UK-SCAPE LUCAS data).
  - Soil hydraulic properties
    - HYPROP-based soil water release curves (pF) and unsaturated hydraulic conductivity (K) using mini-disk infiltrometers for grids 2 and 5.
    - HYPROP data analyzed with HYPROP-FIT software; additional WP4 measurements for high-suction ranges.
  - Deep soil cores and sampling devices
    - Core types include Hyprop cores, national survey style cores, Split Tube samplers, Cobra precision corers, and Russian augers, used to obtain 0–100 cm profiles and ensure core integrity (with cautions about compaction and hole depth).
  - Earthworms
    - Hand-sorted earthworm sampling: excavation to 25 cm depth per sampling point, with standardized sorting time; specimens weighed and identified to species in lab.
  - Microbial communities and functional genes
    - Topsoil and subsoil DNA extracted for amplicon sequencing (16S rRNA for bacteria, ITS2 for fungi) and metagenomic sequencing for functional genes.
    - Data processing includes DADA2 for OTU inference, DIAMOND/ SAMSA2 for metagenomic annotation, and ordination analyses (e.g., NMDS). Fungal-to-bacteria ratios derived from taxonomic annotations.
  - Additional soil chemistry (derived and ancillary)
    - Total carbon and nitrogen by elemental analyzer; total phosphorus via acid digestion and colorimetric measurement; NO3–N and DOC in mineral soils; CEC via ammonium acetate extraction and ICP-OES; pH (DIW and CaCl2), EC, LOI via TGA; PSD via laser diffraction (Beckman Coulter LS13 320) with aggregate size distribution data; SOM density fractionation into LP, OP, MA fractions plus DOC, with LP/OP/MA C and N contents and C:N ratios; enzyme activities for select sites; additional soil metrics including enzyme ratios and microbial indicators.
  - Data quality control
    - Internal standards and duplicates used for EC, pH, and LOI; batch-level QC for instrument calibration; internal references and replicates for several measurements; some site-specific issues noted (e.g., wrong buffer used for some enzyme assays at Gisburn, microbial biomass affected by freezing).

- Data structure, connectivities, and access
  - Data are organized with multiple CSV files and two linking files:
    - SOC-D_DATABASE_CONNECTOR.csv: links site, plot, grid, core, and sample metadata (e.g., transition distance, lateral distance, slice, lab layer, location IDs).
    - SOC-D_DATABASE_LOCATIONS.csv: contains location-specific coordinates and OS grid references.
  - Datasets available (examples)
    - ANPP and LITTER_DEPTH: site- and grid-level ANPP estimates; litter depth means.
    - COMMON_SOIL_METRICS.csv: field- and lab-measured soil metrics aligned to 0–100 cm slices (SAMPLE_ID linkage).
    - SOIL_METRICS_GRID2_GRID5.csv: grid-specific soil metrics (top 5 depth increments) including CEC, Ca, Mg, NO3-N, DOC, etc.
    - SOIL_HYDRAULIC_CONDUCTIVITY.csv and HYPROP-related files: KFS, PF, and log10(K) values and raw HYPROP data.
    - EARTHWORMS.csv: earthworm counts and fresh biomass by species.
    - ENA raw sequencing data: accessible under project PRJEB66294; derived metrics provided in dataset files.
  - Connectivity and location
    - Each sample has a SAMPLE_ID; location-level data connect via LOCATION_ID; the location file includes latitude/longitude and OS grid references for mapping.
  - Missing data
    - NA values indicate samples not collected or analyses not performed; some site-level data were excluded due to methodological issues (e.g., Gisburn enzyme data).

- Supplementary materials and project context
  - Supplement A: field-sheet visualizations and Google Earth mapping of grassland/woodland contrasts.
  - Supplement B: detailed soil coring information by site and core type.
  - Supplement C: measurement prioritization, rationale, and analysis plans for additional ecosystem measurements.
  - Project funding and collaboration
    - UK-SCAPE programme funded by the Natural Environment Research Council (award NE/R016429/1).
    - Acknowledgments to Forest Research for access and collaboration.

- Related project links
  - ELUM, GMEP, UGRASS, ERAMMP project pages for context and integration with broader ecosystem and soil C-flux modeling initiatives.