# Radiocarbon dating of charcoal pieces collected from soil in the Amazon Basin

## Overview
- Dataset of radiocarbon dating for macrocharcoal (~ ≥ 1 mm) from soil profiles in the Amazon forest (Guyana, Peru, Brazil), part of the RAINFOR network.
- 60 charcoal pieces dated from field campaigns in 2015, 2017, 2018, and 2019.
- Data stored in CSV file named C14.csv with site-level metadata and 14C ages.

## Data collection methods and provenance
- Charcoal collected from soil profiles in three replicate pits per site, separated by 100 m; pits located just outside 1 ha plots.
- Macrocharcoal sampling: soil excavated in 1 cm depth increments to 70 cm; four pieces per pit selected for dating using surface-near and progressively deeper depth criteria; one additional depth date in Northern Peru for depth consistency.
- Sample preparation: removal of soil from charcoal surfaces; acid-base-acid pretreatment; conversion to CO2 and then to graphite; AMS dating conducted at UK and Brazilian facilities.
- Funding acknowledged from NERC (grant NE/N011570/1) and CAPES (Brazil).

## Data processing and analysis
- Accelerator Mass Spectrometry (AMS) dating performed after standard chemical pretreatments.
- 14C ages recorded as years before present (yr BP) with associated uncertainties.
- Quality control: failed runs or non-convergent results discarded from the dataset.

## Data structure and metadata
- Data file: C14.csv with columns including:
  - Location, Plot, Latitude, Longitude
  - Soil_Pit, Depth
  - C-14_age_yr_BP, C-14_age_Uncertainty
  - Lab_ID
- Missing data are marked as NA; some field data may be unavailable.

## Data quality and governance
- Clear provenance from field collection to laboratory analysis; traceable methodology and lab IDs support reproducibility.
- Metadata includes precise geographic coordinates and depth information, aiding discoverability and reuse.
- Data ready for integration with related datasets and publications on Amazon forest fire history and charcoal chronology.

## Availability and references
- Related publications cited:
  - Feldpausch et al. (2022) Frontiers in Forests and Global Change
  - Goulart et al. (2017) Quaternary Geochronology
- Methodological reference: Slota et al. (1987) on small-sample preparation for 14C targets.

## Implications for Data Leaders
- Demonstrates end-to-end data governance: from field collection, standardized lab processing, to transparent metadata and data structure.
- Highlights the importance of:
  - Comprehensive metadata (location, depth, age, uncertainty, Lab_ID) for discoverability and reuse.
  - Clear data provenance linking dataset to publications and funding.
  - Explicit quality control practices (discarding failed runs) to ensure dataset reliability.
- Potential considerations for future datasets:
  - Ensure ongoing updates and versioning, and consider expanding metadata to capture more contextual variables (e.g., soil type, pit coordinates, sampling dates).
  - Maintain accessibility beyond publications to maximize cross-network reuse within data communities like RAINFOR.