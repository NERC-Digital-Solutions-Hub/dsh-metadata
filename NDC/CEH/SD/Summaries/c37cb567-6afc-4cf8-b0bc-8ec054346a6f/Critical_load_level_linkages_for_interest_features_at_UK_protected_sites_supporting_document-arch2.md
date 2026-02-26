# Assigning Relevant Critical Loads/Levels to designated features of protected nature conservation sites

## Objective and scope
- Assign critical loads for nitrogen and acidity, and corresponding critical levels, to designated features within UK nature conservation sites (SACs, SPAs, A/SSSIs).
- Structure the work into phases by feature type:
  - Phase 1: Annex I habitat features and Annex II plant features (plants treated as in situ parts of habitat).
  - Phase 2: SPA bird features and Annex II non-plant species features (apply the same method as for SPA features).
  - Phase 3: A/SSSI habitat features only.

## Critical loads for nutrient nitrogen
- Governed by UNECE Long-Range Transboundary Air Pollution framework.
- Based on empirical evidence from experiments and targeted gradient studies.
- Assigned to habitat classes in the European Nature Information System (EUNIS) to ensure consistent habitat terminology across Europe.
- Habitat correspondence tables link EUNIS classes to interest features (Annex I, Annex II/SPA, A/SSSI).
- Sensitivity assessment: majority of features are sensitive to eutrophication; estuaries, reefs, coastal lagoons often not sensitive due to buffering.
- Linking process:
  - Annex I habitats and Annex II plant features matched to suitable EUNIS classes.
  - Justifications recorded for transparency and consistency.
  - Use Noordwijkerhout Expert Workshop (2010) values; note reliability and potential exceedance impacts.
- Exceptions: some Annex I features may not align with a suitable EUNIS class; non-matches are indicated and site-by-site assessments may be needed.

## Critical loads for acidity
- Based on soil and habitat types across six Broad Habitats (e.g., acid grassland, calcareous grassland, dwarf shrub heath, bogs, montane, unmanaged coniferous/broadleaved woodland).
- Habitat correspondence tables from NBN (via JNCC) assign Broad Habitats to Annex I/A/SPA features.
- Sensitivity assessment: most features can be affected by deposition if high and soils have low buffering; coastal features and highly calcareous habitats often show resilience due to buffering; sensitivity justification recorded.
- Process:
  - Match Annex I/A/SPA features to Broad Habitats.
  - Document the justification level and describe potential exceedance impacts.
- Exceptions: if a suitable Broad Habitat mapping is not available, further science review may be required; non-matches are indicated.

## Critical loads for SPA features and Annex II non-plant species
- Direct nitrogen/acid deposition effects on birds and non-plant species are uncommon; instead, assess impacts via habitat integrity and suitability for breeding, feeding, or roosting.
- Apply the same methodology to Annex II non-plant species, using generic conservation objectives and QC checks by statutory bodies and CEH.
- If the associated habitat is insensitive to acidity or eutrophication, no critical load is assigned.
- Species-specific assessment framework:
  - Identify relevant BAP Broad Habitat for the species (could involve multiple habitats).
  - Assess habitat sensitivity to eutrophication or acidification.
  - Evaluate potential impacts on breeding/feeding/roosting viability.
  - Acknowledge possible positive effects (e.g., increased food supply) with associated uncertainty.
  - Assign the most relevant nitrogen or acidity critical load based on the habitat context when negative impacts are anticipated.
  - Provide justification for the linkage and load assignment.

## Critical levels
- Not habitat-specific; set to cover broad vegetation types (e.g., forests, arable land, semi-natural habitats).
- Ammonia: lichens and bryophytes as key receptors; different thresholds for other vegetation.
- NOx: receptor = all; time period = annual mean; value = 30 µg/m3 (WHO/CLRTAP/AQ Directive reference).
- SO2: receptors include forests/natural vegetation (annual mean, 20 µg/m3); sensitive lichens (annual mean, 10 µg/m3).
- Ammonia thresholds:
  - Lichens/bryophytes: 1 µg/m3 (annual mean).
  - Other vegetation: 3 µg/m3 (annual mean) with uncertainty 2–4 µg/m3.
- Linkages:
  - Where possible, align habitat and species with critical levels using National Vegetation Classifications (NVC) and site knowledge to produce site-relevant values for ammonia, NOx, and SO2.

## Data structures and outputs
- Three datasets capturing critical load/level linkages for designated interest features:
  - APIS_SAC_feature_critical_load_level_linkages.csv
  - APIS_SPA_feature_critical_load_level_linkages.csv
  - APIS_SSSI_feature_critical_load_level_linkages.csv
- Key fields (examples):
  - INTERESTCODE, INTERESTNAME, INTERESTLAYNAME, INTERESTTYPECODE, INTERESTTYPE
  - NVC_CODE, APIS_NAME, BROAD_HABITATCODE, BROADHABITAT
  - DEPTYPE, SENSITIVENDEP, NCLCODE, NCLCLASS
  - JUSTIFICATIONALLOCATIONNCL, EUNIS, CLMIN_NUTN, CLMAX_NUTN, RECOMMENDED_VALUE
  - NTEXT, SENSITIVEACIDITY, ACCODE, ACIDITYCLASS, JUSTIFYSA
  - AMMONIA_CL_VALUE, AMMONIA_CL_TEXT, NITROGEN_DIOXIDE_CL_VALUE, NITROGEN_DIOXIDE_CL_TEXT
  - SULPHUR_DIOXIDE_CL_VALUE, SULPHUR_DIOXIDE_CL_TEXT
  - SPECIESSENSITIVEN, SPECIESSENSITIVITYN, JUSTIFYSPECIESSENSITIVITYN
  - SPECIES_SENSITIVE_NH3, JUSTIF_SPECIES_SENSITIVE_NH3, SPECIES_SENSITIVE_NOX, JUSTIF_SPECIES_SENSITIVE_NOX, SPECIES_SENSITIVE_SO2, JUSTIF_SPECIES_SENSITIVE_SO2
- Purpose of datasets: enable traceable, transparent linkage of features to their critical loads/levels and support decision-making and policy assessment.

## Data quality, transparency, and governance
- Justifications: explicit notes for transparency when linking features to loads/levels.
- Quality control: expert judgments reviewed by statutory bodies and CEH.
- Data provenance: based on established frameworks (UNECE LRTAP, Noordwijkerhout 2010) and national sources (NBN, EUNIS, NVC).
- Clear handling of exceptions and non-matches with guidance for potential site-by-site assessments.

## Resources and references
- Fieldwork and instrumentation: not applicable (NA) within dataset context.
- External references and authority:
  - Noordwijkerhout Expert Workshop (2010)
  - UNECE CLRTAP, WHO AQ Directive
  - EUNIS habitat classifications
  - NBN and JNCC habitat mappings
  - APIS data portal (APIS_SRCL)

## Practical implications for monitoring and policy
- Provides a standardized method to quantify how atmospheric deposition may affect protected features, enabling consistent monitoring of environmental health and policy performance over time.
- Facilitates data sharing and interoperability across agencies by using common classifications (EUNIS, NVC, APIS) and standardized datasets.
- Supports scenario analysis for nutrient nitrogen and acidity deposition, guiding habitat and species conservation decisions under atmospheric pollution pressures.