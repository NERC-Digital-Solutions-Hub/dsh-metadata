# Assigning Relevant Critical Loads/Levels to designated features of protected nature conservation sites

- A multi-phase methodology to assign the most relevant critical loads and critical levels to designated features of protected sites, including Annex I habitats, Annex II plant species, SPA bird features, Annex II non-plant species, and A/SSSI habitat features.

## Phases of assignment
- Phase 1: Annex I habitat features and Annex II plant species features (Annex II features treated as part of habitat since plants are in situ).
- Phase 2: SPA bird features and Annex II non-plant species features, using the same method as SPA features.
- Phase 3: A/SSSI habitat features only.

## Critical loads for nutrient nitrogen
- Based on empirical evidence under the UNECE Convention on Long-Range Transboundary Air Pollution.
- Assigned to habitat classes in the European Nature Information System (EUNIS) to ensure consistent habitat terminology across Europe.
- Habitat correspondence tables map EUNIS classes to the interest features (Annex I, A/SSSI, Annex II/SPA).
- Sensitivity assessments determine which features are affected by eutrophication from atmospheric deposition; most features are considered sensitive except some coastal or calcareous features with buffering capacity.
- Justifications for matchings are recorded for transparency; Noordwijkerhout Expert Workshop (2010) values guide reliability and potential impacts of exceedance.

## Critical loads for acidity
- Based on soil and habitat types across six Broad Habitats (per UK Biodiversity Action Plan and JNCC data).
- Uses NBN/JNCC correspondences to assign acidity loads to Annex I features, A/SSSI features, or Annex II/SPA features.
- Designated features are assessed for sensitivity to acidification; coastal features and highly buffered calcareous features may be not sensitive.
- Annex I and Annex II features are matched to the corresponding Broad Habitat critical loads; justification levels and impact descriptions are recorded.

## Exceptions
- Some Annex I habitat features may not align with any suitable EUNIS class, requiring further review or site-by-site assessment to derive sensible critical loads.
- Non-matches are clearly indicated in the dataset.

## Assigning critical loads for SPA features and Annex II non-plant species
- Direct effects of nitrogen or acidity on birds are rare; instead, linkages through habitat integrity inform potential impacts on breeding, feeding, or roosting.
- For each species:
  - Identify the relevant broad habitat (BAP) for breeding/feeding/roosting dependencies.
  - Determine habitat sensitivity to eutrophication or acidification.
  - Assess potential impacts on the species’ viability; note potential positive (e.g., increased food) and negative effects.
  - If negative impacts are likely, assign the most relevant nitrogen or acidity critical load based on the habitat.
  - Provide similar justifications as used for Annex I features, including reliability notes.

## Critical Levels
- Not habitat-specific; applied to broad vegetation types (e.g., forest, arable, semi-natural) and include ammonia-sensitive lichens and bryophytes.
- Specific values and references:
  - NOx receptor: All; Time Period: Annual mean; Critical Level: 30 µg/m3 (WHO/CLRTAP/AQ Directive)
  - SO2 receptor: Forests and natural vegetation; Time Period: Annual mean; Critical Level: 20 µg/m3 (WHO/CLRTAP/AQ Directive)
  - SO2 receptor: Sensitive lichens; Time Period: Annual mean; Critical Level: 10 µg/m3 (WHO)
  - Ammonia receptor: Lichens and bryophytes (key ecosystem integrity); Time Period: Annual mean; Critical Level: 1 µg/m3
  - Ammonia receptor: Other vegetation; Time Period: Annual mean; Critical Level: 3 µg/m3 (2–4 µg/m3 uncertainty range)
- Linkages are made between habitat and species where possible to provide site-relevant critical levels for NH3, NOx, and SO2, informed by National Vegetation Classifications (NVC) and site knowledge.

## Linkages between habitat and species
- Where feasible, habitat-species linkages are established to provide site-relevant critical loads/levels for ammonia, nitrogen dioxide, and sulfur dioxide.
- Supports translating habitat-level thresholds to species-specific implications.

## Data resources and structure
- Resource locator: http://www.apis.ac.uk/srcl
- Datasets (three CSV files):
  - APIS_SAC_feature_critical_load_level_linkages.csv
  - APIS_SPA_feature_critical_load_level_linkages.csv
  - APIS_SSSI_feature_critical_load_level_linkages.csv
- Key columns include:
  - INTERESTCODE, INTERESTNAME, INTERESTLAYNAME, INTERESTTYPECODE, INTERESTTYPE, NVC_CODE, APIS_NAME, BROAD_HABITATCODE, BROADHABITAT, DEPTYPE (deposition type), SENSITIVENDEP, NCLCODE, NCLCLASS, JUSTIFICATIONALLOCATIONNCL, EUNIS, CLMIN_NUTN, CLMAX_NUTN, RECOMMENDED_VALUE, NTEXT, SENSITIVEACIDITY, ACCODE, ACIDITYCLASS, JUSTIFYSA, ATEXT, BRYOPHYTES, LICHENS, AMMONIA_CL_VALUE, AMMONIA_CL_TEXT, NITROGEN_DIOXIDE_CL_VALUE, NITROGEN_DIOXIDE_CL_TEXT, SULPHUR_DIOXIDE_CL_VALUE, SULPHUR_DIOXIDE_CL_TEXT, SPECIESSENSITIVEN, SPECIESSENSITIVITYN, JUSTIFYSPECIESSENSITIVITYN, SPECIESSENSITIVEA, SPECIESSENSITIVITYA, JUSTIFYSPECIESSENSITIVITYA, SPECIES_SENSITIVE_NH3, JUSTIF_SPECIES_SENSITIVE_NH3, SPECIES_SENSITIVE_NH3_TEXT, SPECIES_SENSITIVE_NOX, JUSTIF_SPECIES_SENSITIVE_NOX, SPECIES_SENSITIVE_NOX_TEXT, SPECIES_SENSITIVE_SO2, JUSTIF_SPECIES_SENSITIVE_SO2, SPECIES_SENSITIVE_SO2_TEXT, etc.
- Notes: Metadata fields exist to justify allocations, record uncertainties, and document sensitivity for both habitat and species features.

## Implications for monitoring framework authors
- Provides a structured, transparent approach to assigning deposition thresholds to protected features.
- Emphasizes the use of empirical data, habitat mappings (EUNIS, NVC), and expert judgment with QA checkpoints.
- Highlights data governance and openness considerations, including transparent justifications and potential data-sharing constraints.