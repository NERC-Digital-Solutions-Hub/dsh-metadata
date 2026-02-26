# Soil Organic Carbon Dynamics (SOC-D) Data Description

## Overview
- Five grassland-to-woodland contrasts across England (Gisburn-1, Gisburn-2, Alice Holt, Wytham Woods, Kielder Forest) studied between 2018–2021.
- Aims: understand biotic/abiotic controls on soil organic carbon (SOC) dynamics, identify areas at risk of SOC loss, and test tools for testing scale and sensitivity of interactions across UK land-use combinations; develop a modular, process-based SOC model.
- Data are designed for GIS-ready map-based analysis and integration with climate, vegetation, and land-management layers.

## Study design and sites
- Grassland-to-woodland contrasts chosen to reflect anticipated woodland expansion and its varying SOC responses.
- Site layout per site: two plots (plot 1 = grassland, plot 2 = woodland) with grids 1–3 in grassland and 4–6 in woodland; nine sampling locations per plot (total 18 per site).
- Sampling transects capture edge effects and confounding factors (distance to trees, slope, proximity to roads or water).
- Five contrasts were sampled in detail and mapped (Gisburn-1, Gisburn-2, Alice Holt, Wytham Woods, Kielder Forest); data include GPS coordinates and OS grid references.

## Datasets and data structure
- Four main measurement datasets plus location linking:
  - ANPP and litter layer depth (vegetation and litter measurements at 0–5 cm or 0–15 cm/topsoil where applicable).
  - Soil physical, chemical, and biological properties (0–100 cm, up to six depth increments).
  - Soil hydraulic properties (HYPROP soil water release curves and unsaturated hydraulic conductivity; plus field K measurements).
  - Earthworm counts and species identification with biomass data.
- Two supporting location data files:
  - SOC-D_DATABASE_CONNECTOR.csv: links sample IDs to site, plot, grid, and sampling coordinates; includes transition and lateral distances and core slice information.
  - SOC-D_DATABASE_LOCATIONS.csv: location metadata with site IDs, grid references, and coordinates (OSGB, then lat/long).
- Site- and depth-specific datasets:
  - ANPP and LITTER_DEPTH files with location mappings.
  - COMMON_SOIL_METRICS: 0–1 m soil metrics for all depths across all sites.
  - SOIL_METRICS_GRID2_GRID5: depth-resolved metrics for grids 2 (grassland) and 5 (woodland).
  - HYDRAULIC_CURVE and HYPROP-related files: raw HYPROP data and derived K values (KFS) at specified tensions.
  - EARTHWORMS: counts, biomass, and species IDs by location.
- Data quality and completeness notes:
  - Completeness is high for common measurements (e.g., LOI, BD, pH, EC); some advanced or expensive measurements (e.g., certain enzymes, microbial biomass, some fractions) are incomplete or site-specific.
  - Missing values are marked as NA; some measurements were not collected at certain sites due to logistics or methodological issues.
  - Laboratory QC includes duplicates, blanks, and internal standards; some datasets had methodological adjustments or exclusions (e.g., Gisburn enzyme data removed due to incorrect buffer).

## Depths, measurements and methods
- Depth increments (typical, with site-specific adjustments):
  - Primary: 0–5 cm, 5–15 cm, 15–30 cm, 30–50/60 cm, 50/60–100 cm.
  - Gisburn sites: 0–5 cm and 15–60 cm (adjusted); other sites follow the standard increments.
- Key measurements by dataset:
  - ANPP: estimated from leaf dry matter content (LDMC) using cover-weighted LDMC; mean, high/low bounds provided.
  - Litter depth: measured at three points per sampling location.
  - HYPROP: soil water release curves (0–5 cm at most sites; 30–35 cm at some sites) and subsequent hydraulic conductivity from HYPROP and field mini-disk infiltrometer.
  - Earthworms: hand-sorted counts and biomass (laboratory processing and species IDs where available).
  - Soil chemistry and physics: EC, pH in DIW and CaCl2, bulk density, LOI, total C and N (Vario-EL), total P, NO3-N, DOC, CEC, exchangeable cations (Ca, Mg, K, Na); LOI by thermogravimetric analysis; PSD by laser diffraction; aggregate-size distribution; SOM density fractions (LP, OP, MA) plus dissolved organic carbon (DOC) and total N in fractions; enzyme activities (selected sites); microbial community analyses (16S rRNA and ITS sequencing; metagenomics).
  - SOC fractions and fractions-related metrics: LP-C, OP-C, MA-C and corresponding N contents; C:N ratios; enzyme-related metrics and microbial community ordination scores.
  - Microbial and enzymatic assays: beta-glucosidase, N-acetylglucosaminidase, leucine aminopeptidase, phosphatase, phenol oxidase; data limited to select sites due to buffers and storage constraints.
- Data processing and analysis:
  - ANPP modeled from LDMC with regression (Smart et al. 2017); uncertainties propagated via MCMC-based credible intervals.
  - HYPROP data analyzed with HYPROP-FIT software; derived parameters used to interpret soil hydraulic properties and pore structure.
  - Soil depth increments aligned with UK national monitoring depth ranges where possible (topsoil 0–15 cm split into two functional layers; deeper increments defined to balance material for analyses).
  - Microbial sequencing data processed with standard pipelines (DADA2 for OTU/ASV inference; metagenomic reads annotated with DIAMOND/SEED; ordination with vegan in R).

## GIS-relevant outputs and usage
- Spatial data readiness:
  - Precise sampling coordinates per location; OSGB references and geocoordinates available for mapping and spatial analyses.
  - Co-located data across multiple depth layers and fractions, enabling depth-resolved SOC mapping and visualization of SOC pools (LP, OP, MA) and DOC across sites.
  - Linkable via LOCATION_ID across ANPP, litter, soil metrics, HYPROP/K data, and earthworm datasets for integrated GIS visuals.
- Potential map products:
  - Depth-resolved SOC stocks and fractions by site and land-use contrast (grassland vs woodland).
  - Spatial patterns of ANPP proxies and litter depth across grids to explore vegetation-soil interactions.
  - Soil hydraulic properties and K across depth and space to assess hydrological responses to land-use change.
  - Earthworm distribution and biomass as a biotic proxy linked to soil structure and carbon dynamics.
  - Overlay capabilities with land-use maps, climate layers, and topography to identify regions with SOC vulnerability or high sequestration potential.

## Project context
- Part of UK-SCAPE (grant NE/R016429/1) with collaboration from UKCEH and Forest Research.
- Data accompany methodological supplements (Supplement A–C) detailing field procedures, coring logs, and measurement planning; references provided for analytical methods and data handling.
- Aims to feed into modular, process-based SOC models that can be embedded in broader community soil models and used to test management strategies for SOC storage.

## Practical notes for GIS work
- Use the connectors to join ANPP, litter, and soil metrics to location data for site- and grid-level maps.
- Employ depth-structured layers to create 3D SOC visuals or layered 2D maps by depth interval.
- Consider site-specific depth adjustments (e.g., Gisburn topsoil split versus standard increments) when aligning with national soil datasets.
- Leverage the ENA/ENA-like sequencing and metagenomics metrics to enrich maps with microbial context where appropriate, ensuring site-level comparisons account for data availability.
- Acknowledge data gaps and site-specific QC notes when designing analyses or publishing maps.