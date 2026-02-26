# Assigning Relevant Critical Loads/Levels to designated features of protected nature conservation sites

## Overview
- Describes methodologies for assigning the most relevant critical loads and critical levels to designated habitat and species features across UK nature sites (SAC, SPA, SSSI in England).
- Builds data products to enable mapping and spatial analysis of nitrogen and acidity deposition impacts on protected features.
- Combines data from Annex I habitats, Annex II plant and non-plant species, and SPA bird features with habitat classifications to ensure consistent terminology (EUNIS, NVC, Broad Habitats).

## Phases of assignment
- Phase 1: Annex I habitat features and Annex II plant species features (plant species treated as in situ, part of habitat).
- Phase 2: SPA bird features and Annex II non-plant species features (same method as SPA features).
- Phase 3: SSSI habitat features (England only).

## Critical loads for nutrient nitrogen
- Based on empirical evidence (experiments and gradient studies) under UNECE guidance.
- Assigned to habitat classes in EUNIS to ensure cross-Europe consistency; habitat correspondence tables link EUNIS classes to interest features (Annex I, A/SSSI, Annex II/SPA).
- Sensitivity judgments determine if features may be affected by eutrophication; most habitats are assessed, with some coastal or calcareous features shown as less sensitive due to buffering.
- Justifications are recorded for transparency; uses Noordwijkerhout Expert Workshop (2010) values and reliability notes.
- For SPA and Annex II non-plant features, direct nitrogen deposition impact is often indirect (via habitat integrity affecting birds/species).

## Critical loads for acidity
- Based on soil and habitat types across six Broad Habitats (e.g., acid/calcareous grasslands, heaths, bogs, montane, woodlands).
- Utilizes NBN/JNCC habitat correspondence to match Broad Habitats to Annex I/A/SSSI features and Annex II/SPA features.
- Features are assessed for sensitivity to acidification; coastal features with high buffering are often less sensitive.
- Justifications and potential impacts of exceedance are documented; some calcareous features are considered not sensitive.

## Exceptions
- Some Annex I habitats do not map neatly to a suitable EUNIS class; may require further science-based investigation and site-by-site assessment.
- When no clear match, non-matches are indicated with guidance for potential further work.

## Assigning critical loads for SPA features and Annex II non-plant species
- Direct effects of N or acidity on birds/non-plant species are rare; instead, link to habitat integrity to infer potential impacts on breeding, feeding, or roosting.
- Judgments are based on species’ habitat dependencies, sensitivity to eutrophication/acidification, and potential adverse impacts.
- If habitat is insensitive to either pollutant, no critical load is assigned.
- A structured set of questions guides each species’ linkage to appropriate habitat types and corresponding critical loads.

## Critical Levels
- Not habitat-specific; set to broad vegetation types (e.g., forest, arable, semi-natural) with particular emphasis on sensitive lichens and bryophytes.
- Examples include:
  - NOX: receptor = all; annual mean; critical level = 30 µg/m3.
  - SO2: receptor = forests/natural vegetation; annual mean; critical level = 20 µg/m3.
  - SO2: receptor = sensitive lichens; annual mean; critical level = 10 µg/m3.
  - Ammonia: receptor = lichens and bryophytes; annual mean; critical level = 1 µg/m3.
  - Ammonia: receptor = other vegetation; annual mean; critical level = 3 µg/m3 (uncertainty range 2–4).
- Linkages between habitat and species considered via National Vegetation Classification (NVC) and site knowledge to assign ammonia, nitrogen dioxide, and sulfur dioxide critical levels where appropriate.

## Linkages and data standards
- Habitat-to-load linkages are documented to ensure traceability between features and their critical loads.
- Uses NVC classifications and site-specific knowledge for robust, defensible correlations.

## Data products and structure
- Three CSV datasets representing critical loads/levels linkages across the UK SACs, SPAs, and England-only SSIs:
  - APIS_SAC_sites_feature_critical_load_linkages.csv
  - APIS_SPA_sites_feature_critical_load_linkages.csv
  - APIS_SSSI_sites_feature_critical_load_linkages.csv
- Key fields include:
  - SITECODE, SITENAME, COUNTRY, DESIGNATION, INTERESTCODE, INTERESTNAME, INTERESTTYPE, NVC_CODE, BROAD_HABITATCODE, BROADHABITAT, DEPTYPE, SENSITIVENDEP, NCLCODE, NCLCLASS, JUSTIFICATIONALLOCATIONNCL, EUNIS, CLMIN_NUTN, CLMAX_NUTN, RECOMMENDED_VALUE, NTEXT, SENSITIVEACIDITY, ACCODE, ACIDITYCLASS, JUSTIFICATIONA, ATEXT, BRYOPHYTES, LICHENS, AMMONIA_CL_VALUE, AMMONIA_CL_TEXT, NITROGEN_DIOXIDE_CL_VALUE, NITROGEN_DIOXIDE_CL_TEXT, SULPHUR_DIOXIDE_CL_VALUE, SULPHUR_DIOXIDE_CL_TEXT, SPECIESSENSITIVEN, SPECIESSENSITIVITYN, JUSTIFYSPECIESSENSITIVITYN, SPECIES_SENSITIVE_NH3, SPECIES_SENSITIVE_NOX, SPECIES_SENSITIVE_SO2, and related justification fields.
- Structure captures site code, feature details, habitat classification, corresponding critical loads/levels, justification, sensitivities, and species-specific considerations.

## Data use and implementation
- Geospatial mapping: aligns site features with SAC/SPAs/SSSIs to produce map-based representations of where critical loads/levels are exceeded or of concern.
- Data integration: designed to combine with regional datasets (EUNIS, NVC, APIS) to support consistent, Europe-wide interpretation.
- Quality and transparency: judgements and justifications are documented; expert QC performed by statutory conservation bodies and CEH.

## Access and references
- Resource locator for contextual information: http://www.apis.ac.uk/srcl
- Fieldwork, instrumentation, and calibration details are not part of the dataset (NA).

## Practical implications for GIS Specialists
- Provides three linked, feature-level datasets to map critical loads/levels across protected sites.
- Enables integration with habitat classifications (EUNIS, NVC, Broad Habitats) for consistent interpretation.
- Supports decision-making and policy briefing through transparent justifications and explicit sensitivity assessments.
- Facilitates cross-border and cross-designation analyses by standardizing feature-level loadings and linkages.