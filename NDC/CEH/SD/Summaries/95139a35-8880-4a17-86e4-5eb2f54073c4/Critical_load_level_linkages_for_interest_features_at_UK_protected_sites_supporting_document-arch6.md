# Assigning Relevant Critical Loads/Levels to designated features of protected nature conservation sites

## Overview
- Describes methodology to assign relevant critical loads and critical levels to designated features within the UK's SACs, SPAs, and A/SSSIs.
- Utilises three linked datasets that map features to nitrogen and acidity thresholds, aiding policy, site management, and conservation decisions.
- Bases loads/levels on empirical evidence, habitat classifications, and expert judgement, with transparency and traceability.

## Phases of assignment
- Phase 1: Annex I habitat features and Annex II plant species features (plant species treated as part of habitat in situ).
- Phase 2: Special Protection Area (SPA) bird features and Annex II non-plant species features (using the same method as for SPA features).
- Phase 3: A/SSSI habitat features only.

## Critical loads for nutrient nitrogen
- Derived under UNECE LRTAP; based on empirical evidence from experiments and gradient studies.
- Assigned to habitat classes from the European Nature Information System (EUNIS) to ensure consistent habitat terminology across Europe.
- Habitat correspondence tables link EUNIS classes to the interest features (Annex I, Annex II/SPA, A/SSSI habitats).
- Sensitivity assessments determine which features may be affected by eutrophication; many features show sensitivity, others (e.g., certain coastal estuaries) may not.
- For features that do not map directly to an appropriate EUNIS class, non-matches are flagged and may require site-by-site assessment.

## Critical loads for acidity
- Based on soil and habitat types across six Broad Habitats (e.g., acid grassland, calcareous grassland, etc.).
- Uses NBN/JNCC habitat correspondences to assign acidity critical loads to Annex I/A/SSSI/Annex II features.
- Sensitivity assessments by specialists indicate potential impacts of acid deposition; coastal features with high buffering are often not sensitive.
- As with nitrogen, feature-to-Broad Habitat mappings are documented with justification.

## Critical levels (air-borne pollutants)
- Not habitat-specific; defined for broad vegetation types and notable for lichens and bryophytes (and other vegetation).
- Key values (annual mean):
  - NOX: 30 µg/m3 (receptor: All; WHO/CLRTAP/AQ Directive reference)
  - SO2: 20 µg/m3 (receptor: Forests/natural vegetation); 10 µg/m3 for sensitive lichens
  - Ammonia: 1 µg/m3 (lichens/bryophytes); 3 µg/m3 (other vegetation; range 2–4 µg/m3)
- Where possible, site-relevant linkages between habitats, species, and these levels are established using National Vegetation Classifications (NVC) and site knowledge.

## Exceptions and notes
- Some Annex I features may not map to a suitable EUNIS class; may require updated science or site-by-site assessment.
- For birds and some Annex II non-plant species, critical loads are inferred from the habitat's sensitivity and potential impacts on breeding/feeding/roosting rather than direct deposition effects.

## Data products and structure
- Three CSV datasets:
  - APIS_SAC_feature_critical_load_level_linkages.csv
  - APIS_SPA_feature_critical_load_level_linkages.csv
  - APIS_SSSI_feature_critical_load_level_linkages.csv
- Core fields (examples):
  - INTERESTCODE, INTERESTNAME, INTERESTLAYNAME, INTERESTTYPECODE/NAME
  - NVC_CODE, APIS_NAME, BROAD_HABITATCODE/NAME
  - DEPTYPE (deposition type)
  - SENSITIVENDEP, NCLCODE, NCLCLASS
  - JUSTIFICATIONALLOCATIONNCL, EUNIS, CLMIN_NUTN, CLMAX_NUTN, RECOMMENDED_VALUE
  - NTEXT, SENSITIVEACIDITY, ACODE/ACIDITYCLASS, JUSTIFICATIONA, ATEXT
  - BRYOPHYTES, LICHENS
  - AMMONIA_CL_VALUE/TEXT, NITROGEN_DIOXIDE_CL_VALUE/TEXT
  - SULPHUR_DIOXIDE_CL_VALUE/TEXT
  - SPECIESSENSITIVEN, SPECIESSENSITIVITYN, JUSTIFYSPECIESSENSITIVITYN
  - SPECIESSENSITIVEA, SPECIESSENSITIVITYA, JUSTIFYSPECIESSENSITIVITYA
  - SPECIES_SENSITIVE_NH3, JUSTIF_SPECIES_SENSITIVE_NH3, SPECIES_SENSITIVE_NH3_TEXT
  - SPECIES_SENSITIVE_NOX, JUSTIF_SPECIES_SENSITIVE_NOX, SPECIES_SENSITIVE_NOX_TEXT
  - SPECIES_SENSITIVE_SO2, JUSTIF_SPECIES_SENSITIVE_SO2, SPECIES_SENSITIVE_SO2_TEXT
- Purpose of datasets: enable site-level assignment of appropriate nitrogen and acidity critical loads and associated levels to designated features, linking habitats, species, and deposition contexts for decision-making and policy support.

## Data sources and references
- Core basis: UNECE NOX/NOx, SO2, and ammonia deposition frameworks; Noordwijkerhout Expert Workshop (2010) for critical loads.
- Habitat classifications: EUNIS, National Vegetation Classification (NVC).
- National partners: APIS, JNCC, NBN, English Nature/Natural England, SNH, CEH.
- Resource locator: http://www.apis.ac.uk/srcl

## How this supports data use and decision making
- Translates complex ecological-deposition science into structured data products that can be integrated into planning tools and dashboards.
- Provides transparent justifications and traceable mappings from features to loads/levels, supporting risk assessments and compliance with environmental policies.
- Enables both broad assessments and site-specific analyses through explicit handling of non-matches and exceptions.