# Limits to adaptation: Causes and consequences for ecology and ecosystem function

- A large-scale mesocosm experiment to understand how genetic diversity and intrinsic plasticity in Daphnia magna influence ecosystem responses to repeated heatwaves.
- Location and scale: 42 mesocosms (3,000 L each) at Ness Botanical Gardens, UK; part of a project funded by NERC (NE/N016017/1) and conducted by the University of Liverpool and collaborators.
- Experimental design: seven treatments varying in genetic diversity, plasticity, and exposure to heatwaves, aimed at teasing apart how these factors affect ecosystems under warming.
- Data sharing intent: multiple datasets collected during 2017–2019 are provided for downstream analysis of temperature dynamics, environmental conditions, host phenotypes, community composition, and clone dynamics.

## Experimental design and sampling regime

- Treatments and factors
  - Manipulated genetic diversity and plasticity of Daphnia magna clones.
  - manipulated exposure to heatwaves across mesocosms (frequency and timing) to simulate climate stress.
  - The full treatment map and specifics are described in the study plan and accompanying figures (plan for Ness mesocosm layout referenced).

- Data collection timeframe and scope
  - Temperature data (hourly) collected continuously; additional environmental measurements every 2 weeks; phenotypic and community data collected over two years.
  - Five data streams (datasets) are made available for download, each with specific sampling schedules and protocols.

## Datasets available to download

- Data set 1 – Hourly temperature
  - 42 mesocosms; 5-minute temperature intervals; sun-protected sensors at 50 cm depth.
  - Temperature control system simulated two summer heatwaves per mesocosm (except certain controls with high diversity).
  - Data columns include Date.Time and per-mesocosm temperature readings (Tank_2 to Tank_50).

- Data set 2 – Environmental parameters
  - Environmental measurements across mesocosms spanning July 2017 to June 2019.
  - Variables include block/treatment information, chlorophyll, oxygen saturation and mg/L, temperature, light transmission, pH, conductivity, various nutrient measures (DP, DN, NH4, TP, TN), and presence/absence of D. magna.
  - Metadata fields describe sampling dates, treatments, and system conditions (e.g., light, CT measurements).

- Data set 3 – Phenotypic evolution
  - Life-history data for D. magna collected at five timepoints (Sept 2017; Mar 2018; Jun 2018; Aug 2018; Oct 2018).
  - Common garden rearing (21°C, standard diet) and tracking of one individual through its second clutch.
  - Nine life-history variables (e.g., age at maturity, size at maturity, juvenile and adult growth, clutch metrics, heat tolerance CTmax, etc.).

- Data set 4 – Community data
  - Zooplankton community composition sampled at eight timepoints.
  - Sampling method: depth-integrated water samples processed to counts and identifications for various taxa (Daphnia spp., other cladocerans, copepods, ostracods, insect larvae/adults, arachnids, and other crustaceans).
  - Counts documented per mesocosm, with taxonomic resolution to the lowest possible level.

- Data set 5 – Clone frequency changes
  - D. magna clones genotyped at multiple timepoints from selected treatments (8 timepoints total across different treatment blocks).
  - Genotyping methods differ by treatment: 4 microsatellite markers for high-plasticity/maladaptive treatments; 15 microsatellite markers for 43-clone controls.
  - Data include timepoint, sample ID, clone identity, proportion per clone, and population factor.
  - Genotype counts per mesocosm/timepoint averaged around 45.51 ± 0.41, with some sample exclusion due to quality issues.

## Data collection details and methods (highlights)

- Data set 1: Temperature
  - Real-time data collection via Campbell Scientific CR6 loggers; heatwave events defined by temperature profiles matching historical events plus a +2°C increment.
- Data set 2: Environment
  - In situ measurements of water quality, light, pH, conductivity, nutrients, and biotic indicators (e.g., chlorophyll, D. magna presence).
- Data set 3: Phenotypes
  - Standardized husbandry and a suite of nine life-history traits measured across five temporal checkpoints; includes CTmax thermal tolerance assays.
- Data set 4: Community
  - Systematic counting and taxonomic identification of microzooplankton from multiple depths and locations within each mesocosm.
- Data set 5: Genotypes
  - DNA-based clone identification using microsatellite markers; data structured to show clone frequencies across time and treatments.

## Data quality, structure, and provenance

- Quality control
  - All data have been checked, verified, and processed for analysis.
- Data formats
  - All datasets provided as comma-separated values (CSV) with detailed variable descriptions.
- Metadata and structure highlights
  - Dataset 1 includes time-stamped temperature readings by mesocosm.
  - Dataset 2 includes a range of environmental and biotic measurements with explicit treatment and block identifiers.
  - Dataset 3 documents standardized phenotypic assays across five timepoints with a set of 9 life-history metrics.
  - Dataset 4 captures community composition with spatially and temporally explicit sampling records.
  - Dataset 5 records clone proportions using microsatellite genotyping data, with timepoint, clone identity, and population context.

## Access, provenance, and governance

- Provenance
  - Data generated as part of the Limits to Adaptation project, supported by NERC grant NE/N016017/1.
- Access
  - Data are available for download as CSV files with clearly named datasets and associated metadata.
- Documentation
  - Each dataset includes detailed column descriptions and methods aligned with the experimental design, enabling reproducibility and re-use.

## Data stewardship considerations and recommendations

- Metadata and standardization
  - Maintain comprehensive, dataset-level metadata including study purpose, experimental design, treatment definitions, spatial layout, sampling schedules, and measurement protocols.
  - Preserve units, sampling frequencies, and sensor specifications to ensure cross-dataset interoperability.
- Provenance tracking
  - Record data origin, transformations, QC steps, and any exclusions or corrections to enable audit trails.
- Reuse and interoperability
  - Ensure consistent file naming, versioning, and licensing information; consider offering derived data products (e.g., time-aggregated summaries) to facilitate reuse.
- Long-term accessibility
  - Archive in a stable repository with persistent identifiers; document grant-based provenance and contact points for data access questions.