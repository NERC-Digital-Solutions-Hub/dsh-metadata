# Abundance of airborne pollen for nine grass species, measured by qPCR, UK, 2016-2017

## Overview
- Open data: Available under the Open Government Licence; provenance at the provided DOI.
- Citation requirement: Brennan, G.; Creer, S.; Griffith, G. (2020). Abundance of airborne pollen for nine grass species, measured by qPCR, UK, 2016-2017. NERC Environmental Information Data Centre.
- Purpose for GIS: A dataset of spatially and temporally resolved pollen abundance suitable for map-based analyses of grass pollen distribution in the UK.

## Data collection and methods
- Molecular method: Quantitative PCR (qPCR) on aerial pollen DNA using species-specific primers targeting ITS2; species include Anthoxanthum odoratum, Arrhenatherum elatius, Cynosurus cristatus, Dactylis glomerata, Lolium perenne, Phleum pratense, Poa pratensis, Alopecurus/Agrostis group, plus one non-discriminatory probe.
- Instrumentation: QuantStudio 6 Flex Real-Time qPCR; standard curves from Primer Design (2 to 2×10^5 copies/µl).
- Sampling device: Burkard Automatic Multi-Vial Cyclone Samplers; 16.5 L/min airflow; collection into 1.5 ml vials; targets aerial plant particles only.
- Site metadata: 13 sampling sites across the UK; coordinates provided in the data file; rooftop locations (4–6 floors) to sample from mixed air flow; sites chosen per Met Office Pollen Monitoring Network requirements.

## Sampling design and timing
- Coverage strategy: Sites spread across broad geographic areas to capture varied soils and land uses; aligned with Met Office seven-day pollen traps.
- Bangor exception: Bangor followed the same methodology but is not part of the Met Office network.

## Data processing and quality control
- Data exclusions: From 1,400 daily aerial samples, 1,210 were analyzed; exclusions due to rainwater contamination, qPCR efficiency outside 85–115%, high replicate variability, and atypical CT ranges (outside 10–38 cycles) to minimize false results.
- Data processing: qPCR results converted to copy-number abundances using standard curves; three technical replicates per sample; records include mean, SD, SE for copy numbers and CT values.
- Reproducibility controls: Positive and negative controls used to assess reliability.

## Data structure and metadata
- Primary data file: qPCR_copy_number_abundance_data_aerial_DNA.csv
- Table 1 descriptions: Headers include sample identifiers, site IDs, target species, task IDs, sampling windows (start/end dates, days pooled), year, standard-curve metrics (R^2, slope, intercept, efficiency), copy-number statistics (mean, SD, var, SE), CT statistics, collection dates, and geospatial coordinates (latitude, longitude). Also includes MaxPoaceaeConc and days since first sample.
- Randomization: DNA extractions randomized for Bangor samples; plate-level randomization for qPCR runs.

## Spatial and data quality considerations for GIS use
- Spatial data: 13 site coordinates; explicit dating for each pooled aerial sample; day-month and year-month fields for temporal alignment.
- Temporal context: Sampling seasons 2016 and 2017 with site-level date ranges; pollen counts linked to Met Office pollen data for temporal framing.
- Data quality flags: Exclusion criteria clearly documented (rain contamination, qPCR efficiency, replicate variability, and cycle thresholds).

## Licensing, access details and citation
- Access: Data available under Open Government Licence; DOI provided in the data record.
- Citation format: Include authors, year, dataset title, and DOI as listed above.