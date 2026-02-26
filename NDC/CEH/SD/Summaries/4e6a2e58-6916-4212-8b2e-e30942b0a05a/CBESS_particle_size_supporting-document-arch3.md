# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) sediment particle size in mudflat and saltmarsh habitats.

## Overview
- Dataset documenting sediment particle size distributions in mudflat and saltmarsh habitats as part of the CBESS program.
- Data collection across 6 sites at 2 locations (Essex and Morecambe Bay) during winter and summer 2013.
- 3 replicates across 22 quadrats, spanning 4 spatial scales.
- Staff responsible: Christina Wood and Martin Solan.

## Study design and locations
- Locations representing contrasting habitat types and sediment characteristics:
  - Essex: Abbotts Hall (AH) and Fingringhoe Wick (FW); cohesive clays, mud, and silt in mudflats; clay soils for saltmarsh.
  - Morecambe Bay: Cartmel Sands (CS) and Warton Sands (WS); saltmarsh with sandy soils; mudflats with coarse, mobile sediments.
- Saltmarsh regions differ in inundation frequency, creek structure, and vegetation.
- Mudflat habitats differ between sites (Essex vs. Morecambe Bay) in sediment composition.

## Monitoring and sampling methods
- Sampling periods: winter and summer 2013; no planned repeat sampling.
- Mudflat sampling: surface sediment scrapes.
- Saltmarsh sampling: sediment collected from 2 cm below the surface.
- Sample handling: all samples frozen at -20°C prior to analysis.
- Analysis method: particle size analyzed using the Malvern Mastersizer protocol; full details and calibration references provided via linked methods pages.
- Data quality and procedures:
  - Quality control and calibration references available (links provided in the dataset metadata).
  - Data are formatted and described for reproducibility, with procedures and checks outlined.

## Data structure and key fields
- Core dataset fields:
  - Row Number, Season (Winter = W, Summer = S), Location (Morecambe = M, Essex = E), Site (CS, WS, WP; AH, FW), Habitat (Mudflat MF, Saltmarsh SM), Quadrat Number (1–22), Scale (A–D; various spatial extents), Replicate (1–3), Measurement Type (PSA = Particle Size Analysis).
- Primary observational variables:
  - Particle size distribution metrics: d(0.050), d(0.160), d(0.5), d(0.840), d(0.950) in micrometers.
  - D[4,3] and inclusive mean (Phi) values.
  - Inclusive kurtosis, inclusive standard deviation, inclusive skewness (both Phi and µm units).
  - Percent clay metrics across a range of phi-size bins (e.g., %Clay 0.021–0.03 µm to %Clay 1.38–1.95 µm, and similar fractions for larger size classes).
  - Percent finer fractions such as <63.000 µm, and successive clay/silt/sand fractions across detailed size ranges.
- Miscellaneous metadata:
  - Raw data references and unit definitions; guidance on equation sources and formatting (e.g., phi-scale conversions, methodology references).
  - Data format: CSV.
- Data provenance and references:
  - Observational and analytical procedures aligned with Blott & Pye (2001) and related PSD literature.
  - Full methodological details and calibration information accessible via linked URLs in the dataset metadata.

## Data quality, governance, and accessibility
- Metadata-rich dataset designed to support verification and reuse:
  - Detailed field descriptions and measurement definitions enable cross-site comparability.
  - Clear data formats and provenance facilitate integration into monitoring frameworks.
- Data handling considerations:
  - Procedures for data cleaning, transformation, and QA are described, with external references for the analytical protocol.
  - Some links point to external facilities pages for detailed technique descriptions and calibration standards.
- Public sharing and openness:
  - The dataset is structured to support open sharing of underlying data, aligning with data governance and transparency requirements common in monitoring frameworks.
  - The metadata includes references and links to ensure traceability of methods and units.

## Relevance for monitoring frameworks
- Demonstrates a robust, multi-site, multi-habitat approach to environmental health monitoring:
  - Captures spatial and temporal variation (multiple sites, two habitats, two seasons).
  - Uses standardized measurement techniques with comprehensive metadata to enable comparability and longitudinal assessment.
- Aligns with common monitoring framework challenges:
  - Addresses data availability and standardization by providing detailed field definitions, sampling design, and measurement protocols.
  - Supports data governance through explicit QA expectations, data format specifications, and provenance.
  - Illustrates how to communicate complex sedimentological findings via structured, repeatable metrics (particle size distributions, clay content fractions, and derived statistics).
- Provides a template for integrating similar environmental health datasets into dashboards, reports, and governance processes.