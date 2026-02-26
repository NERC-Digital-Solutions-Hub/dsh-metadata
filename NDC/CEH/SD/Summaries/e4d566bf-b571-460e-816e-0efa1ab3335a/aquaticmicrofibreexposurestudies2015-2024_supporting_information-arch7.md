# AquaticMicrofibreExposurestudies2015-2024 Supporting information

## Overview
- Dataset includes the file "TraitResponsesofAquaticOrganismsfromMicrofibreExposurestudiespublished20152024.csv" with data extracted from published laboratory studies.
- Focus: impacts of microfibres (<5 mm) on traits such as development, fecundity, feeding, growth, hatching, health, and survival in aquatic organisms.
- Global scope: data collected from published literature by researchers worldwide; available as of 19/06/2024.
- Purpose: to support a meta-analysis comparing biological responses to non-petroleum versus petroleum-based microfibres.
- Curator: Ben Parker.
- Completeness: limited to studies and responses meeting predefined eligibility criteria; references of eligible studies provided.

## What is included
- Extracted study data for laboratory studies on microfibre impacts, including exposure to single polymer types (no mixtures) and measured responses that could be extracted (means and errors).
- Key traits captured: Development, Fecundity, Feeding, Growth, Hatching, Health, Survival.
- Data extraction sources: manuscript text, supplementary information (SI), and figures via plot digitiser.
- Data are included for final timepoints/lifestages when multiple timepoints existed; co-contaminant exposures excluded.
- Positive responses prioritized (increasing values deemed “good”); some negative responses converted to positive if necessary for inclusion.
- All eligible responses were extracted across exposure combinations (starved/fed, different parameters) but excluded co-contaminants.

## Collection and screening (quality control)
- Screening stages:
  - Stage 1: titles/abstracts screened for relevance to microfibre exposure effects.
  - Stage 2: citing/cited studies screened for relevance.
  - Stage 3: eligibility screening on duplicates, study design, exposure type, and data extractability.
- Eligibility criteria:
  - Aquatic organisms used
  - Controlled microfibre exposure (>1 µm and <5 mm) of a single polymer type
  - Means with associated errors available for exposure and control
  - Data extractable from manuscript/SI/figures
- Data extraction method: mean values, standard deviations (SD), and other necessary statistics were captured; where needed, values were converted or standardised.

## Data structure and units
- Main CSV: AquaticMicrofibreExposurestudies2015-2024
- Key fields (representative list):
  - ID, Study.no, Reference, Authors, Title, Year
  - FA.country (country of first author’s primary affiliation)
  - Species, Source (where species sourced)
  - Environment (Freshwater, Marine, Estuarine, etc.)
  - Assigned taxonomic grouping
  - Days.exposed, Days.cat (exposure duration category)
  - Microfibre category (Non-petroleum vs petroleum-based)
  - MF.category, Length.mm, Length.cat, Width.mm
  - Study.exposure, Study.exposure.units (non-standardised exposure concentration)
  - Standard.exposure (standardised exposure concentration by mass or fibre number)
  - S.cat (units for standardised exposure)
  - Time.series, Additional.variable
  - C.N, C.mean, C.SD, E.N, E.mean, E.SD (control vs exposed statistics)
  - Data.source (MS or SI)
  - Response (trait category; e.g., Development, Fecundity, etc.)
  - Converted.measure (if a conversion was performed)
  - Response.units
- Purpose of fields:
  - Facilitate meta-analysis synthesis
  - Enable GIS-friendly attribute mapping (e.g., geography, environment, species, exposure type)

## How this relates to GIS and map-based data products
- Geographic context: FA.country enables mapping of study origins and potential geographic patterns in microfibre research.
- Environmental context: Environment field supports spatial layer integration (freshwater vs marine vs estuarine) for regional exposure analyses.
- Taxonomic and trait data: Enables choropleth or symbol maps by taxonomic group or trait category when aggregating across studies.
- Exposure and polymer data: Supports geospatial querying to compare outcomes by fibre type, length, or concentration across study sites.
- Time context: Days.exposed and final timepoint data allow temporal layering in meta-analytic GIS visuals (e.g., exposure duration across regions).

## Data usage notes
- Data are intended for meta-analysis; users should refer to the published manuscript and supplementary information for detailed methodology.
- Only eligible responses with extractable data and compliant exposure conditions are included; caution when comparing across studies due to varying experimental designs.
- Positive responses were prioritized; where necessary, conversions were applied to harmonise measures.
- Data extraction sources are noted (MS or SI) for traceability.

## Study references
- The dataset references a broad set of primary studies (e.g., Au et al. 2015; Blarer & Burkhardt-Holm 2016; Bour et al. 2022; Choi et al. 2021, 2022; Cole et al. 2020; and many others) across various aquatic organisms and microfibre exposure scenarios. Full references are included in the dataset.