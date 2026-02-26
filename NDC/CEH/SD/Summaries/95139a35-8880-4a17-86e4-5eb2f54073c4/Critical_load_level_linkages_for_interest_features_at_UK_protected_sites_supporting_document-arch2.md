# Assigning Relevant Critical Loads/Levels to designated features of protected nature conservation sites

- Purpose: to assign the most relevant critical loads and critical levels to designated features of protected sites, enabling consistent assessment of eutrophication and acidification risks to habitats and species over time.

## Phases of assignment
- Phase 1: Annex I habitat features and Annex II plant species features (Annex II plants treated as in situ, part of the habitat).
- Phase 2: Special Protection Area (SPA) bird features and Annex II non-plant species features; same method as SPA features.
- Phase 3: A/SSSI habitat features only.

## Critical loads for nutrient nitrogen
- Set under UNECE Long-Range Transboundary Air Pollution framework.
- Based on empirical evidence from experiments and gradient studies.
- Linked to habitat classes in the European Nature Information System (EUNIS) for consistency.
- Habitat correspondence tables determine relationships between EUNIS classes and interest features (Annex I, A/SSSI, Annex II/SPA).
- Sensitivity assessments determine how eutrophication affects features; most habitats are sensitive, with some exceptions (e.g., estuaries, reefs, coastal lagoons may be less sensitive).
- Justifications for matching habitats to EUNIS classes are documented for transparency.
- Values referenced from the Noordwijkerhout Expert Workshop (2010); include reliability and potential impacts of exceedance.

## Critical loads for acidity
- Based on soil and habitat types across six Broad Habitats (e.g., acid grassland, calcareous grassland, dwarf shrub heath, bogs, montane, unmanaged woodland).
- Uses National Biodiversity Network (NBN) / JNCC habitat correspondence to assign Broad Habitats to Annex I features, A/SSSI features, or Annex II/SPA features.
- Designated features assessed for sensitivity to acidification by experienced specialists.
- Coastal features with strong sea-salt buffering may be less sensitive; calcareous features (e.g., limestone pavements) may also be less sensitive due to buffering.
- Annex I and Annex II features are matched to the corresponding acidity critical loads.
- Justifications for allocations and descriptions of potential impacts are recorded.

## Exceptions to critical load assignments
- Sometimes Annex I features do not map to a suitable EUNIS class; may require further literature review or site-by-site assessment.
- Non-matches are documented; in some cases, targeted site assessments are indicated.

## Assigning critical loads for SPA features and Annex II non-plant species
- Direct deposition effects on birds are rare/unlikely; instead, habitat integrity is used to infer potential impacts on birds (breeding, feeding, roosting).
- A similar methodology is used for Annex II non-plant species, informed by generic conservation objectives and Quality Control by statutory bodies and CEH.
- Per-species assessment workflow:
  - Identify relevant Broad Habitat for the species (habitat dependency for breeding/feeding/roosting).
  - Determine habitat sensitivity to eutrophication and/or acidification.
  - Evaluate potential impacts on the species’ viability.
  - Note positive or negative potential effects where applicable; uncertainty is acknowledged.
  - If habitat is insensitive to acidity or eutrophication, no critical load is assigned.

## Critical Levels
- Not habitat-specific; applied to broad vegetation types (e.g., forest, arable, semi-natural) and certain sensitive lichens and bryophytes (ammonia context).
- Example receptor/time/value entries include:
  - NOX: Receptor = All; Time Period = Annual mean; Critical Level = 30 µg/m3.
  - SO2: Receptor = Forests and natural vegetation; Time Period = Annual mean; Critical Level = 20 µg/m3.
  - SO2: Receptor = Sensitive lichens; Time Period = Annual mean; Critical Level = 10 µg/m3.
  - Ammonia: Receptor = Lichens and bryophytes; Time Period = Annual mean; Critical Level = 1 µg/m3.
  - Ammonia: Receptor = Other vegetation; Time Period = Annual mean; Critical Level = 3 µg/m3 (uncertainty range 2-4).
- Linkages between habitat and species are made where possible, incorporating National Vegetation Classification (NVC) and site knowledge.

## Linkages and data provenance
- Linkages established between habitat types and species where feasible to provide site-relevant critical loads for multiple pollutants (ammonia, NOX, SO2).
- Data supported by APIS and national vegetation classifications; informed by site-based knowledge and expert judgement.

## Resource locators
- APIS information and related guidance: http://www.apis.ac.uk/srcl

## Details of data structure
- Three datasets capturing critical load/level linkages for UK nature sites:
  - APIS_SAC_feature_critical_load_level_linkages.csv
  - APIS_SPA_feature_critical_load_level_linkages.csv
  - APIS_SSSI_feature_critical_load_level_linkages.csv
- Common fields include:
  - INTERESTCODE, INTERESTNAME, INTERESTLAYNAME, INTERESTTYPECODE, INTERESTTYPE, NVC_CODE, APIS_NAME, BROAD_HABITATCODE, BROADHABITAT, DEPTYPE, SENSITIVENDEP, NCLCODE, NCLCLASS, JUSTIFICATIONALLOCATIONNCL, EUNIS, CLMIN_NUTN, CLMAX_NUTN, RECOMMENDED_VALUE, NTEXT, SENSITIVEACIDITY, ACCODE, ACIDITYCLASS, JUSTIFYSA, ATEXT, BRYOPHYTES, LICHENS, AMMONIA_CL_VALUE, AMMONIA_CL_TEXT, NITROGEN_DIOXIDE_CL_VALUE, NITROGEN_DIOXIDE_CL_TEXT, SULPHUR_DIOXIDE_CL_VALUE, SULPHUR_DIOXIDE_CL_TEXT, SPECIESSENSITIVEN, SPECIESSENSITIVITYN, JUSTIFYSPECIESSENSITIVITYN, SPECIESSENSITIVEA, SPECIESSENSITIVITYA, JUSTIFYSPECIESSENSITIVITYA, SPECIES_SENSITIVE_NH3, JUSTIF_SPECIES_SENSITIVE_NH3, SPECIES_SENSITIVE_NH3_TEXT, SPECIES_SENSITIVE_NOX, JUSTIF_SPECIES_SENSITIVE_NOX, SPECIES_SENSITIVE_NOX_TEXT, SPECIES_SENSITIVE_SO2, JUSTIF_SPECIES_SENSITIVE_SO2, SPECIES_SENSITIVE_SO2_TEXT.
- Additional notes on data: fields cover sensitivity, justification, species-specific sensitivities to ammonia, NOx, and SO2, and links to NVC and habitat classifications.