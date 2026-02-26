# Assigning Relevant Critical Loads/Levels to designated features of protected nature conservation sites

## Overview
- Describes a methodology to assign critical loads and critical levels to designated conservation features to support environmental policy scrutiny, monitoring, and decision-making.
- Targets UK sites across SACs, SPAs, and SSSIs; aims to link atmospheric deposition to habitat/species integrity and inform management.

## Phases of assignment
- Phase 1: Annex I habitat features and Annex II plant species features.
  - Annex II plant features treated as in situ components of habitat rather than mobile Annex II species.
- Phase 2: SPA bird features and Annex II non-plant species features.
  - Uses the same method as for SPA features.
- Phase 3: SSSI habitat features (England only).

## Critical loads for nutrient nitrogen
- Based on empirical evidence from experiments and targeted gradient studies.
- Assigned to habitat classes in the European Nature Information System (EUNIS) to ensure consistent terminology across Europe.
- Habitat correspondence tables determine relationships between EUNIS classes and Annex I/A-SSSI features or Annex II/SPA features.
- Sensitivity assessment:
  - Most features are judged sensitive to eutrophication from atmospheric deposition.
  - Some coastal/coastal lagoon features and certain calcareous features show lower sensitivity due to buffering.
- Justifications documented for transparency and consistency.
- Uses critical loads defined at Noordwijkerhout Expert Workshop (2010); notes reliability and potential impacts of exceedance.

## Critical loads for acidity
- Based on soil and habitat types across six Broad Habitats (e.g., acid grassland, calcareous grassland, dwarf shrub heath, bogs, montane, unmanaged woodland).
- Habitat correspondence tables (NBN/JNCC) map Broad Habitats to Annex I/A-SSSI or Annex II/SPA features.
- Sensitivity assessment by experts (Natural England, SNH, CEH):
  - Generally, many features are sensitive to acidification where deposition is high or soils have low buffering.
  - Coastal features with high base cation levels and calcareous features often not sensitive due to buffering.
- Annex I habitat and Annex II plant features linked to corresponding aciditycritical loads.
- Justifications for the match and impacts of exceedance recorded.

## Exceptions
- Some Annex I features do not map neatly to a suitable EUNIS class; may require further science review or site-by-site assessment.
- Non-matches are indicated in the dataset; where relevant, site-by-site work may be invoked.

## Assigning critical loads for SPA features and Annex II non-plant species
- Direct effects of nitrogen and acidity on bird/non-plant species are rare; focus on habitat impact on species viability.
- Process involves assessing whether habitat sensitivity to eutrophication or acidification could affect breeding, feeding, or roosting.
- If the habitat is deemed insensitive, no critical load is assigned for the corresponding species.
- For each species, a sequence of questions is applied:
  1) Identify the relevant broad habitat (BAP) the species relies on.
  2) Assess whether that habitat is sensitive to eutrophication or acidification.
  3) Evaluate potential impacts on breeding, feeding, or roosting viability.
  4) Document expert judgments and note uncertainties, including possible positive effects (e.g., increased food supply) versus negative effects.
  5) If negative effects are possible, assign the most relevant nutrient nitrogen or acidity critical load based on the habitat, with similar justification as for Annex I features.

## Critical Levels
- Not habitat-specific; set for broad vegetation types and certain sensitive organisms (e.g., lichens, bryophytes) for ammonia.
- Specific values listed:
  - NOX: Receptor = All; Time = Annual mean; Critical Level = 30 µg/m3; References = WHO, CLRTAP, AQ Directive.
  - SO2: Receptor = Forests and natural vegetation; Time = Annual mean; Critical Level = 20 µg/m3; References = WHO, CLRTAP, AQ Directive.
  - SO2: Receptor = Sensitive lichens; Time = Annual mean; Critical Level = 10 µg/m3; Reference = WHO.
  - Ammonia: Receptor = Lichens and bryophytes; Time = Annual mean; Critical Level = 1 µg/m3.
  - Ammonia: Receptor = Other vegetation; Time = Annual mean; Critical Level = 3 µg/m3 (uncertainty range 2–4 µg/m3); Reference = CLRTAP.
- Linkages established between habitat and species where possible, using National Vegetation Classifications (NVC) and site knowledge.

## Linkages and data interpretation
- Linkages made between habitat features and species where possible to provide site-relevant critical loads/levels for nitrogen compounds (ammonia, NOX) and sulfur dioxide.
- Emphasis on integrating habitat classification (EUNIS, NVC) with species requirements to support decision-making.

## Resource locators
- APIS (Assessing Policy Impacts on Species) resource URL provided for methodology and data context.

## Fieldwork, instrumentation, and quality control
- Fieldwork/instrumentation sections marked NA, implying reliance on existing datasets and established classifications.
- Quality control and analytical method fields are NA in the data context.

## Details of data structure
- Three datasets capture critical loads/levels for designated features across the UK’s SAC, SPA, and England-only SSSI networks:
  - APIS_SAC_sites_feature_critical_load_linkages.csv
  - APIS_SPA_sites_feature_critical_load_linkages.csv
  - APIS_SSSI_sites_feature_critical_load_linkages.csv
- Key columns include:
  - SITECODE, SITENAME, COUNTRY, DESIGNATION, INTERESTCODE, INTERESTNAME, INTERESTLAYNAME, INTERESTTYPECODE, INTERESTTYPE, NVC_CODE, APIS_NAME, BROAD_HABITATCODE, BROADHABITAT, DEPTYPE (deposition type), SENSITIVENDEP, NCLCODE, NCLCLASS, JUSTIFICATIONALLOCATIONNCL, EUNIS, CLMIN_NUTN, CLMAX_NUTN, RECOMMENDED_VALUE, NTEXT, SENSITIVEACIDITY, ACCODE, ACIDITYCLASS, JUSTIFICATIONA, ATEXT, BRYOPHYTES, LICHENS, AMMONIA_CL_VALUE, AMMONIA_CL_TEXT, NITROGEN_DIOXIDE_CL_VALUE, NITROGEN_DIOXIDE_CL_TEXT, SULPHUR_DIOXIDE_CL_VALUE, SULPHUR_DIOXIDE_CL_TEXT, SPECIESSENSITIVEN, SPECIESSENSITIVITYN, JUSTIFYSPECIESSENSITIVITYN, SPECIESSENSITIVEA, SPECIESSENSITIVITYA, JUSTIF_SPECIES_SENSITIVE_NOX, SPECIES_SENSITIVE_NOX_TEXT, SPECIES_SENSITIVE_SO2, JUSTIF_SPECIES_SENSITIVE_SO2, SPECIES_SENSITIVE_SO2_TEXT.
- The dataset schema supports multi-feature associations (e.g., a species may depend on more than one broad habitat).

## Summary for monitoring framework authors
- The document presents a structured, phase-based approach to attributing atmospheric deposition impacts to protected features, enabling policy-relevant monitoring and reporting.
- It integrates empirical nitrogen loading data with habitat classifications (EUNIS/NVC) and expert judgments to determine where critical loads/levels should be applied.
- It emphasizes transparency through justifications, explicit handling of exceptions, and clear linkage between habitat features and species wherever feasible.
- Data products are designed for integration into monitoring systems, with explicit dataset structures and fields to support interoperability and governance considerations.