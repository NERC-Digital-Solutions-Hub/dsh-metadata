# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) sediment particle size in mudflat and saltmarsh habitats

- A dataset of sediment particle size analyzed from six sites across two locations (Essex and Morecambe Bay), collected during winter and summer 2013 as part of the CBESS field campaign.
- Sampling involved three replicates across 22 quadrats at four spatial scales, covering both mudflat and saltmarsh habitats.
- Staff responsible: Christina Wood and Martin Solan.

## Spatial and temporal coverage

- Locations:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS)
- Coordinates:
  - Essex: AH 51.7833°N, 0.8667°E; FW 51.8167°N, 0.9667°E; TM 51.6833°N, 0.9333°E
  - Morecambe Bay: CS 54.1667°N, 3.0000°W; WS 54.1333°N, 2.8000°W
- Habitats: Mudflat (MF) and Saltmarsh (SM)
- Habitat contrasts: Essex saltmarsh with clay soils; Morecambe Bay saltmarsh with sandy soils; differences in inundation frequency, creek structure, and dominant vegetation.
- Sampling period: Winter and Summer 2013
- Coverage notes: No planned repeat sampling.

## Data collection and methodology

- Measurement focus: Sediment particle size (PSA) analysis.
- Sampling methods:
  - Mudflats: surface sediment scrapes
  - Saltmarsh: sediment collected from 2 cm below surface
- Sample handling: samples frozen at −20°C; analyzed using Malvern Mastersizer particle size protocol.
- Calibration and quality: references and procedures linked to external resources (calibration and QA procedures available online).
- Data format: CSV files (and associated metadata), with source citations including Blott & Pye (2001) and related PS distribution references.
- Full article/metadata: Additional details and context available via linked sources (e.g., CBESS outputs and technique pages).

## Dataset schema and key variables

- Core variable: Sediment particle size distribution
- Common fields (examples):
  - Row Number: sorting index
  - Season: Winter (W) or Summer (S)
  - Location: Morecambe (M) or Essex (E)
  - Site: Morecambe CS, WS; Essex AH, FW
  - Habitat: Mudflat (MF) or Saltmarsh (SM)
  - Quadrat Number: 1–22
  - Scale: A (1 m), B (1–10 m), C (10–100 m), D (100 m to upper limit)
  - Replicate: 1–3
  - Measurement Type: PSA
  - d(0.050) µm: 5th percentile
  - d(0.160) µm: 16th percentile
  - d(0.5) µm: 50th percentile (median)
  - d(0.840) µm: 84th percentile
  - d(0.950) µm: 95th percentile
  - D[4,3] µm: De Broucker/mean equivalent spherical volume
  - Phi-scale metrics: inclusive mean, inclusive kurtosis, inclusive standard deviation, inclusive skewness
  - Phi-based clay fractions and size classes: %Clay and various size fractions from clay (<63 µm) to very coarse sands (up to ~2000 µm)
- Notes: The dataset includes detailed size distribution metrics across multiple percentiles and derived statistics, with some fields described via equations or external methodology references.

## Data formats, access, and provenance

- Primary format: CSV
- Additional references: calibration, QA, and PSD method pages; full article with background information
- Data provenance: field-collected measurements from six sites across two regions, processed per Malvern Mastersizer protocol; linked to CBESS materials and related literature

## Data quality, limitations, and stewardship

- Temporal limitation: single field campaigns in 2013 (winter and summer) with no planned repeats
- Spatial limitation: six sites across two regions; may affect broad-scale extrapolation
- Data quality indicators: QA procedures and calibration references available online
- Data standardization: dataset includes a comprehensive set of metrics, but users should be aware of multiple scales and habitat contexts when integrating with other GIS layers

## GIS usage and visualization guidance

- Potential map layers:
  - Site locations with coordinates and habitat type (mudflat vs saltmarsh)
  - Scale polygons or buffers representing sampling extents (A–D)
  - Quadrats (1–22) within each site/habitat for fine-grained mapping
- Attribute usage:
  - Use particle size distribution metrics (percentiles, D[4,3], inclusive mean, etc.) as raster/vector attributes linked to quadrats or sites
  - Create derived layers for habitat type (esx clay vs sand), inundation context, and vegetation type to support spatial analyses
- Temporal aspects:
  - Separate seasonal analyses (Winter vs Summer 2013) within GIS to explore temporal changes in sediment characteristics
- Integration opportunities:
  - Combine with other CBESS data layers (biodiversity, ecosystem services) to assess spatial relationships between sediment properties and ecological indicators
- Data preparation tips:
  - Import CSV with explicit geographic coordinates for site centroids or quadrat centroids
  - Maintain clear join keys: Site, Habitat, Quadrat Number, Season
  - Normalize scale categories (A, B, C, D) for consistent mapping

## Contact and provenance

- Responsible researchers: Christina Wood and Martin Solan
- Data sources and references: CBESS project materials; Malvern Mastersizer protocol; cited literature (e.g., Blott & Pye 2001)
- Full article and technique references available via linked sources in the dataset metadata