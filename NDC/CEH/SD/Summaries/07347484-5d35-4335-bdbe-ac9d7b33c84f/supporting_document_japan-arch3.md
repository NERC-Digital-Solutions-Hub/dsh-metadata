# Impact of environmental radiation on the health and reproductive status of fish from Japan, 2017

## Overview
- Study conducted May 8–18, 2017 across multiple lakes in Japan (Suzuuchi SU, Funazawa FZ, Kashiramori KM, Abakuma; Abukuma River at Shinobu Dam coordinates 37°42'21.28"N, 140°30'07.03"E).
- Target species: crucian carp, common carp, smallmouth bass, with sampling focused on assessing radiation-related effects.
- Primary aims: evaluate radiation-related cataract formation in carps and largemouth bass; assess reproductive status in carps.
- Data produced includes a structured dataset (japan_biometry.csv) with detailed morphometric and gonad measurements.

## Objectives
- Assess cataract formation in carp and largemouth bass as a potential radiological effect.
- Assess reproductive status in carp (gonad weight and related metrics).

## Study design and methods
- Specimen collection:
  - Largemouth bass: adults of uniform size (total length 17–22 cm) to target a single age group.
  - Carps: adults across a 20–30 cm range to target two generations (F0 and ideally F1).
- Measurements and processing:
  - Post-mortem measurements and scales/otoliths removed for age determination.
  - Gonads dissected, weighed, fixed in buffered formalin for 24 hours, then preserved in ethanol.
- Data captured (as part of Japan biometry dataset) includes morphometrics and gonad data at the individual level.

## Data structure and content
- Dataset name: japan_biometry.csv
- Key fields and what they represent:
  - Site: Lake/region reference
  - Species: Common carp (Cyprinus carpio), Crucian carp (Carassius carassius), Largemouth bass (Micropterus salmoides), Smallmouth bass (Micropterus dolomieu), Carp KOI (Cyprinus sp.)
  - Weight: total fish weight (grams)
  - BL: body length to start of tail (cm)
  - SL: standard length to fork of tail (cm)
  - TL: total length (cm)
  - GW1: gonad weight (grams)
  - GW2: second gonad weight for males (grams; may be blank if not recorded)
  - Sex: M or F (male/female; may be blank if not identified)
  - Liver weight: liver weight (grams; may be blank if not recorded)
- Data quality notes:
  - Some fields may be blank if data were not recorded.
  - Units are specified (grams for weights; centimeters for lengths).

## Data access and reuse
- Data access: https://doi.org/10.5285/07347484-5d35-4335-bdbe-ac9d7b33c84f
- Citation:
  - Lerebours, A.; Smith, J.T. (2019). Impact of environmental radiation on the health and reproductive status of fish from Japan, 2017. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/07347484-5d35-4335-bdbe-ac9d7b33c84f

## Data quality, interoperability, and governance considerations for monitoring frameworks
- Metadata and data accessibility:
  - Clear metadata fields and units support interoperability and reuse.
  - Explicit data sharing through a public dataset with a formal citation and DOI aligns with open data and governance expectations.
- Data completeness and gaps:
  - Some fields may be missing (e.g., GW2, Sex, or Liver weight in certain records), highlighting the need for clear documentation of missing data when integrating datasets.
- Standardization:
  - Consistent measurement types (weight, various length measures, gonad weights) and standardized age targeting enable cross-study comparisons.
- Governance and transparency:
  - Public data sharing and dataset provenance support accountability, reproducibility, and data stewardship—key considerations for monitoring frameworks.
- Practical implications for policy monitoring:
  - The structured data approach (species, site, morphometrics, gonad data) supports evaluating radiation-related health and reproductive endpoints across taxa and locations.
  - Availability of a detailed dataset enhances capacity to track trends, compare sites, and inform future monitoring design and decision-making.