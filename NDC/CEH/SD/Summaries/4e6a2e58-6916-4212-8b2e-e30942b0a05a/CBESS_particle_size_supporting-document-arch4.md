# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) sediment particle size in mudflat and saltmarsh habitats

## Overview
- Dataset describing sediment particle size from Coastal biodiversity and Ecosystem Service Sustainability (CBESS).
- Coverage: 6 sites across 2 locations (Essex and Morecambe Bay), encompassing two habitats per site (mudflat and saltmarsh).
- Sampling design: data collected from winter and summer 2013, with 3 replicates across 22 quadrats at 4 spatial scales per habitat.
- Staff responsible: Christina Wood and Martin Solan.
- Purpose: supports analysis of sediment size distributions across habitats, sites, seasons, and spatial scales.

## Dataset scope and sampling design
- Locations and sites:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Habitat representation:
  - Each site includes both mudflat and saltmarsh habitats.
  - Saltmarsh sites exemplify contrasting soil types (clay in Essex; sandy in Morecambe Bay).
- Temporal coverage:
  - Winter and summer 2013 as part of the CBESS field campaign.
  - No planned repeat sampling.
- Data captured:
  - Sediment particle size measurements across multiple spatial scales and quadrats.

## Spatial and temporal coverage details
- Spatial scale and sampling grid:
  - 4 spatial scales: A (1 m), B (1–10 m), C (10–100 m), D (100 m to upper limit).
  - 22 quadrats per habitat per site, with 3 replicates.
- Coordinates and site descriptors:
  - Essex sites include precise latitude/longitude coordinates; Morecambe Bay sites have corresponding coordinates.
  - Habitat types and site names documented for cross-site comparability.

## Data collection, processing and protocols
- Field collection:
  - Mudflats: surface sediment scrapes.
  - Saltmarsh: sediment cut from 2 cm below the surface.
- Sample handling:
  - Samples frozen at -20°C prior to analysis.
- Measurement technique:
  - Particle size analysis following Malvern Mastersizer protocol.
  - Calibration and processing references provided via linked documentation.
- Documentation and references:
  - Links provided for methods, calibration, and quality control procedures.
  - Full article and related PSD (particle size distribution) references available (e.g., Gradistat).

## Dataset structure and fields
- Primary data format: CSV file(s).
- Key field groupings (represented in the dataset description):
  - Row Number: sort/identifier for original input order.
  - Season: Winter (W) or Summer (S).
  - Location: Morecambe (M) or Essex (E).
  - Site: CS, WS, WP (Morecambe); AH, FW (Essex); TM is also listed.
  - Habitat: Mudflat (MF) or Saltmarsh (SM).
  - Quadrat Number: 1–22.
  - Scale: A, B, C, D corresponding to 1 m, 1–10 m, 10–100 m, 100 m–upper limit.
  - Replicate: 1–3.
  - Measurement Type: PSA (particle size analysis).
  - Size distribution metrics (µm scale and phi scale):
    - d(0.050), d(0.160), d(0.5), d(0.840), d(0.950) – percentiles or equivalent statistics.
    - D [4,3] µm and inclusive mean (Phi) with associated statistics (kurtosis, standard deviation, skewness) in both phi and µm scales.
  - Clay fractions and silt/clay groupings:
    - %Clay across multiple size ranges, with phi-based buckets and corresponding µm ranges.
  - Meta-structure indicators:
    - Rawle (1992) referenced for particle size analysis principles.
- Notes on field descriptions:
  - Location, site and habitat codes (M/E, MF/SM) and scale definitions are explicitly defined to enable cross-site harmonization.
  - A comprehensive mapping of particle-size distribution statistics is provided, enabling multiple analytical approaches (percentiles, means, moments, and clay fractions).

## Quality control, calibration and data provenance
- Data collection and processing documentation:
  - Detailed procedures, calibration and quality-control references are provided via linked resources.
  - Procedures align with standard PSD analysis approaches and established literature (e.g., Gradistat).
- Data provenance:
  - Data produced by CBESS field campaign teams; staff acknowledged.
  - Descriptions include links to methodologies and full articles for reproducibility.

## Access, reuse and references
- File formats:
  - Primary dataset available as CSV.
  - Additional references include standardized PSD protocols and Gradistat methodology PDFs.
- Related materials:
  - Full article and external technique references accessible via provided links (e.g., Gradistat PDF, PSD method pages).
- Licensing and reuse notes:
  - Not specified in the extract; governance and licensing should be confirmed with data custodians if reuse is planned.

## Data governance and strategic implications for Data Leaders
- Rich, multi-dimensional data asset:
  - Combines cross-site, cross-habitat, and multi-season measurements with granular size-distribution metrics.
  - Supports cross-site benchmarking of sediment characteristics and their ecological implications.
- Metadata richness and discoverability:
  - Extensive field metadata and explicit definitions for locations, habitats, scales, and variables enhance discoverability and integration with other CBESS datasets.
- Data quality and sustainability considerations:
  - Explicit QC and calibration references improve trustworthiness, but no repeat sampling is planned, so use should account for static temporal coverage.
- Actionable steps for data leadership:
  - Ensure metadata harmonization across CBESS datasets to enable broader meta-analysis.
  - Verify licensing and access rights with custodians; consider persistent identifiers and comprehensive metadata to improve discoverability.
  - Leverage the dataset for cross-habitat and cross-site analyses of sediment size distributions, informing sediment dynamics, habitat suitability, and ecosystem service assessments.