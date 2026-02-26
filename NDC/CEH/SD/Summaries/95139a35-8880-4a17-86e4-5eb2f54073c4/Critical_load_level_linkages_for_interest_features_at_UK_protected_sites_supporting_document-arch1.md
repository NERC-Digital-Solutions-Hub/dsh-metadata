# Assigning Relevant Critical Loads/Levels to designated features of protected nature conservation sites

## Aim and overall approach
- Objective: assign the most relevant critical loads and critical levels to designated features (habitats, birds, non-plant species) within UK protected sites (SAC, SPA, A/SSSI).
- Multi-phase methodology to align features with appropriate load/level values and support consistent interpretation across Europe.

## Phases of assignment
- Phase 1: Annex I habitat features and Annex II plant species features (Annex II plant features treated as in situ habitat; other Annex II species treated separately).
- Phase 2: Special Protection Area (SPA) bird features and Annex II non-plant species features; method mirrors SPA feature approach.
- Phase 3: A/SSSI habitat features only.

## Critical loads for nutrient nitrogen
- Basis: UNECE Convention on Long-Range Transboundary Air Pollution; empirical loads from experiments and gradient studies.
- Habitat mapping: empirical nitrogen critical loads linked to EUNIS habitat classes; habitat correspondence tables connect EUNIS to interest features (Annex I, A/SSSI, Annex II/SPA).
- Sensitivity judgement: expert assessment of eutrophication sensitivity for designated features; most features considered sensitive, with some coastal or calcareous features deemed not sensitive due to buffering.
- Process: assign the relevant nitrogen critical load to the feature via its associated broad habitat; document justification for transparency.
- Key reference values (illustrative examples):
  - Noordwijkerhout Expert Workshop (UNECE 2010) as a basis; note reliability and potential exceedance impacts.
- Exceptions: where Annex I features do not map to a suitable EUNIS class; may require further scientific investigation or site-by-site assessment.

## Critical loads for acidity
- Basis: soil and habitat types; six Broad Habitats (e.g., acid grassland, calcareous grassland, dwarf shrub heath, bogs, montane, unmanaged woodlands).
- Mapping: use NBN/JNCC habitat correspondence tables to assign Broad Habitats to Annex I features, A/SSSI features, or Annex II/SPA features.
- Sensitivity assessment: expert judgement; most features potentially impacted by deposition if soil buffering is low; coastal features with high buffering often not sensitive; some calcareous features also buffered.
- Process: match Annex I and Annex II features to corresponding acidity critical loads; record justification and expected impact of exceedance.
- Exceptions: non-matches or gaps addressed via additional investigation or site-specific assessment.

## Assigning critical loads for SPA features and Annex II non-plant species
- Direct nitrogen/acidity effects on birds and some non-plant species are rare; instead, link to habitat integrity to infer potential impacts on breeding, feeding, or roosting.
- Procedure: for each species, evaluate:
  1) Relevant Broad Habitat for the species (e.g., breeding/feeding/roosting habitat).
  2) Habitat sensitivity to eutrophication or acidification.
  3) Potential impacts on species viability; consider both positive and negative effects (e.g., increased food supply vs. detrimental ecological changes).
  4) If negative impacts are likely, assign the most relevant nutrient nitrogen or acidity critical load based on the habitat.
  5) Document similar justifications as for Annex I features and note the resulting critical load values and impacts.

## Critical Levels
- Not habitat-specific like critical loads; set to broad vegetation types (e.g., forest, arable, semi-natural) with specific values for sensitive lichens and bryophytes (ammonia context).
- Example values:
  - NOx: Receptor = All; Time Period = Annual mean; Critical Level = 30 µg/m3 (Reference: WHO, CLRTAP, AQ Directive).
  - SO2: Receptor = Forests and natural vegetation; Time Period = Annual mean; Critical Level = 20 µg/m3; Receptor = Sensitive lichens; Time Period = Annual mean; Critical Level = 10 µg/m3 (Reference: WHO).
  - Ammonia: Receptor = Lichens and bryophytes (key ecosystem components); Time Period = Annual mean; Critical Level = 1 µg/m3; Receptor = Other vegetation; Time Period = Annual mean; Critical Level = 3 µg/m3 (uncertainty range 2–4 µg/m3) (Reference: CLRTAP).
- Linkages: where possible, connect habitat types to species to provide site-relevant ammonia, NOx, and SO2 critical levels; guided by National Vegetation Classification (NVC) and site knowledge.

## Data resources and structure
- Resource location: APIS (Air Pollution Information System) – SCRL data resource link provided.
- Datasets (three CSVs) detailing critical loads/levels linkages for designated interest features:
  - APIS_SAC_feature_critical_load_level_linkages.csv
  - APIS_SPA_feature_critical_load_level_linkages.csv
  - APIS_SSSI_feature_critical_load_level_linkages.csv
- Key fields (examples):
  - INTERESTCODE, INTERESTNAME, INTERESTLAYNAME, INTERESTTYPECODE, INTERESTTYPE, NVC_CODE, APIS_NAME, BROAD_HABITATCODE, BROADHABITAT, DEPTYPE, SENSITIVENDEP, NCLCODE, NCLCLASS, JUSTIFICATIONALLOCATIONNCL, EUNIS, CLMIN_NUTN, CLMAX_NUTN, RECOMMENDED_VALUE, NTEXT, SENSITIVEACIDITY, ACCODE, ACIDITYCLASS, JUSTIFYSA, ATEXT, BRYOPHYTES, LICHENS, AMMONIA_CL_VALUE, AMMONIA_CL_TEXT, NITROGEN_DIOXIDE_CL_VALUE, NITROGEN_DIOXIDE_CL_TEXT, SULPHUR_DIOXIDE_CL_VALUE, SULPHUR_DIOXIDE_CL_TEXT, SPECIESSENSITIVEN, SPECIESSENSITIVITYN, JUSTIFYSPECIESSENSITIVITYN, SPECIESSENSITIVEA, SPECIESSENSITIVITYA, JUSTIFYSPECIESSENSITIVITYA, SPECIES_SENSITIVE_NH3, JUSTIF_SPECIES_SENSITIVE_NH3, SPECIES_SENSITIVE_NH3_TEXT, SPECIES_SENSITIVE_NOX, JUSTIF_SPECIES_SENSITIVE_NOX, SPECIES_SENSITIVE_NOX_TEXT, SPECIES_SENSITIVE_SO2, JUSTIF_SPECIES_SENSITIVE_SO2, SPECIES_SENSITIVE_SO2_TEXT.
- Additional notes: field types include qualitative justifications and site-specific annotations; links to NVC codes and APIS habitat names support crosswalks between features and values.

## Glossary of key concepts (practical for analysts)
- Annex I habitats, Annex II plant species: core targeted features for load/level allocation; Annex II plant species treated as part of habitat.
- SPA features vs. Annex II non-plant features: approach to deriving related critical loads via habitat relationships rather than direct species-specific loads.
- Broad Habitats: used for acidity critical loads; mapping via NBN/JNCC tables to designated features.
- EUNIS classes: used to harmonize nitrogen critical loads with habitat terminology across Europe.
- Deposition type (F/M/G): context for nitrogen and acidity deposition assessments.

## Practical considerations and challenges (alignment with the Analysts archetype)
- Data linkage and standardisation: unifying multiple data sources (habitats, species, NVC classes) to produce consistent critical loads/levels.
- Data gaps and non-matches: handling cases where no suitable EUNIS or habitat match exists; may require site-specific analysis.
- Transparency and traceability: explicit justifications for each linkage and load/level decision, with documentation of uncertainties.
- Site-level applicability: assigning site-relevant values by combining habitat, species dependencies, and local sensitivity assessments.
- Access and reproducibility: dataset structure designed to enable discoverability and reuse, with metadata and clear field definitions.