# Assigning Relevant Critical Loads/Levels to designated features of protected nature conservation sites

- Purpose: Establish critical loads and critical levels for nitrogen and acidity to designated features of protected sites (SAC, SPA, SSSI in England) to assess environmental health and policy performance over time.
- Structure: Describes phased methodology, data mappings, expert judgments, and data products used for monitoring and reporting.

## Phases of assigning critical loads

- Phase 1: Assign to Annex I habitat features and Annex II plant species features. Annex II plant features are treated as in situ habitat components and combined with habitat features.
- Phase 2: Assign to SPA bird features and Annex II non-plant species features using a unified approach with SPA features.
- Phase 3: Assign to SSSI habitat features (England only).

## Critical loads for nutrient nitrogen

- Basis: Empirical critical loads derived under UNECE Long-Range Transboundary Air Pollution, linked to habitat classes in the European Nature Information System (EUNIS) to ensure consistent European terminology.
- Method: Use habitat correspondence tables to relate EUNIS classes to interest features (Annex I, A/SSSI, Annex II/SPA). Assess sensitivities to eutrophication from atmospheric deposition.
- Process: Link Annex I features and Annex II plant features to the most suitable EUNIS class; record justifications for transparency. Use Noordwijkerhout Expert Workshop (2010) values, noting reliability and potential exceedance impacts.
- Exceptions: If no suitable EUNIS match exists, document non-matches and potentially conduct site-by-site assessments to derive sensible estimates.

## Critical loads for acidity

- Basis: Critical loads based on soil and habitat types across six Broad Habitats (e.g., acid calcareous grasslands, bogs, woodlands). Use NBN/JNCC habitat correspondence to assign Broad Habitats to designated features.
- Method: Assess sensitivity of features to acidification; coastal features with strong buffering may be non-sensitive. Match Annex I and Annex II features to corresponding Broad Habitats and record justifications and potential impacts of exceedance.
- Exceptions: Similar to nitrogen, where matches are not available or robust, additional evaluation may be required.

## Exceptions and special cases

- Annex I features may not always map to a suitable EUNIS class; provide alternative investigations or site-by-site assessments.
- For SPA features and Annex II non-plant species, direct nitrogen or acidity effects on birds or non-plant species are typically unlikely; assessment relies on habitat-bird/species relationships and potential impacts on breeding, feeding, or roosting.

## Critical Levels and linkage to species/habitat

- Critical levels are not habitat-specific like loads; they apply to broad vegetation types and sensitive components (e.g., lichens, bryophytes, ammonia effects).
- Specific values include:
  - NOX: receptor = all; annual mean; 30 µg/m3 (WHO, CLRTAP, AQ Directive)
  - SO2: receptor = forests/natural vegetation; annual mean; 20 µg/m3
  - SO2: receptor = sensitive lichens; annual mean; 10 µg/m3
  - Ammonia: receptor = lichens/bryophytes; annual mean; 1 µg/m3
  - Ammonia: receptor = other vegetation; annual mean; 3 µg/m3 (uncertainty 2–4 µg/m3)
- Linkages: When possible, align habitat and species to provide site-relevant critical levels for ammonia, NO2, and SO2 using National Vegetation Classifications (NVC) and site knowledge.
- Species-specific process: For SPA birds and Annex II non-plant species, apply a structured set of questions to determine if habitat sensitivity to eutrophication or acidification warrants a critical load/level assignment.

## Data products and structure

- Output datasets (three CSVs):
  - APIS_SAC_sites_feature_critical_load_linkages.csv
  - APIS_SPA_sites_feature_critical_load_linkages.csv
  - APIS_SSSI_sites_feature_critical_load_linkages.csv
- Key fields include: SITECODE, SITENAME, COUNTRY, DESIGNATION, INTERESTCODE, INTERESTNAME, INTERESTLAYNAME, INTERESTTYPECODE, INTERESTTYPE, NVC_CODE, BROADHABITAT, NCLCODE/NCLCLASS, JUSTIFICATIONALLOCATIONNCL, EUNIS, CLMIN_NUTN, CLMAX_NUTN, RECOMMENDED_VALUE, NTEXT, SENSITIVEACIDITY, AMMONIA_CL_VALUE, NITROGEN_DIOXIDE_CL_VALUE, SULPHUR_DIOXIDE_CL_VALUE, multiple sensitivity and justification fields, and species-specific sensitivity indicators.
- Purpose of datasets: store site-by-site critical loads/levels, justifications, and linked habitat/species information to support monitoring, QA, and portal-based data sharing.

## Data provenance and quality

- Data are anchored in established international and national frameworks (UNECE, EUNIS, NBN/JNCC, Noordwijkerhout 2010) with transparent justifications.
- Quality control involves expert judgement from English Nature/Natural England, SNH, CEH, and other statutory bodies; where uncertainties exist, they are documented.
- Datasets are prepared for standardised storage and upload to appropriate monitoring portals to support consistent environmental health assessment over time.