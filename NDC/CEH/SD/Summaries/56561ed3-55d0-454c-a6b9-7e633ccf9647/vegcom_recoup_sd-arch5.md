# RECOUP-Moor Vegetation Community data: Methodology

## Overview
- Post-fire ecological study on Saddleworth Moor (Stalybridge estate), a blanket bog near Manchester, UK.
- Fire occurred June 24, 2018, affecting 18 km2 and removing surface vegetation; study tracks post-fire recovery and seed-bank dynamics.
- Data collected include vegetation surveys and soil seed-bank samples across plots with varying burn severities, plus a nearby unburned reference site.
- Methodology defines data collection, storage, processing, and metadata structure to support future discovery and reuse.

## Study design and sampling
- Site and treatments:
  - 10 plots (10 m x 10 m) established in October 2018 at the post-fire site.
  - 5 plots in shallower burn areas (S1–S5) and 5 plots in deeper burn areas (D1–D5); a reference unburned area (R1–R5) within 2 km.
  - Post-fire surface vegetation removed, exposing bare peat.
- Vegetation surveys:
  - 1 m x 1 m point quadrats with 1 cm interval sampling.
  - Two surveys per plot at random positions; results combined to yield one vegetation community per plot per survey time.
- Timeframe and processing:
  - Sampling across post-fire conditions with subsequent data processing to derive community composition.

## Seed-bank sampling and treatment
- Soil sampling:
  - Peat samples collected from three random locations per plot.
  - Each sample comprises two depth layers: 0–5 cm (top) and 5–10 cm (bottom); three samples per plot aggregated to one soil sample per plot per depth.
  - Reference site sampled with identical procedure (n=5).
- Seed-bank processing:
  - Samples transported to University of Southampton; stored at ~5°C for 21 days, then frost-treated at -20°C for 48 hours.
  - Seeds germinated in greenhouse with approximately 1 L of horticultural peat; seedlings identified and removed; process continued for 12 weeks until no new seedlings emerged.
  - Seed-bank abundance values adjusted to 1 L of extracted peat soil; this standardizes seed-bank data while vegetation abundances remain unadjusted.
- Data handling:
  - Post-processing step accounts for initial soil weight differences; final seed-bank data reflect per-liter soil basis.

## Variable structure and data keys
- Plot and sample identifiers:
  - Plot_number/Plot_ID to distinguish plots and replicates (S1–S5 shallow burn, D1–D5 deep burn, R1–R5 reference).
- Data categories:
  - Survey Descriptions: Veg (vegetation surveys) or SB (seed-bank surveys).
  - Soil_layer: Top (T) or Bottom (B) for seed-bank samples.
  - Sample_group: Reference or Post-Fire.
- Measurements and metadata:
  - Weight_soil: weight of extracted peat soil (seed-bank only).
  - Date: sampling date.
  - Species_Latin: Latin species name; Abundance: total individuals per sample.
  - Seed-bank vs Vegetation: Seed-bank values, Abundance are seed-bank specific; Raw_Abundance indicates raw counts per sample (seed-bank abundances not standardized by weight).
- Data standardization:
  - Seed-bank values standardized to 1 L of extracted soil; vegetation abundances left as raw counts.
  - Clear documentation of which data are standardized and which are not.

## Species coverage
- Curated species list with both Latin nomenclature and common names, including:
  - Betula pubescens (Moor birch)
  - Calluna vulgaris (Common heather)
  - Epilobium angustifolium (Rosebay willowherb/Fireweed)
  - Epilobium hirsutum (Great willowherb)
  - Erica tetralix (Bog heather)
  - Eriophorum vaginatum (Hare's-tail cottongrass)
  - Festuca rubra (Red fescue)
  - Holcus lanatus (Yorkshire fog)
  - Juncus bufonius (Toad rush)
  - Juncus effusus (Soft rush)
  - Rumex acetosa (Common sorrel)
  - Vaccinium myrtillus (European blueberry)

## Data governance and reuse considerations
- Metadata-rich design supports discoverability and informed reuse by data users and downstream analyses.
- Explicit separation of seed-bank and vegetation data, including sampling methods, depths, and units, facilitates interoperability across systems.
- Documentation of burn severity, reference site, sampling times, and processing steps supports transparency and reproducibility.
- Data are prepared for upload to data portals and catalogues, with clear data provenance and processing workflows embedded in the methodology.