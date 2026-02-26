# Physiology and stable isotope ecology of moss growth for modelling spatial and temporal climatic signals NERCDMP-555 - monthly field and dark adapted PAM fluorescence measurements

## Overview
- A study combining moss physiology and stable isotope ecology to model spatial and temporal climatic signals using monthly field measurements and dark-adapted PAM fluorescence data.
- Time period: fieldwork conducted monthly from April 2017 to September 2018.
- Output intended for GIS-based data products to support spatial-temporal climate interpretation through moss-based proxies.

## Spatial scope and sites
- Dersingham Bog (52.83° N, 0.48° E) – habitat: bog heathland; multiple moss species targeted.
- Brandon Country Park (52.43° N, 0.62° E) – habitat: heathland; moss species present.
- Wicken Fen (52.31° N, 0.29° E) – habitat: fen and shaded woodland; moss species present.
- Sites include representative moss lifeforms and habitats suitable as analogues for palaeoclimate work.
- Permissions obtained from landowners/managers prior to field work.

## Target taxa and field sampling
- Target species identified to cover a range of moss lifeforms and growing conditions.
- On each visit: three samples per target species (approximately 2 x 2 x 2 cm) collected and sealed for analysis.
- Voucher specimens collected and species identities verified by bryologists.

## Measurements and laboratory procedures
- Chlorophyll fluorescence (F, Fm, PAR, ETR) measured in the field on moss tips using a Walz MINI-PAM II; three measurements per sample in the field, followed by at least 30 minutes dark adaptation and three additional measurements.
- Derived fluorescence metrics:
  - Fluorescence yield in dark and light (Φ)
  - Non-photochemical quenching (NPQ)
  - Electron transport rate (ETR) calculated as 0.84 × PAR × 0.5 × Φ
- Water content and related metrics:
  - Fresh and dry mass to determine field relative water content (RWC = (Fresh − Dry)/Dry)
  - Dry moss subjected to cellulose extraction (standard method)
  - Water extraction from fresh moss via cryogenic vacuum distillation
  - Fresh precipitation collected at Ely (near field sites)
- Additional analyses:
  - Enzymatic photo-spectrophotometric sucrose content analysis on selected fresh moss samples
- Field and lab methodologies cited from Loader et al. (1997), Stitt et al. (1989), and West et al. (2006)

## Dataset structure and contents
- Dataset comprises 14 monthly sequential CSV files, spanning 01_Jul_2017 to 14_Oct_2018.
- Each CSV contains 18 columns with paired structure (Unit; Description) for metadata and measurements:
  - Session, Date, Sample, Site, Species, Notes
  - F, Fm, Dark_Y, Field_F, Field_Fm, Field_PAR, Field_Y
  - Field_ETR, Field_NP
  - RWC, Cellulose, Value, Date, and related reference/metadata fields
  - Includes references for cellulose and methodological sources
- The columns capture: collection session and date, species/site information, fluorescence measurements (F, Fm, F', Fm'), light metrics (PAR), calculated metrics (Field_Y, Field_F, Field_Fm, Field_ETR, Field_NP), relative water content (RWC), and cellulose-related data, plus notes and sample identifiers.

## Data provenance and references
- Field protocols and analytical methods are grounded in established sources:
  - Loader et al. (1997) for batch processing of cellulose
  - Stitt et al. (1989) for metabolite analyses in plant cells
  - West et al. (2006) for water extraction times in stable isotope analysis
- Data components tied to specific methodological references and field site metadata.

## GIS-ready implications and potential uses
- Spatially explicit, time-resolved moss physiology data across multiple, well-defined sites enables:
  - Time-series mapping of photosynthetic efficiency (Φ), NPQ, and ETR across habitats and taxa
  - Visualisation of spatial patterns in relative water content (RWC) and tissue moisture proxies
  - Integration with climate variables to model spatial-temporal climatic signals using moss-derived proxies
  - Comparative analysis of moss responses across bog heathland and fen landscapes
- Data management considerations for GIS:
  - Ensure consistent georeferencing and harmonized metadata across 14 monthly files
  - Handle varying resolutions and sampling across sites; align with other climate and environmental layers
  - Maintain provenance links to measurement methods and reference standards for reproducibility

## Notes on scope and limitations
- Focused on fluorescence and water-content–related metrics with cellulose and isotopic components described in the broader project context; the dataset details emphasize physiological measurements and their temporal progression.
- Proper use in GIS requires careful metadata integration to preserve site, date, and measurement context for robust spatial-temporal analyses.