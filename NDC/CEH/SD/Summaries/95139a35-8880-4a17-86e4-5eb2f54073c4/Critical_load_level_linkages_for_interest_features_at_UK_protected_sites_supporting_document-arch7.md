# Assigning Relevant Critical Loads/Levels to designated features of protected nature conservation sites

## Overview
- Describes methodology to assign relevant critical loads and critical levels to designated features of UK protected sites (SAC, SPA, A/SSSI).
- Supports mapping-based data products for assessing atmospheric deposition impacts on habitats and species.
- Uses habitat-based linkages (EUNIS, NVC) to ensure consistent terminology across Europe.

## Methodology and Phases
- Phase 1: Assign Annex I habitat features and Annex II plant species features (Annex II plants treated as in situ habitat).
- Phase 2: Assign SPA bird features and Annex II non-plant species features (uses same method as SPA features; indirect approach to birds via habitat).
- Phase 3: Assign A/SSSI habitat features only.
- For each, provide justification, reliability notes, and transparent matching to appropriate habitat classes.

## Critical Loads for Nutrient Nitrogen
- Based on empirical evidence and gradient studies (UNECE/Noordwijkerhout Expert Workshop 2010).
- Assigned to habitat classes in the European Nature Information System (EUNIS) to maintain harmonised habitat terminology.
- Habitat correspondence tables link EUNIS classes to features (Annex I, Annex II/SPA, A/SSSI).
- Sensitivity assessments determine if features are affected by eutrophication; exemptions for estuaries, reefs, coastal lagoons where buffering reduces sensitivity.
- Justifications are recorded for transparency and consistency.

## Critical Loads for Acidity
- Based on soil and habitat types; six Broad Habitats (e.g., acid/calcareous grassland, heath, bogs, montane, woodlands).
- Use NBN/JNCC habitat correspondences to assign acidity loads to Annex I, A/SSSI, or Annex II/SPA features.
- Sensitivity assessments determine potential impacts; coastal features with buffering may be non-sensitive.
- Justifications and impact descriptions are documented.

## Exceptions and Direct Applications
- Some Annex I features may not map neatly to a suitable EUNIS class; may require further science-based adjustments or site-by-site assessments.
- Directly assigning loads to bird features or non-plant species is generally unsuitable; instead infer impacts through habitat condition and species dependencies.

## Linkages to Species and Habitats
- For each species, assess relevant Broad Habitat, habitat sensitivity to eutrophication or acidification, and potential impacts on breeding/feeding/roosting.
- When habitat is insensitive to deposition effects, no load is assigned.
- Where possible, link habitat-level conclusions to species outcomes; acknowledge possible positive or negative effects of eutrophication.

## Critical Levels
- Not habitat-specific like loads; set to broad vegetation types with receptor specifics (e.g., lichens, bryophytes).
- Key values:
  - NOX: 30 µg/m3 (annual mean) – receptors: all; references: WHO, CLRTAP, AQ Directive.
  - SO2: 20 µg/m3 (annual mean) – receptors: forests/natural vegetation; sensitive lichens; references: WHO, CLRTAP, AQ Directive.
  - Ammonia: 1 µg/m3 (lichens/bryophytes); 3 µg/m3 (other vegetation) – annual mean; references: CLRTAP.
- Linkages to NH3, NOX, and SO2 through habitat and potential species dependencies; use National Vegetation Classification (NVC) and site knowledge where possible.

## Data Resources and Structure
- Resource locator: http://www.apis.ac.uk/srcl
- Datasets (three CSVs):
  - APIS_SAC_feature_critical_load_level_linkages.csv
  - APIS_SPA_feature_critical_load_level_linkages.csv
  - APIS_SSSI_feature_critical_load_level_linkages.csv
- Core fields (examples):
  - INTERESTCODE, INTERESTNAME, INTERESTLAYNAME, INTERESTTYPECODE, INTERESTTYPE, NVC_CODE, APIS_NAME, BROAD_HABITATCODE, BROADHABITAT, DEPTYPE, SENSITIVENDEP
  - NCLCODE, NCLCLASS, JUSTIFICATIONALLOCATIONNCL, EUNIS, CLMIN_NUTN, CLMAX_NUTN, RECOMMENDED_VALUE, NTEXT
  - SENSITIVEACIDITY, ACCODE, ACIDITYCLASS, JUSTIFICATIONA, ATEXT
  - BRYOPHYTES, LICHENS, AMMONIA_CL_VALUE, AMMONIA_CL_TEXT, NITROGEN_DIOXIDE_CL_VALUE, NITROGEN_DIOXIDE_CL_TEXT, SULPHUR_DIOXIDE_CL_VALUE, SULPHUR_DIOXIDE_CL_TEXT
  - SPECIESSENSITIVEN, SPECIESSENSITIVITYN, JUSTIFYSPECIESSENSITIVITYN, SPECIESSENSITIVEA, SPECIESSENSITIVITYA, JUSTIFYSPECIESSENSITIVITYA
  - SPECIES_SENSITIVE_NH3, JUSTIF_SPECIES_SENSITIVE_NH3, SPECIES_SENSITIVE_NH3_TEXT, SPECIES_SENSITIVE_NOX, JUSTIF_SPECIES_SENSITIVE_NOX, SPECIES_SENSITIVE_NOX_TEXT, SPECIES_SENSITIVE_SO2, JUSTIF_SPECIES_SENSITIVE_SO2, SPECIES_SENSITIVE_SO2_TEXT

## How to Use in GIS
- Integrate the three linkages CSVs with corresponding SAC/SPA/SSSI feature layers in a GIS environment.
- Use:
  - Habitat codes (EUNIS, NVC) to join to feature attributes.
  - Recommended critical load/level values for each feature as map symbology or for filtering.
  - Justifications and notes to populate metadata/pop-up information.
- Visualize risk by overlaying deposition data, linking to features via the provided codes and classifications.
- Leverage the data to support policy, client, or public-facing map products, ensuring transparency through recorded justifications.

## Practical Notes for GIS Projects
- Ensure consistent use of EUNIS/BAP broad habitats and NVC codes when joining to features.
- Where mismatches occur, flag for further assessment or site-specific data integration.
- Use the exposure thresholds (loads and levels) to categorize features into risk classes for mapping and reporting.
- Reference APIS and the Noordwijkerhout framework to align with European-scale deposition assessments.

## Limitations and Considerations
- Some features may not have a direct one-to-one mapping to EUNIS or Broad Habitats; expert judgement may be required.
- Uncertainty exists in positive vs negative eutrophication effects on some species; document assumptions in GIS pop-ups or metadata.