# Telomere length data in a wild Seychelles warbler population

## Overview
- Long-term dataset of relative telomere length (RTL) in Seychelles warblers on Cousin Island (approx. 320 adults across 115 territories).
- RTL measured via qPCR from blood samples collected between 1995 and 2014; dataset used to study telomere heritability and parental age effects.
- Data include both individual-level metadata and laboratory QA/processing information, enabling longitudinal and cross-sectional analyses.
- Key publications informing the dataset: Sparks et al. (2021), Spurgin et al. (2018), Bebbington et al. (2016).

## Data collection and laboratory methods
- Field collection
  - Major breeding season: June–September; minor season: January–March.
  - Birds caught using mist nets; blood samples (~25 μl) stored in absolute ethanol at room temperature.
- DNA extraction and RTL measurement
  - DNA extracted with DNeasy kit; integrity checked by agarose gel.
  - RTL measured by qPCR; DNA diluted to 3.3 ng/μl before measurement.
  - Quality checks included DNA concentration thresholds, purity ratios (260/280 between 1.8–2.0; 260/230 > 1.8), and gel-based integrity validation.
- Randomization and bias control
  - Sample assignment to qPCR plates randomized prior to runs to avoid systematic bias related to age, sex, cohort, or environment.
- Replicates and plate effects
  - Within-plate repeatability: GAPDH ~0.74; RTL ~0.73.
  - Between-plate repeatability (n=422 samples measured twice): RTL ~0.68.
  - Plate included as a random effect in analyses to account for inter-plate variance.

## Data quality and processing
- Data cleaning and inclusion criteria (based on Spurgin et al. 2018)
  - Exclude samples with telomere cq > 25 or GADPH cq > 26; exclude replicate differences > 0.5.
  - Include only samples with RTL values ≥ 3.
  - Exclude DNA degraded samples; re-extract or exclude as needed.
  - Post-cleaning dataset includes 2,664 samples from 1,318 individuals.
- Outlier handling
  - Outlier samples with extremely large cq values were removed to prevent bias.
- Sample assignment and replicates
  - For analyses requiring replication across plates, RTL values for a given blood sample were randomly selected from replicates when plate effects needed to be evaluated.

## Data structure and fields
- BirdID: Individual bird identifier
- Sex: 0 = female, 1 = male
- AgeY: Age at catch (years)
- AgeClass: A (adult), CH (chick), FL (fledgling), J (juvenile), OFL (old fledgling), SA (subadult)
- BirthFPID: Birth fieldwork period ID
- U_PlateID: qPCR plate ID for RTL measurements
- RTL: Relative telomere length
- Technician: Technician who performed the qPCR (2 levels)
- Terr: Territory in which the bird resided during capture
- FPID: Fieldwork period ID when the bird was caught
- mum: Mother ID from genetic pedigree
- dad: Father ID from genetic pedigree
- MAC: Maternal age at conception (years)
- PAC: Paternal age at conception (years)
- BrF: Dominant female in natal territory
- BrM: Dominant male in natal territory

## Experimental design and fieldwork
- Major breeding season runs June–September; some pairs breed in the minor season (January–March).
- Each breeding season, as many birds as possible are captured using mist nets to maximize data coverage across individuals and territories.

## Practical implications for GIS and data integration
- Spatial components available: Terr (territory) and FPID provide a link to spatial time-series data, enabling mapping RTL across territories and over time.
- Potential for GIS workflows:
  - Join RTL and metadata to territory boundaries, habitat layers, and temporal event data.
  - Analyze spatial patterns of RTL by territory or lineage, accounting for year and plate effects.
- Data challenges relevant to GIS
  - Data are distributed across multiple sources and years; ensure consistent data standards and join keys (BirdID, Terr, FPID) for robust mapping.
  - Handling large longitudinal datasets requires careful data management and potential aggregation (per territory, per year) for tractable visualization.
  - Quality control metadata (plate, replicate, cq values) is essential for reliable spatial-temporal analyses and uncertainty assessment.

## References
- Sparks et al. 2021
- Spurgin et al. 2018
- Bebbington et al. 2016