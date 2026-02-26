# Assigning Relevant Critical Loads/Levels to designated features of protected nature conservation sites

## Overview
- Purpose: Assign relevant critical loads and critical levels to designated features of protected sites to assess impacts from atmospheric nitrogen and acidity.
- Scope: Covers Annex I habitat features, Annex II plant species features (treated as in situ and part of habitat), Annex II non-plant species features (via habitat-based assessment), SPA features, and England-only SSSI habitat features.
- Aim of approach: Link empirical critical loads/levels to site features through habitat classifications and expert judgement, enabling impact assessment and management decisions.

## Phases of assignment
- Phase 1: Assign Annex I habitat features and Annex II plant species features (plant features treated as part of the habitat).
- Phase 2: Assign SPA bird features and Annex II non-plant species features using the same methodology as SPA features.
- Phase 3: Assign SSSI habitat features (England only).

## Critical loads for nutrient nitrogen
- Framework: Set under UNECE Long-Range Transboundary Air Pollution conventions; empirical loads from experiments and gradient studies.
- Habitat linkage: Empirical nitrogen critical loads are assigned to habitat classes in EUNIS to maintain consistent terminology across Europe.
- Mapping: Use habitat correspondence tables to relate EUNIS classes to Annex I, A/SSSI, or Annex II/SPA features.
- Sensitivity and justification: Assess feature sensitivities to eutrophication; document justifications and reliability; note that only a minority of habitats are not sensitive.
- Reference values: Based on Noordwijkerhout Expert Workshop (2010); record critical load values, reliability, and potential exceedance impacts.

## Critical loads for acidity
- Basis: Derived from soil and habitat types across six Broad Habitats (e.g., acid grassland, calcareous grassland, dwarf shrub heath, bogs, montane, unmanaged woodlands).
- Mapping: Use JNCC/NBN habitat correspondence tables to assign acidity critical loads to respective Annex I/A/SSSI/Annex II features.
- Sensitivity assessment: Conducted by experts; coastal features and calcareous features may be less sensitive due to buffering; document justification and impacts.
- Linkage: Match Annex I/Annex II features to Broad Habitats and record the appropriate acidity critical loads with justification.

## Exceptions
- Some Annex I features may not match an appropriate EUNIS class; may require further science-based investigation or site-by-site assessment.
- Non-matches are indicated in the dataset; additional work may be needed for sensible critical load estimation.

## Assigning critical loads for SPA features and Annex II non-plant species
- Indirect approach for birds: Direct nitrogen/acidity loads to birds are rare/unreliable; instead infer potential impacts via habitat integrity on breeding/feeding/roosting.
- Methodology: Apply habitat-based critical load reasoning using expert judgments aligned with species-specific conservation objectives; QC by other conservation scientists.
- Insensitive habitats: If the habitat is deemed insensitive to either acidity or eutrophication, no critical load is assigned.
- Species-specific steps: For each species, determine relevant Broad Habitat, assess sensitivity to eutrophication and acidity, evaluate impacts on breeding/feeding/roosting, consider potential positive effects, and assign the most relevant nutrient nitrogen or acidity critical loads with documented justifications.

## Critical Levels
- Nature: Not habitat-specific; set to cover broad vegetation types (e.g., forest, arable, semi-natural) and include ammonia-sensitive lichens and bryophytes.
- Specific values (examples):
  - NOX: Receptor = All; Time period = Annual mean; Critical level = 30 µg/m3; References = WHO, CLRTAP, AQ Directive.
  - SO2: Receptor = Forests and natural vegetation; Time period = Annual mean; Critical level = 20 µg/m3; Receptors for sensitive lichens; References = WHO, CLRTAP, AQ Directive.
  - Ammonia: Receptor = Lichens and bryophytes (key ecosystem components); Time period = Annual mean; Critical level = 1 µg/m3; Receptor = Other vegetation; Time period = Annual mean; Critical level = 3 µg/m3 (uncertainty 2–4 µg/m3); References = CLRTAP.
- Linkages: Where possible, align habitat-level levels with site-relevant levels for ammonia, NO2, and SO2 using National Vegetation Classifications (NVC) and site knowledge.

## Data, linkages, and access
- Resource locator: APIS website provides access to the critical loads linkages and related data.
- Datasets (three CSVs):
  - APIS_SAC_sites_feature_critical_load_linkages.csv
  - APIS_SPA_sites_feature_critical_load_linkages.csv
  - APIS_SSSI_sites_feature_critical_load_linkages.csv

## Data structure and fields (summary)
- Key identifiers: SITECODE, SITENAME, COUNTRY, DESIGNATION (SAC/SPA/SSSI).
- Interest/features: INTERESTCODE, INTERESTNAME, INTERESTLAYNAME, INTERESTTYPECODE, INTERESTTYPE.
- Habitat/classification: NVC_CODE, BROAD_HABITATCODE, BROADHABITAT, DEPTYPE, SENSITIVENDEP.
- Critical load/level metadata: NCLCODE, NCLCLASS, JUSTIFICATIONALLOCATIONNCL, EUNIS, CLMIN_NUTN, CLMAX_NUTN, RECOMMENDED_VALUE, NTEXT.
- Acidification and nitrogen sensitivity: SENSITIVEACIDITY, ACCODE, ACIDITYCLASS, JUSTIFICATIONA, ATEXT.
- Species sensitivity fields (when applicable): SPECIESSENSITIVEN, SPECIESSENSITIVITYN, JUSTIF_SPECIESSENSITIVITYN, SPECIES_SENSITIVE_NH3-related fields, SPECIES_SENSITIVE_NOX-related fields, SPECIES_SENSITIVE_SO2-related fields, and corresponding justification fields.
- Additional notes: AMMONIA_CL_VALUE/AMMONIA_CL_TEXT, NITROGEN_DIOXIDE_CL_VALUE/NITROGEN_DIOXIDE_CL_TEXT, SULPHUR_DIOXIDE_CL_VALUE/SULPHUR_DIOXIDE_CL_TEXT, and related explanatory text fields for site-level decision support.

## Data quality and outputs
- Outputs are designed to support self-serve data exploration and informed decision-making for land management and conservation planning.
- Outputs include transparent justification records to support reproducibility and potential updates as new science becomes available.
- Emphasis on documenting when no critical load is assigned due to habitat insensitivity.