# Limits to adaptation: Causes and consequences for ecology and ecosystem function

## Overview
- Large-scale mesocosm experiment to understand how genetic diversity and intrinsic plasticity in Daphnia magna influence ecosystem responses to repeated heatwaves.
- 42 mesocosms (3,000 L each) at Ness Botanical Gardens, UK, with 7 treatments manipulating diversity, plasticity, and heatwave exposure.
- Real-time environmental control to simulate heatwave events; data collected to link climate stress, organismal traits, and community dynamics.

## Data assets available
- Five downloadable datasets, with QC’d data prepared for analysis:
  - Data set 1: Hourly temperature ( Jul 2017 – Sep 2019 ), 42 mesocosms
  - Data set 2: Environmental parameters ( July 2017 – June 2019 )
  - Data set 3: Phenotypic evolution ( 2-year plant/microbial context in Daphnia ), across five timepoints
  - Data set 4: Zooplankton community data, across eight sampling sessions
  - Data set 5: Clone frequency changes (genotyping across selected treatments and timepoints)
- Data provided in CSV format with detailed column definitions and variable descriptions.
- Data provenance: part of NERC Highlight grant NE/N016017/1.

## Experimental design and data collection
- Treatments and manipulations:
  - 7 treatments emphasizing different levels of genetic diversity, plasticity, and heatwave exposure.
  - Use of Brown Moss clones; inclusion of high/low plasticity lines and maladaptive Danish clones in some treatments.
- Heatwave protocol:
  - Two summer heatwaves: Aug 2017–Sept 2017 and Jul 2018–Aug 2018.
  - Heatwaves programmed to mirror a historical profile plus +2°C.
- Data collection cadence:
  - Temperature: hourly/5-minute sampling via sun-protected sensors at 50 cm depth (live real-time monitoring).
  - Environmental parameters: biweekly to every few weeks, including pH, conductivity, nutrients, light transmission, chlorophyll proxy, and ecological markers (e.g., algal crust, turbidity).
  - Phenotypic evolution: five timepoints over two years; common-garden rearing to assess heritable life-history traits and heat tolerance (CT max).
  - Community data: eight sampling sessions across the experiment; depth-integrated zooplankton sampling and identification to lowest feasible taxonomic level.
  - Clone frequencies: genotyping of Daphnia magna from selected mesocosms at multiple timepoints using multiple microsatellite markers.

## Data structure and metadata
- Data set 1 – Hourly temperature:
  - Columns include Date.Time, Tank_2 to Tank_50 with hourly temperature values per mesocosm.
- Data set 2 – Environmental parameters:
  - Variables include week/date, treatment/block, chlorophyll, oxygen saturation/conc, pH, conductivity, nutrients (N/P species and totals), and biotic indicators (presence of D. magna, algal indicators, etc.).
- Data set 3 – Phenotypic evolution:
  - Timepoint, mesocosm, replicate, block, treatment, clutches, maturation metrics, growth rates, body/juvenile sizes, and CT max (heat tolerance).
- Data set 4 – Community data:
  - Mesocosm, collection date, sampling session, block, treatment, diversity/plasticity factors, and counts for multiple taxa (Daphnia spp., other zooplankton, and invertebrates).
- Data set 5 – Clone frequency changes:
  - Timepoint, sample, clone identity, proportion per mesocosm, and population-level factors; genotyped using microsatellite markers.
- Quality and completeness:
  - All data quality-checked and processed; note: some samples missing due to quality or assay failures (e.g., dataset 5 had 45.51 ± 0.41 genotypes per mesocosm/timepoint, min 13, max 48).

## Data quality, provenance, and governance
- Data verification and processing conducted prior to release.
- Data generated as part of a funded project (NERC grant), enabling traceability to original collection events and experimental design.
- Rich metadata enables cross-domain analyses (environmental drivers, phenotypic trait changes, community composition, and genetic frequencies).

## Access, reuse, and potential analyses
- Enables integrated, multi-level analyses of adaptation and ecosystem function under climate stress:
  - G x E interactions across genetic diversity and plasticity contexts.
  - Linking environmental stress (heatwaves) to phenotypic changes and reproductive traits.
  - Assessing how altered community composition interacts with host genotypes and phenotypes.
  - Tracking clonal dynamics and their relation to fitness under heat stress.
- Suitable for meta-analyses on experimental climate adaptation and for informing data-management practices in complex ecological experiments.

## Challenges and considerations
- Data heterogeneity: multiple data types (continuous time-series, count data, life-history traits, genetic frequencies) with varying sampling frequencies and units.
- Missing data: some samples not completed due to quality issues, requiring careful handling in analyses.
- Complexity of integration: aligning timepoints across datasets (temperature, phenotypes, community data, and clone frequencies) for robust G x E inferences.

## References
- Geerts AN, et al. Rapid evolution of thermal tolerance in the water flea Daphnia. Nature Climate Change. 2015.
- Plaistow SJ, Collin H. Phenotypic integration plasticity in Daphnia magna: an integral facet of G × E interactions. J Evol Biol. 2014.