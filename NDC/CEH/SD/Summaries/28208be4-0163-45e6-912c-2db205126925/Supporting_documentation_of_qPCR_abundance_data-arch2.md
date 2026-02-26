# Abundance of airborne pollen for nine grass species, measured by qPCR, UK, 2016-2017

- Purpose and scope
  - Presents data on airborne pollen abundance for nine grass species in the UK, measured by quantitative PCR (qPCR) during 2016–2017.
  - Aims to provide a standardized, auditable dataset for environmental health monitoring, enabling assessment of grass pollen abundance over time.

- Data access and licensing
  - Open Government Licence.
  - Dataset available at the stated DOI; primary citation: Brennan, G.; Creer, S.; Griffith, G. (2020). Abundance of airborne pollen for nine grass species, measured by qPCR, UK, 2016-2017. NERC Environmental Information Data Centre.
  - Data usage requires attribution to the cited dataset.

- Data collection (methods)
  - Molecular method: qPCR on DNA extracted from aerial particles using primers targeting the ITS2 region for abundant UK grass species (nine targets) plus one degenerate probe unable to discriminate species.
  - Instrumentation: QuantStudio 6 Flex Real-Time qPCR; copy-number standards provided by Primer Design (range 2 to 2×10^5 copies/µl).
  - Air sampling: Burkard Automatic Multi-Vial Cyclone Samplers (16.5 L/min) on exposed rooftops (4–6 storeys) to sample from mixed air flow; seven-day volumetric trap data used for pollen counts.
  - Study sites: 13 locations across the UK, aligned with the Met Office UK Pollen Monitoring Network (Bangor included as a non-network site in this study).

- Timing and location
  - Sampling seasons: 2016 (May 25 – Aug 28) and 2017 (May 5 – Sept 10), with slight site-by-site date variations.
  - Sampling locations: 13 sites across the UK with precise latitude/longitude recorded; sites chosen to cover broad geographic and land-use variation.

- Data processing and analysis
  - Data processing: qPCR data analyzed with QuantStudio Software V1.3; copy numbers calculated using standard curves.
  - Quality controls: Only samples with acceptable qPCR efficiency (85–115%), replicate consistency (SD within replicates, specifically ≤6.95 upper quartile-based threshold), and appropriate amplification cycles (Ct between 10 and 38) were retained.

- Data exclusions and quality assurance
  - From 1,400 daily aerial samples, 1,210 were retained after removing samples with excessive rainwater contamination or poor qPCR performance.
  - Reproducibility checked using positive and negative controls; randomization of DNA extractions and plate layouts to mitigate bias.

- Randomization and reproducibility
  - DNA extractions randomized for Bangor site; qPCR data collected on randomized 96-well or 384-well plates to support reproducibility.

- Data structure and contents
  - Primary data file: qPCR_copy_number_abundance_data_aerial_DNA.csv.
  - Data headers (described in Table 1) include fields such as:
    - Site, Target.Name (grass species), qPCR ID, start.date, end.date, year, day-month, year-month.
    - Quantities: Quantity.Mean, Quantity.SD, Quantity.var, Quantity.SE for copy numbers.
    - qPCR metrics: CT.Mean, CT.SD, CT.var, CT.SE; standard curve parameters (Y.Intercept, R^2, Slope, Efficiency).
    - Location and sampling details: Lat, Long, number.of.days (days pooled), etc.
  - Data rows are organized by sample and target, including technical replicates and metadata for each measurement.

- How this aligns with the Analyst monitoring the environment aims
  - Provides a standardized, openly licensed dataset with clear QA steps, enabling cross-site and temporal comparisons of grass pollen abundance.
  - Includes contextual metadata (timing, location, sampling strategy) and a well-documented data structure to facilitate reuse, integration with other datasets, and scrutiny of environmental health and policy performance over time.