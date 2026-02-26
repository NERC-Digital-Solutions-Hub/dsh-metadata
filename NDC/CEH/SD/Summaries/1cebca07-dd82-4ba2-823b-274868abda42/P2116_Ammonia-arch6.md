# Bacterial community structure and soil process data from a sewage sludge amended upland grassland soil experiment, 2000 [NERC Soil Biodiversity Programme]

## Overview
- A data release from the NERC Soil Biodiversity Thematic Programme focusing on how sewage sludge and lime amendments affect bacterial communities and soil processes in upland grassland at Sourhope, Scotland (1999–2000).
- Addresses whether treatments select for specific bacterial populations and how changes in community structure relate to soil biogeochemical function.

## Experimental design and sampling
- Site: Rigg Foot experimental field at Sourhope Research Station; acidic brown forest soils.
- Design: Randomised block with three replicates and four treatments: untreated control, lime only, sludge only, sludge with lime.
- Treatments: Lime 600 g m^-2 over two years; sewage sludge applications (10 L m^-2 in 1999 and 20 L m^-2 in 2000).
- Sampling: Soil cores collected across plots; in 1999 data showed root-zone activity was dominant, so 2000 sampling focused on the root zone.
- Time points: Sampling occurred days 1, 3, 16, 30 and 58 after sludge application (May 30, 2000).

## Measurements and methods
- Soil characteristics: pH, moisture content, total carbon, total organic carbon, total Kjeldahl nitrogen, soil NH3; baseline weather and vegetation data also recorded.
- Soil processes: Basal respiration (CO2 production) and autotrophic nitrification potentials (nitrite production in chlorate-treated slurries).
- Molecular analyses: TTGE (temporal temperature gradient electrophoresis) of PCR-amplified 16S rDNA to profile bacterial communities, including eubacteria and ammonia-oxidizing bacteria (AOB).
- Data handling: DNA extracted from soil, PCR products GC-clamped, TTGE gels run and imaged; banding patterns analyzed to generate community similarity metrics.

## TTGE analysis and data processing
- Band identification: Intensity and position of bands determined per gel lane; used to compute weighted Sorensen similarity coefficients between samples.
- Temporal and treatment analyses: Similarity coefficients plotted over time and across treatments; clustering via UPGMA.
- Statistics: Two-factor ANOVA (time and treatment) on replicate data; exploratory methods (e.g., PCA) not applied due to design constraints.
- Outputs: Profiles for eubacteria and ammonia-oxidizing bacteria across treatments and time points.

## Datasets and data structure
Eight CSV files provided, covering soil chemistry, sampling details, and TTGE-derived microbial profiles:

- Dataset 1034: Soil analysis data (2000)
  - Variables include SAMPLE_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, pH, SM (soil moisture), TOC, TKN, RES (soil respiration), AM_OX (ammonia oxidation potential), NIT_RED (nitrification potential), METH_GEN (methane production), METH_OX (methane oxidation).

- Dataset 1035: Soil analysis data – Bulk Sampling Details
  - Metadata on sampling units (SUID), BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT, SOIL_HORIZON, TIME_AFTER_SLUDGE, SAMPLE_TYPE.

- Dataset 1124: Numerical analysis of eubacterial community profiles (P2116_EUBACTERIAL_CP.csv)
  - TTGE band intensities for 54 bands (BANDS1–54), DAYS_AFTER_SLUDGE, TREATMENT, HORIZON, etc., plus SUID and sampling metadata.

- Dataset 1125: Numerical analysis of ammonia oxidizer community profiles (P2116_AMMONIA_OXIDISER_CP.csv)
  - TTGE data for ammonia-oxidizer profiles with similar structure to 1124, including RELATIVE_INTENSITY per band and sampling metadata.

- Dataset 1126: Numerical analysis of ammonia oxidizer CP – sludge-only (P2116_AMMONIA_SLUDGE.csv)
  - Ammonia-oxidizer TTGE data for sludge-only treatment across time points; includes BAND_NUMBER and RELATIVE_INTENSITY.

- Dataset 1127: Numerical analysis of ammonia oxidizer CP – untreated soil (P2116_AMMONIA_UNTREATED.csv)
  - Ammonia-oxidizer TTGE data for untreated soil across time points; includes BAND_NUMBER and RELATIVE_INTENSITY.

- Note: All TTGE datasets include SUID, BLOCK, MAIN_PLOT, SUB_PLOT, TREATMENT, HORIZON, DAYS_AFTER_SLUDGE, and band-specific values.

## Quality control and caveats
- Validation steps included numeric range checks, formatting conformity, and logical integrity checks.
- Data were quality assured, but NERC disclaims warranting the accuracy or fitness of the data for any particular use; user bears responsibility for interpretation and use.
- Additional background data (weather, vegetation surveys) are available via the Environmental Information Centre catalogue.

## Usage and references
- Data are organized to support cross-dataset analyses: linking soil chemistry, sampling metadata, and TTGE-derived microbial profiles.
- References include methodological standards and related findings from the Sourhope field data and the NERC Soil Biodiversity Programme.
- Users are encouraged to consult linked handbooks and related publications for detailed context and data handling practices (e.g., Scott et al. 2003; Griffiths et al. 2000; Head et al. related works).