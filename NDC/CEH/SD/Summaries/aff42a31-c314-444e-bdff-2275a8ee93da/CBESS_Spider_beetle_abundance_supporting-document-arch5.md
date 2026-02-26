# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) spider and beetle abundance on salt marsh sites at Morecambe Bay and Essex

## Overview
- Dataset documenting spider and beetle abundance on salt marsh sites at Morecambe Bay and Essex.
- Sampling method: suction sampling from 1 m x 1 m quadrats; four 20-second suctions per sample; samples preserved in 70% IMS; spiders and beetles identified to species level where possible.
- Field campaign conducted in Winter and Summer 2013.
- Staff responsible: Hilary Ford.

## Location and Habitat Context
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM) with provided coordinates.
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP) with provided coordinates.
- Habitat context: Saltmarsh sites chosen to represent two contrasting soil types (Essex: clay; Morecambe Bay: sandy). Regions also differ in inundation frequency, creek structure, and dominant vegetation.
- Grazing regimes: Essex areas (hare grazing; some sites heavily grazed by Brent geese); Morecambe Bay areas (heavy sheep grazing; pink-footed geese present; West Plain lightly grazed).

## Temporal and Sampling Design
- Temporal coverage: Winter and Summer 2013.
- Sampling framework: 1 m x 1 m quadrats across multiple sites with a consistent suction protocol; quadrats organized with a templated approach; scale categories defined (A–D) representing increasing spatial extent.

## Data Collection and Processing
- Observed variables: counts of numerous spider and beetle species per sample (numbers per sample).
- Data structure includes a comprehensive species list (e.g., Pardosa purbeckensis, Pardosa pullata, Pardosa amentata, Pirata sp., various Linyphiidae, Coccinellidae, Carabidae, etc.), each recorded as species abundance per sample.
- Field and lab procedures: samples collected in the field, preserved, and later identified using a stereoscope; taxonomic guidance provided by Roel van Klink (Groningen University, Netherlands).
- Calibration procedures: None documented.
- Data quality checks: No data checking procedures documented.
- File format: Excel workbook.
- Other information: NA cells indicate no data.

## Data Structure and Metadata
- Core fields (per dataset schema): Season (Winter or Summer), Location (Morecambe or Essex), Site (e.g., CS, WS, WP; AH, FW, TM), Quadrat Number, Scale (A–D with corresponding spatial interpretations), Row Number.
- Species abundance: a large set of columns for individual species (numbers per sample) and related entries for juvenile specimens where applicable.
- Descriptions indicate two parallel entries (1 and 2) for many fields, suggesting paired or duplicate schema definitions within the dataset.

## Data Governance and Stewardship Considerations
- Strengths: Detailed spatial and temporal context; precise site coordinates; clear sampling method and unit definitions; extensive species-level counts enabling biodiversity analyses.
- Gaps for stewardship: documented calibration and quality control steps are absent; data checks are not described; two-part field schema (1 vs 2) may complicate integration; taxonomy updates and nomenclature consistency are not addressed.
- Recommendations for data stewards:
  - Implement and document QA/QC procedures for species identifications and data entry.
  - Standardize taxonomy and update to current accepted names; record synonyms where applicable.
  - Provide a consolidated data dictionary and resolve duplicate field schemas (1/2) to ensure interoperability.
  - Consider exporting to more interoperable formats (e.g., CSV, database) and defining a clear data license and update workflow.
  - Ensure precise metadata for coordinates, sampling dates, and site descriptions to improve discoverability and downstream reuse.

## Practical Implications and Potential Reuse
- Useful for biodiversity and ecosystem service studies, particularly in understanding species abundance patterns across soil types, grazing regimes, and inundation contexts.
- Enables analyses of species-level responses to habitat variation and temporal changes (Winter vs Summer).
- Suitable for GIS-based analyses given explicit coordinates and site-level context, provided data quality and schema are harmonized.