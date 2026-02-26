# Impact of environmental radiation on the health and reproductive status of fish from Japan, 2017

## Overview
- A 10-day study conducted in May 2017 targeting crucian carp, common carp, and smallmouth bass across four lakes (Suzuuchi SU, Funazawa FZ, Kashiramori KM, Abakuma) and a site at Abukuma River Shinobu Dam (with precise coordinates provided).
- Objectives: assess radiation-related cataract formation in carp and largemouth bass; assess reproductive status in carp.

## Objectives of the study
- Evaluate the impact of environmental radiation on cataract formation in carps and largemouth bass.
- Assess the effects of radiation on the reproductive status of carps.

## Methods
- Specimen collection: adult fish of similar size for largemouth bass (total length 17–22 cm) to target a uniform age group; carps collected across 20–30 cm to target two generations (F0 and F1) when possible.
- Processing: fish were killed, measured, scales and otoliths removed for age determination; gonads dissected, weighed, fixed in buffered formalin for 24 hours, then preserved in ethanol.

## Data structure and variables (japan_biometry.csv)
- Site: Lake (geographical region)
- Species: includes Common Carp (Cyprinus carpio), Crucian (Carassius carassius), Largemouth Bass (Micropterus salmoides), Smallmouth Bass (Micropterus dolomieu), Carp KOI (Cyprinus sp.)
- Weight: total fish weight (grams)
- BL: body length up to start of tail (cm)
- SL: length up to fork of tail (cm)
- TL: total fish length (cm)
- GW1: gonad weight (grams)
- GW2: second gonad weight for males (grams; may be blank)
- Sex: M or F (blank if unknown)
- Liver weight: liver weight (grams; blank if not recorded)
- Note: blank fields indicate data were not recorded

Data access and reuse
- Data available at: https://doi.org/10.5285/07347484-5d35-4335-bdbe-ac9d7b33c84f
- Citation: Lerebours, A.; Smith, J.T. (2019). Impact of environmental radiation on the health and reproductive status of fish from Japan, 2017. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/07347484-5d35-4335-bdbe-ac9d7b33c84f

## Implications for Data Leaders
- Demonstrates end-to-end data lifecycle considerations: standardized sampling sizes, clear metadata (sites, species, measurements, units), and a structured CSV schema to enable discovery and reuse.
- Highlights importance of documenting context (sampling dates, locations, objectives) to support cross-study comparisons and meta-analyses.
- Emphasizes data quality and completeness challenges (missing GW2, Sex, and other fields) and the need for clear metadata to interpret blanks.
- Provides a stable data access point (DOI) and formal citation to support data governance, reproducibility, and attribution.