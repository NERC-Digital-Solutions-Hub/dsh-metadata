# Soil Organic Carbon Dynamics (SOC-D) data description

- Five long-term grassland-to-woodland contrasts across England (Gisburn-1, Gisburn-2, Alice Holt, Wytham Woods, Kielder Forest)
- Timeframe: measurements collected 2018–2021 (with ANPP and litter depth in 2021; core sampling 2018–2019)
- Aim: understand physical, chemical, and biological controls on soil organic carbon (SOC) dynamics; identify areas/conditions at risk of SOC loss; inform land management to enhance SOC storage; develop process-based SOC models for national-scale application

## Study design and sites

- Each site contains two plots (grassland vs woodland) with nine sampling locations per plot (total n ≈ 18 per contrast)
- Layout includes three grids per plot (grassland grids 1–3; woodland grids 4–6) and a predefined boundary between grids 3 and 4
- Transect-based sampling to capture proximity effects of trees on soils; randomized sampling points within grids; location data linked via GPS
- Site descriptions emphasize contrasting vegetation and management histories to test SOC sensitivity to climate and land use

## Datasets and data structure (key components)

- Datasets (four main content groups):
  - Aboveground and litter measurements: Aboveground Net Primary Productivity (ANPP) and litter layer depth
  - Soil properties (0–100 cm; up to six depth increments): common metrics (pH, EC, BD, LOI, TOC, TN, P, Nitrates, DOC, CEC, etc.) plus selective deeper/biogeochemical measurements
  - Soil hydraulic properties: soil water release curves (HYPROP) and unsaturated hydraulic conductivity (K) from field mini-disk infiltrometer tests
  - Earthworm counts and species IDs
- Data files and linking structure:
  - SOC-D_DATABASE_CONNECTOR.csv: links site, land-use, plot, grid, core, and sample metadata (14 columns; 458 rows)
  - SOC-D_DATABASE_LOCATIONS.csv: location-level coordinates and references (6 columns; 91 rows)
  - ANPP and litter depth files: SOC-D_DATABASE_ANPP.csv and SOC-DATABASE_LITTER_DEPTH.csv (location-level ANPP estimates and litter depth means)
  - Soil metrics (common and grid-specific): SOC-DATABASE_COMMON_SOIL_METRICS.csv; SOC-DATABASE_SOIL_METRICS_GRID2_GRID5.csv
  - Soil hydraulic data: SOC_D_DATABASE_SOIL_HYDRAULIC_CONDUCTIVITY.csv; HYPROP raw and related HYPROP conductivity datasets (HYPROP_RETENTION_T_PF.csv, HYPROP_CONDUCTIVITY_K_PF.csv, HYPROP_CONDUCTIVITY_K_T.csv)
  - Earthworms: SOC-DATABASE_EARTHWORMS.csv
  - Topsoil vs subsoil soil metrics: SOC-DATABASE_SOIL_METRICS_TOP_AND_SUB_SOIL.csv
- Biological data (ancillary): microbial community sequencing (16S rRNA and ITS marker genes) and metagenomes; derived metrics (ordination axes, gene counts) provided; sequencing data deposited in ENA under PRJEB66294
- Depths and sampling:
  - Core depths and slices: 0–5, 5–15, 15–30, 30–50/60, 50/60–100 cm (five depth increments; some sites used slightly different top-layer definitions)
  - Topsoil focus: 0–15 cm (or 0–5 cm for some sites) to align with UK national datasets; deeper segments for SOC-D questions

## Data collection and processing methods (highlights)

- Aboveground productivity and litter
  - ANPP estimated from cover-weighted leaf dry matter content (LDMC) across dominant species (locations in grids 2 and 5)
  - LDMC-based ANPP prediction using regression model; uncertainty propagated with Bayesian methods
- Soil core sampling and analyses
  - Pre-field planning to select homogeneous areas; sampling within each grid; 5–9 points per grid
  - Core types used:
    - Hyprop cores: 0–5 cm (and 30–35 cm at some sites) for hydraulic release curves
    - National survey style cores: 0–15 cm for topsoil carbon and compaction effects
    - Split Tube Sampler: 0–30 cm
    - Cobra precision corer: 0–100 cm (or 30–100 cm in deeper layers)
    - Russian Auger: 0–50 cm and 50–100 cm for deep sampling
  - Soil processing: homogenization, litter removal, segmenting into five depth increments for analyses
- Soil hydraulic and moisture measurements
  - HYPROP used to derive water retention curves and hydraulic properties; HYPROP-FIT software for curve fitting
  - Unsaturated hydraulic conductivity measured in the field with mini-disk infiltrometers at low and high suction ranges
- Soil chemical and physical properties
  - LOI and LOI-derived soil organic matter; LOI quality checks with internal standards
  - Bulk density determined from 1-m cores
  - pH (DIW and CaCl2), EC (suspension method with standards), and BD calculations
  - Total C and N (Vario EL) with UKAS QA; total P (H2O2/H2SO4 digestion) with colorimetric detection
  - Nitrate-N and DOC measured by standard extraction and colorimetric/TOC methods
  - CEC determined via ammonium acetate extraction and ICP-OES for major cations (Ca, Mg, K, Na)
- Soil texture, aggregates, and SOM fractions
  - PSD by laser diffraction after OM removal; ASD by laser diffraction to describe aggregate size distribution
  - SOM density fractionation into four fractions (DOC, LP-fraction, OP-fraction, MA-fraction) with SPT density separation; carbon and nitrogen quantified by elemental analyzer
  - Extracellular enzyme activities (β-glucosidase, N-acetylglucosaminidase, leucine aminopeptidase, phosphatase, phenol oxidase) measured on selected sites
- Microbial ecology
  - DNA extraction from 0.2–2.5 g samples; amplicon sequencing (16S rRNA V4-V5; ITS2) and metagenomics
  - Data processed to derive OTU counts and relative abundances; ordination metrics and fungal/bacterial ratios provided
- Data quality and QA
  - Internal standards, replicates, blanks, and calibration checks across chemical analyses
  - QC notes for site-specific issues (e.g., buffer mismatches invalidating some enzyme datasets at Gisburn)
  - Certain measurements excluded or flagged due to process issues (e.g., microbial biomass affected by freezing)
- Supplementary materials
  - Supplement A: field site maps and sampling points
  - Supplement B: detailed coring and hole-depth information per site
  - Supplement C: measurement priorities and analytical considerations

## Project background and rationale

- SOC-D aims to test how biotic (soil biota) and abiotic (soil structure, chemistry, climate) controls regulate SOC dynamics
- Investigates where UK SOC stocks are most at risk and how land management could enhance SOC storage
- Emphasizes deep SOC (below 20 cm; potentially down to 100 cm) and the coupling between soil physics, chemistry, and biology
- Grassland-to-woodland contrasts chosen to:
  - Reflect anticipated woodland expansion and its effect on SOC
  - Address questions about when trees increase SOC and under what conditions across the UK

## Data completeness, challenges, and interpretation notes

- Completeness varies by measurement; some deep soil measures (HYPROP cores, certain biological/enzyme datasets) are not available at all sites
- Topsoil depth definitions differed slightly among sites (0–15 cm versus 0–5 cm for some samples) to balance material sufficiency and comparability with national datasets
- Some measurements were not collected (e.g., infiltration for certain grids) or not analysed (e.g., texture for organic samples); missing values are recorded as NA
- Site-specific issues noted (e.g., Gisburn core compaction affecting certain core types; enzyme buffers incorrect at Gisburn leading to data removal)
- Data are structured to allow linking across datasets via the CONNECTOR file; location metadata and coordinates provided to enable spatial analyses and integration with external datasets

## Context and access

- Funded by the UK Natural Environment Research Council under the UK-SCAPE programme NE/R016429/1
- Collaboration with Forest Research and access permissions at Alice Holt and Kielder Forest; Gisburn site described
- Data intended for integration with national soil datasets and models; suitable for policy-relevant analyses of SOC dynamics under current and future land-use scenarios

## References and related projects

- Key methodological and conceptual references cited (e.g., Smart et al. 2017 for LDMC-based ANPP, HYPROP manuals, standard soil chemistry methods)
- Related projects and data platforms: ELUM, GMEP, UGRASS, ERAMMP; ENA deposition PRJEB66294 for sequencing data