# Data describing population responses of wild bees to oilseed rape neonicotinoid seed treatments in Hungary, Germany and the UK

## Overview
- A dataset describing how three neonicotinoid seed treatments (clothianidin, thiamethoxam, and a fungicide-only control) affect two wild pollinators: Bombus terrestris (bumblebee) and Osmia bicornis (solitary bee).
- Conducted across 33 commercial oilseed rape sites in the UK, Hungary, and Germany during spring 2015.
- Combines biological responses (reproductive output, colony development, weights) with neonicotinoid residue measurements in pollen/nectar and landscape context around colonies.

## Study design and spatial context
- Sites and treatments
  - UK: 12 sites; Hungary: 12 sites; Germany: 9 sites.
  - Within each site, oilseed rape fields were arranged in blocks of three sites, randomly assigned to: clothianidin (CTD), thiamethoxam (TMX), or control (fungicide only).
- Temporal scope
  - Oilseed rape established Aug–Sep 2014; flowering Apr–Jun 2015; exposures and measurements conducted during 2015.
- Biological sampling structure
  - Bombus terrestris: 12 commercial colonies per site, clustered into four multi-hives; measurements based on multi-hive data due to colony expansion.
  - Osmia bicornis: 50 cocoons released per site with two artificial trap nests; post-flowering dissections to count reproductive cells.
- Spatial data collection for GIS
  - Landscape around each colony/trap nest within 1.5 km radius were digitised and classified into land-use parcels (crops, grassland, woodland, water, urban, etc.).
  - Landscape diversity quantified using Shannon–Weiner index.

## Data collected and measurements
- Population responses
  - Bombus terrestris: weight of multi-hives over time; counts of workers, drones, eggs, queen cells, and queens produced.
  - Osmia bicornis: counts of reproductive cells, larvae presence, and associated weights.
- Neonicotinoid residues
  - Concentrations of clothianidin, thiamethoxam, and imidacloprid in pollen and nectar (ng/g, w/w) from stored pots and worker pollen baskets.
  - Sampling timing aligned with nectar/pollen collection; some pollen/nectar samples absent if no bees were present at a given nest.
- Derived residue metrics
  - Median and maximum residues per site for each compound; combined metrics (NNI_median_raw, NNI_peak_raw) and corrected versions using LD50-based weighting to reflect relative acute toxicity across the three compounds.
  - LD50-based correction factors applied because species-specific wild pollinator LD50s were unavailable; honeybee LD50 values used as a proxy.
- Exposure and temporal context
  - Days of exposure (R1–R8) recorded for successive measurement points.
- Biological and environmental covariates
  - Pre-exposure colony weight and successive weights (Weight_R1 to Weight_R8).
  - Relative peak weight (difference between pre-exposure weight and peak during flowering).
  - Oilseed rape cover within 1.5 km and landscape diversity around colonies.

## Landscape context and GIS features
- Spatial data products
  - Discrete land parcels around each site categorized into land-use classes and used to compute landscape diversity (Shannon-Weiner index).
  - OSR_cover: percentage cover of oilseed rape within 1.5 km radius.
- Data infrastructure
  - Landscape and site data were created and managed in ArcGIS; enables map-based visualization of habitat context and pesticide exposure.

## Data structure and metadata
- Metadata files
  - bombus_sites.csv: site-level Bombus terrestris data including medians for multi-hive responses and residues, landscape metrics, and residue measurements.
  - osmia_sites.csv: site-level Osmia bicornis data including larval counts, nest counts, landscape metrics, and residue measurements.
  - osmia_residue.csv: residue data within Osmia bicornis reproductive cells (pollen/nectar within cells) across trap nests.
- Key fields and units (examples)
  - Country, site, block; treatment (C = control, CLT = clothianidin, TMX = thiamethoxam).
  - OSR_cover (%), landscape_div (dimensionless index).
  - Residues in pollen/nectar (ng/g w/w) for CTD, TMX, IMI (imidacloprid) with medians and peaks.
  - NNI_median_raw / NNI_peak_raw and NNI_median_corrected / NNI_peak_corrected (sum of three neonicotinoids; ng/g w/w).
  - Days_of_exposure_R1…R8 (days); pre_weight and Weight_R1…Weight_R8 (g); relative_peak_weight (g).
- Data quality notes
  - Limits of quantification (LoQ) and detection (LoD) provided; values below LoQ treated as half LoD.
  - Some pollen/nectar samples unavailable at sites without Osmia cells.
  - LD50-based corrections rely on honeybee values due to lack of species-specific wild pollinator LD50 data.

## Data quality, limitations, and provenance
- Experimental platform funded by CEH/NERC (Project NEC05829); platform support from Syngenta and Bayer CropScience.
- Residue analyses conducted with accredited LC-MS methods; QA/QC aligned with ISO standards referenced in the protocol.
- Some sites lacked pollen/nectar samples or Osmia cells, leading to gaps in residue or biological data for those locations.

## Potential GIS data products and use cases
- Spatial comparison of pollinator responses to seed treatments across countries.
- Map-based analysis of associations between OSR habitat cover, landscape diversity, and pollinator metrics (weights, colony development, cell production).
- Overlay of residue exposure surfaces with pollinator outcomes to identify hotspots of impact.
- Creation of interactive dashboards linking site-level treatments, residue concentrations, and population responses for policymakers, practitioners, and the public.