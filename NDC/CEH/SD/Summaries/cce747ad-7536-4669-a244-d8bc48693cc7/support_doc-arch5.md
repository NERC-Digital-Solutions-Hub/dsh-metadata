# Multivariate Life-history phenotype of 56 Daphnia magna clones reared in four different environments (Factorial cross of temperature x food). Brunner, F.S., Reynolds, A., Price, S., Atkinson, D.A., Paterson, S., and Plaistow, S.J. (2022)

## Overview
- A dataset describing life-history and thermal-tolerance traits for 56 Daphnia magna clones reared in a factorial cross of two temperatures and two food levels.
- Aims to quantify additive genetic variation and its alignment with plasticity across environments.
- Data are organized as a single CSV data set (Data set 1 - Multivariate plasticity data set) with extensive metadata and trait measurements.

## Experimental design and sampling
- Clones and origins:
  - 43 UK clones collected as resting eggs from Brown Moss, July 2016.
  - 5 French clones from the Camargue (2007).
  - 8 Danish clones from Lake Ring (2000).
- Pre-experiment maternal effects control:
  - From each clone, three females were isolated and reared to produce clutches.
  - One offspring from each clutch was reared to reduce maternal effects; used for the experiment.
- Rearing and treatments:
  - 56 clones reared in a full factorial design crossing food level (2x10^5 vs. 0.4x10^5 C. vulgaris cells ml^-1 day^-1) and temperature (24°C and 18°C).
  - Individuals reared in 200 ml jars with 150 ml artificial pond water media; fed live algae; media refreshed every two weeks.
  - 3–8 second-clutch neonates per clone allocated to each of four treatments.
  - Experimental blocks: 5 temporal blocks (Jan 2017–Mar 2018); each clone assayed in multiple blocks.

## Measurements and data collected
- Sampling regime:
  - Photography of neonates, mature individuals, and those releasing their second clutch.
  - Offspring counts: number of neonates in clutch 1 and clutch 2; five neonates per clutch photographed to estimate offspring size.
  - Body size: measured as distance from the top of the head to the base of the tail-spine (mm) using ImageJ.
- Traits measured per individual:
  - Length at maturity; length at second clutch.
  - Age at maturity; age at second clutch.
  - Juvenile growth rate (mm/day).
  - Adult growth rate (mm/day).
  - Average fecundity (across clutches 1 and 2).
  - Average offspring size (across clutches 1 and 2).
  - Thermal tolerance (CTmax) after acclimation and ramping protocol (21°C acclimation, 40 s/°C ramp from 21°C to 50°C).

## Data structure and content
- Data format: Comma-separated values (CSV) with a single data set titled Data set 1 - Multivariate plasticity data set.
- Core fields and examples:
  - Clone, Rep, Block, Tray, T (temperature), food, treat (treatment group).
  - cl1No, cl1moult; cl2No, cl2moult.
  - agemat, Age1cl, Age2cl.
  - Lneo, LMat, L2cl.
  - cl1size, cl2size.
  - Htdate, Tfaint, Timm.
  - obs, clutchpresHT, HTBatch.
  - aveclNo, aveoffsize.
  - grjuv (juvenile growth rate), grad (adult growth rate).
  - Pop (population of origin factor).
- The data structure supports analyses of additive genetic variation, plasticity, and genotype-by-environment interactions across the four rearing environments.

## Quality control and provenance
- All data have been checked, verified, and processed for analysis.
- References linked to the study design and methods:
  - Geerts et al. (2015) on rapid evolution of thermal tolerance in Daphnia.
  - Plaistow & Collin (2014) on phenotypic integration and G×E interactions.

## Metadata, standards, and governance considerations for Data Stewards
- Data provenance:
  - Clear documentation of clone origins, collection years, and maternal-effect control procedures.
  - Detailed experimental design description (crossed temperature x food, block structure) to support reproducibility.
- Metadata and discoverability:
  - Comprehensive field descriptions and units (e.g., mm for size, days for ages, °C for temperature).
  - Inclusion of replication, block, tray, and treatment identifiers to facilitate data filtering and re-use.
- Data format and interoperability:
  - CSV with wide-ranging life-history and thermotolerance metrics; consistent column naming as per dataset description.
- Sharing and maintenance:
  - Consider providing a persistent identifier (e.g., DOI) for Data set 1, with versioning for updates.
  - Documentation should accompany the dataset to enable discovery, interpretation, and reuse in comparative or meta-analyses.
- Potential use cases:
  - Analyses of additive genetic variation and alignment with plasticity.
  - Genotype-by-environment interaction studies across temperature and food environments.
  - Life-history and thermal-tolerance trait integration across clonal lineages.

## Use and reuse considerations
- Suitable for examining how genetic variation among clones maps onto plastic responses to environmental factors.
- Useful for understanding trade-offs and covariation among life-history traits under different rearing conditions.
- Appropriate for data-driven governance studies on data sharing, metadata richness, and reproducibility in ecological genetics datasets.