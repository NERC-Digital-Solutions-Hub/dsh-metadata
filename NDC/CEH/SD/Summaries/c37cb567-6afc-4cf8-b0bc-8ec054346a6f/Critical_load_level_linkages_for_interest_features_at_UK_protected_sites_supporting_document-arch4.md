# Assigning Relevant Critical Loads/Levels to designated features of protected nature conservation sites

- Purpose: Outline the method for assigning relevant critical loads and critical levels to designated features within protected nature conservation sites, across multiple feature types and phases.

## Phases of assignment

- Phase 1: Annex I habitat features and Annex II plant species features ( Annex II features grouped as they are in situ and part of the habitat).
- Phase 2: Special Protection Area (SPA) bird features and Annex II non-plant species features, using the same method as SPA features.
- Phase 3: A/SSSI habitat features only.

## Critical loads for nutrient nitrogen

- Governed by the UNECE Convention on Long-Range Transboundary Air Pollution.
- Based on empirical evidence from experiments and gradient studies.
- Assigned to habitat classes of the European Nature Information System (EUNIS) to ensure consistent habitat terminology across Europe.
- Use habitat correspondence tables to relate EUNIS classes to interest features (Annex I, A/SSSI, Annex II/SPA).
- Sensitivity judgments to eutrophication are made; most features are assessed, with transparency notes for those not sensitive.
- Link Annex I/Annex II plant features to the most suitable EUNIS class; Noordwijkerhout Expert Workshop (2010) values and impacts documented.
- Justifications are recorded for transparency and consistency.

## Critical loads for acidity

- Based on soil and habitat types across six Broad Habitats (e.g., acid/calcareous grasslands, dwarf shrub heath, bogs, montane, woodland).
- Assigned using NBN/JNCC habitat correspondence tables to match Annex I/A/SSSI/ANNEX II features.
- Designated features assessed for sensitivity to acidification via expert judgment from English Nature, SNH, and CEH.
- Coastal features and calcareous features often less sensitive due to buffering; examples of not sensitive include certain estuaries, reefs, coastal lagoons, limestone pavements, and alkaline fens.
- Once sensitivity is established, match Annex I/Annex II features to corresponding acidity critical loads; justification level and expected impacts are recorded.

## Exceptions in nitrogen and acidity loads

- Some Annex I habitat features may not align with any suitable EUNIS class; further science review may yield a better estimate.
- Non-matches are indicated, and in some cases site-by-site assessments are used.

## Assigning critical loads for SPA features and Annex II non-plant species

- Direct assignment of nitrogen/acidity loads to bird or non-plant species is generally unsuitable.
- Use habitat integrity to infer potential impacts on birds and other species; assess whether habitat-level impacts could affect breeding, feeding, or roosting viability.
- Expert judgments are based on generic conservation objectives and QC by statutory bodies and CEH.
- If the habitat is deemed insensitive to acidity or eutrophication, no critical load is assigned.

## Species-focused assessment process

- For each species, follow a series of questions:
  1. Identify the relevant BAP Broad Habitat the species depends on (could be multiple habitats).
  2. Determine if that habitat is sensitive to eutrophication or acidification.
  3. Assess potential impacts on habitat viability related to the species’ breeding, feeding, or roosting.
  4. Consider both positive and negative potential effects of eutrophication; note uncertainty.
  5. If potential negative effects exist, assign the most relevant nutrient nitrogen or acidity critical load based on the habitat.

## Critical Levels

- Not habitat-specific; applicable to broad vegetation types (e.g., forest, arable, semi-natural) with specific attention to sensitive lichens and bryophytes for ammonia.
- Specified values:
  - NOX: Annual mean, receptor All, CL 30 µg/m3; references WHO, CLRTAP, AQ Directive.
  - SO2: Annual mean, receptors Forests/Natural Vegetation; various receptors (e.g., sensitive lichens) with limits (20 µg/m3, 10 µg/m3 respectively) and references (WHO, CLRTAP, AQ Directive).
  - Ammonia: Annual mean; receptor categories include lichens/bryophytes and other vegetation; values 1 µg/m3 and 3 µg/m3 (uncertainty range 2–4 µg/m3); CLRTAP references.
- Linkages created between habitat and species where possible, using National Vegetation Classifications (NVC) and site knowledge.

## Linkages and data sources

- Linkages established between habitats and species wherever possible to provide site-relevant critical loads for ammonia, nitrogen dioxide, and sulphur dioxide.
- NVC and site knowledge used to inform linkage decisions.

## Data resources and access

- Resource locator: http://www.apis.ac.uk/srcl
- Fieldwork/lab instrumentation: NA
- Calibration/values: NA
- Data nature/units: NA
- Analytical methods: NA
- Quality control: NA

## Data structure and datasets

- Three datasets covering critical loads and level linkages for UK nature sites (SAC, SPA, A/SSSI):
  - APIS_SAC_feature_critical_load_level_linkages.csv
  - APIS_SPA_feature_critical_load_level_linkages.csv
  - APIS_SSSI_feature_critical_load_level_linkages.csv
- Common columns include:
  - INTERESTCODE, INTERESTNAME, INTERESTLAYNAME
  - INTERESTTYPECODE, INTERESTTYPE
  - NVC_CODE, APIS_NAME, BROAD_HABITATCODE, BROADHABITAT
  - DEPTYPE (deposition type: F, M, G)
  - SENSITIVENDEP
  - NCLCODE, NCLCLASS, JUSTIFICATIONALLOCATIONNCL
  - EUNIS, CLMIN_NUTN, CLMAX_NUTN, RECOMMENDED_VALUE, NTEXT
  - SENSITIVEACIDITY, ACCODE, ACIDITYCLASS, JUSTIFYA
  - BRYOPHYTES, LICHENS
  - AMMONIA_CL_VALUE, AMMONIA_CL_TEXT
  - NITROGEN_DIOXIDE_CL_VALUE, NITROGEN_DIOXIDE_CL_TEXT
  - SULPHUR_DIOXIDE_CL_VALUE, SULPHUR_DIOXIDE_CL_TEXT
  - SPECIESSENSITIVEN, SPECIESSENSITIVITYN, JUSTIFYSPECIESSENSITIVITYN
  - SPECIESSENSITIVEA, SPECIESSENSITIVITYA, JUSTIFYSPECIESSENSITIVITYA
  - SPECIES_SENSITIVE_NH3, JUSTIF_SPECIES_SENSITIVE_NH3, SPECIES_SENSITIVE_NH3_TEXT
  - SPECIES_SENSITIVE_NOX, JUSTIF_SPECIES_SENSITIVE_NOX, SPECIES_SENSITIVE_NOX_TEXT
  - SPECIES_SENSITIVE_SO2, JUSTIF_SPECIES_SENSITIVE_SO2, SPECIES_SENSITIVE_SO2_TEXT
  - SPECIES_SENSITIVITY_NH3, SPECIES_SENSITIVITY_NOX, SPECIES_SENSITIVITY_SO2, JUSTIF_SPECIES_SENSITIVITY
- These datasets capture the relationships between designated features and their assigned critical loads/levels, with detailed justification and notes.