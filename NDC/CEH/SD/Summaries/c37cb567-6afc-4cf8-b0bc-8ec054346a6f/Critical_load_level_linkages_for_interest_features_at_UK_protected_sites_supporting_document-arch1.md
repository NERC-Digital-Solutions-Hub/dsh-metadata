# Assigning Relevant Critical Loads/Levels to designated features of protected nature conservation sites

- Objective: Assign the most relevant critical loads and critical levels to designated features across protected sites (Annex I habitats, Annex II plant and non-plant species, SPA features, and A/SSSI habitats) to support understanding of impacts from atmospheric deposition.

## Phases of assignment
- Phase 1: Annex I habitat features and Annex II plant species features (plants treated as in situ components of habitat).
- Phase 2: Special Protection Area (SPA) bird features and Annex II non-plant species features (using the same method as SPA features for non-plant species).
- Phase 3: A/SSSI habitat features only.

## Critical loads for nutrient nitrogen
- Framework: Set under UNECE Convention on Long-Range Transboundary Air Pollution; based on empirical evidence from experiments and gradient studies.
- Habitat mapping: Empirical nitrogen critical loads linked to habitat classes in the European Nature Information System (EUNIS) to maintain consistent European terminology.
- Habitat correspondence: Use tables to relate EUNIS classes to Annex I features, A/SSSI features, or Annex II/SPA features.
- Sensitivity judgement: Experts assessed which features are sensitive to eutrophication; most are, with exceptions (e.g., estuaries, reefs, coastal lagoons).
- Linkages: Annex I features and Annex II plant features matched to appropriate EUNIS classes; justifications recorded for transparency.
- Uses Noordwijkerhout 2010 values: Critical load values, reliability, and potential exceedance impacts documented.

## Critical loads for acidity
- Basis: Soil- and habitat-type–driven; six Broad Habitats (e.g., acid calcareous gradients, bogs, montane, woodland).
- Habitat mapping: Use NBN/JNCC habitat correspondence tables to align Broad Habitats with Annex I features, A/SSSI features, or Annex II/SPA features.
- Sensitivity assessment: Expert evaluations by English Nature/Natural England, SNH, CEH; most features sensitive to acidification under deposition scenarios with buffering exceptions (coastal features with high base cation levels, calcareous features).
- Linkages: Annex I and Annex II features linked to corresponding acidity critical loads; transparency via justifications.
- Notes on exceedance: Justifications describe potential impacts; some features show resilience due to buffering.

## Exceptions in load assignment
- Non-matches: Annex I habitat features may not map to a suitable EUNIS class; may require further science review or site-by-site assessment.
- Documentation: Non-matches and site-specific adjustments are indicated in the dataset.

## Assigning critical loads for SPA features and Annex II non-plant species
- Direct effects on birds from nitrogen or acidity are minimal; instead, assess through habitat integrity and the likelihood of negative impacts on breeding, feeding, or roosting.
- Procedure: For each species, questions address relevant Broad Habitat, habitat sensitivity to eutrophication or acidification, potential impacts on viability, and whether to assign nitrogen or acidity critical loads based on the habitat context.
- Judgments: Based on best available science and Quality Control by statutory conservation bodies and CEH.
- Outcome: If the habitat is insensitive to acidity or eutrophication, no critical load is assigned for that feature.

## Critical Levels
- Scope: Not habitat-specific; applied to broad vegetation types (e.g., forest, arable, semi-natural) and specific receptors like lichens and bryophytes (ammonia).
- Values and references: 
  - NOX: Annual mean; 30 µg/m3 (WHO, CLRTAP, AQ Directive)
  - SO2: Annual mean; 20 µg/m3 for forests/natural vegetation; 10 µg/m3 for sensitive lichens
  - Ammonia: Annual mean; 1 µg/m3 (lichens/bryophytes); 3 µg/m3 (other vegetation; with 2–4 µg/m3 uncertainty range)
- Linkages: Where possible, connect habitat features with species via National Vegetation Classifications (NVC) and site knowledge to derive site-relevant levels for NH3, NO2, and SO2.

## Data and resources
- Resource locator: http://www.apis.ac.uk/srcl
- Data products: Datasets comprising critical loads and level linkages for SAC, SPA, and A/SSSI features.
- Data structure (three CSVs):
  - APIS_SAC_feature_critical_load_level_linkages.csv
  - APIS_SPA_feature_critical_load_level_linkages.csv
  - APIS_SSI_feature_critical_load_level_linkages.csv
- Key fields (example): INTERESTCODE, INTERESTNAME, INTERESTLAYNAME, INTERESTTYPECODE, INTERESTTYPE, NVC_CODE, APIS_NAME, BROAD_HABITATCODE, BROADHABITAT, DEPTYPE, SENSITIVENDEP, NCLCODE, NCLCLASS, JUSTIFICATIONALLOCATIONNCL, EUNIS, CLMIN_NUTN, CLMAX_NUTN, RECOMMENDED_VALUE, NTEXT, SENSITIVEACIDITY, ACCODE, ACIDITYCLASS, JUSTIFYSA, AMMONIA_CL_VALUE, AMMONIA_CL_TEXT, NITROGEN_DIOXIDE_CL_VALUE, NITROGEN_DIOXIDE_CL_TEXT, SULPHUR_DIOXIDE_CL_VALUE, SULPHUR_DIOXIDE_CL_TEXT, SPECIESSENSITIVEN, SPECIESSENSITIVITYN, JUSTIFYSPECIESSENSITIVITYN, SPECIESSENSITIVEA, SPECIESSENSITIVITYA, JUSTIFYSPECIESSENSITIVITYA, SPECIES_SENSITIVE_NH3, JUSTIF_SPECIES_SENSITIVE_NH3, SPECIES_SENSITIVE_NOX, JUSTIF_SPECIES_SENSITIVE_NOX, SPECIES_SENSITIVE_SO2, JUSTIF_SPECIES_SENSITIVE_SO2, etc.
- Purpose of datasets: Store relationships between interest features and empirical critical loads/levels, including justifications, sensitivity flags, and recommended values for case work.

## How this aligns with data practice for analysts
- Combines habitat expertise with empirical deposition science to derive site-relevant load/level assignments.
- Uses structured data schemas and explicit justifications to support reproducibility and auditability.
- Acknowledges data gaps and exceptions, with guidance for site-by-site or science-review updates when mappings are imperfect.
- Emphasizes traceability to data sources (EUNIS, NVC, Noordwijkerhout/Noordwijkerhout 2010, CLRTAP/WHO references) and transparent quality control.