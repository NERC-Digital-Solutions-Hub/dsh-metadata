# Assigning Relevant Critical Loads/Levels to designated features of protected nature conservation sites

- Aims to assign the most relevant critical loads and critical levels to designated features across UK protected sites (SAC, SPA, SSSI in England). Features include Annex I habitats, Annex II plant and non-plant species, and SPA birds. Combines habitat-based approaches with species considerations and relies on established ecological classifications and expert judgement.

## Phases of the assignment

- Phase 1: Annex I habitat features and Annex II plant species features (plant species treated as in situ components of habitat).
- Phase 2: SPA bird features and Annex II non-plant species features (same method as for SPA features).
- Phase 3: SSSI habitat features (England only).

## Critical loads for nutrient nitrogen

- Basis: Empirical critical loads established under UNECE for long-range transboundary air pollution, linked to habitat classes in EUNIS to ensure cross-European consistency.
- Method: Use habitat correspondence tables to relate EUNIS classes to interest features (Annex I, A/SSSI, Annex II/SPA features); assign relevant nitrogen critical loads via these mappings.
- Sensitivity assessment: Judgments on how designated features respond to eutrophication; minority deemed not sensitive (e.g., certain estuaries, reefs, coastal lagoons). Link features to the most appropriate EUNIS class and note justifications for transparency.
- Exceedance: Note the likely impacts and document the rationale and reliability (No/low sensitivity vs. higher risk) based on Noordwijkerhout Expert Workshop (UNECE 2010) values and associated impacts.
- Exceptions: Some Annex I features may not match an ideal EUNIS class; non-matches are indicated and may require site-by-site investigation.

## Critical loads for acidity

- Basis: Six Broad Habitats defined in the UK context (acid grassland, calcareous grassland, dwarf shrub heath, bogs, montane, unmanaged coniferous/broadleaved woodland) as per UK Biodiversity Action Plan (1994).
- Method: Use NBN-JNCC habitat correspondences to assign Broad Habitats to Annex I/A/SSSI features or Annex II/SPA features; assess sensitivity to acidification and link to corresponding acidity critical loads.
- Sensitivity assessment: Expert judgments on whether acidification deposition impacts the feature; coastal/coastal-buffered features often not sensitive; calcareous features may be buffered; provide justifications and describe potential impacts of exceedance.
- Documentation: Justifications for assignments and a transparent description of expected impacts.

## Exceptions and approach for SPA features and Annex II non-plant species

- Direct effects on birds from nitrogen or acidity are unlikely; thus, critical loads are not assigned directly to bird features.
- Indirect approach: assess whether habitat-level impacts from acidification or eutrophication affect bird breeding, feeding, or roosting, using habitat-based linkages to infer potential species-level effects.
- Process: For each species, assess relevant BAP Broad Habitat, habitat sensitivity to eutrophication/acidification, potential impacts on viability of breeding/feeding/roosting, and apply expert judgments with consideration of uncertainty and possible positive effects.
- Decision rule: If potential negative effects are identified, assign the most relevant nitrogen or acidity critical load based on the habitat in which the species occurs; document similarities to the approach used for Annex I features.

## Critical levels

- Not habitat-specific, but set to cover broad vegetation types (e.g., forest, arable, semi-natural) with specific attention to sensitive lichens and bryophytes for ammonia.
- Key values (examples):
  - NOx: Receptor = All; Time Period = Annual mean; Critical Level = 30 µg/m3 (WHO/CLRTAP/AQ Directive reference).
  - SO2: Receptor = Forests and natural vegetation; Time Period = Annual mean; Critical Level = 20 µg/m3 (WHO/CLRTAP/AQ Directive).
  - SO2 (lichens): Receptor = Sensitive lichens; Time Period = Annual mean; Critical Level = 10 µg/m3 (WHO reference).
  - Ammonia: Receptor = Lichens and bryophytes; Time Period = Annual mean; Critical Level = 1 µg/m3 (CLRTAP).
  - Ammonia: Receptor = Other vegetation; Time Period = Annual mean; Critical Level = 3 µg/m3 (uncertainty range 2–4 µg/m3, CLRTAP).
- Linkages: Where possible, link habitat and species to apply ammonia/nitrogen dioxide/sulphur dioxide levels through National Vegetation Classification (NVC) and site knowledge.

## Linkages and data integration

- Habitat-to-species linkages are established where feasible to provide site-relevant critical loads/levels for ammonia, NOx, and SO2.
- Uses NVC classifications and site-based knowledge to contextualize critical levels with respect to particular habitats and designated features.
- Emphasizes that bird and non-plant species are evaluated via habitat integrity rather than direct deposition impacts.

## Data products and structure

- Datasets:
  - APIS_SAC_sites_feature_critical_load_linkages.csv
  - APIS_SPA_sites_feature_critical_load_linkages.csv
  - APIS_SSSI_sites_feature_critical_load_linkages.csv
- Core fields (examples):
  - SITECODE, SITENAME, COUNTRY, DESIGNATION
  - INTERESTCODE, INTERESTNAME, INTERESTTYPECODE, INTERESTTYPE
  - NVC_CODE, BROAD_HABITATCODE, BROADHABITAT
  - NCLCODE, NCLCLASS, JUSTIFICATION_ALLOCATION_NCL
  - EUNIS, CLMIN_NUTN, CLMAX_NUTN, RECOMMENDED_VALUE, NTEXT
  - SENSITIVE_ACIDITY, ACCODE, ACIDITYCLASS, JUSTIFICATIONA, ATEXT
  - BRYOPHYTES, LICHENS, AMMONIA_CL_VALUE, AMMONIA_CL_TEXT
  - NITROGEN_DIOXIDE_CL_VALUE, NITROGEN_DIOXIDE_CL_TEXT
  - SULPHUR_DIOXIDE_CL_VALUE, SULPHUR_DIOXIDE_CL_TEXT
  - SPECIESSENSITIVEN, SPECIESSENSITIVITYN, JUSTIFYSPECIESSENSITIVITYN
  - SPECIESSENSITIVEA, SPECIESSENSITIVITYA, JUSTIF_SPECIESSENSITIVITYA
  - SPECIES_SENSITIVE_NH3, JUSTIF_SPECIES_SENSITIVE_NH3, SPECIES_SENSITIVE_NOX, JUSTIF_SPECIES_SENSITIVE_NOX, SPECIES_SENSITIVE_SO2, JUSTIF_SPECIES_SENSITIVE_SO2
- Data context: English site network (SAC, SPA, SSSI) with corresponding designated features and their associated critical load/level linkages, including recommended values and justifications.

## Methods, quality, and accessibility

- Data are linked to established international and national frameworks (UNECE, Noordwijkerhout workshop, NBN/JNCC, EUNIS, APIS).
- Expert judgement and quality control are applied in sensitivity assessments and in justifications to ensure transparency.
- Datasets are designed to be discoverable and usable, with metadata and site-by-site linkage records to support use in decision-making and reporting.

## Resources and references

- Resource locator: http://www.apis.ac.uk/srcl
- Frameworks: UNECE Noordwijkerhout expert workshop (2010), CLRTAP, WHO guidelines, EUNIS habitat classification, NVC, UK BAP (1994), NBN/JNCC habitat correspondences.