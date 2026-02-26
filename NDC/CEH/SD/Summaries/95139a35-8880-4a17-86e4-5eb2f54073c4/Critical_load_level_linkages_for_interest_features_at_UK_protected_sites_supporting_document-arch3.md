# Assigning Relevant Critical Loads/Levels to designated features of protected nature conservation sites

## Purpose and scope
- Methodology to assign the most relevant critical loads and critical levels for nutrient nitrogen and acidity to designated features of protected sites (SAC, SPA, and A/SSSI).
- Phases cover Annex I habitat features, Annex II plant features (combined as in situ) and Annex II non-plant features; SPA bird features; and A/SSSI habitat features.
- Aims to enable consistent assessment of atmospheric pollution impacts and support monitoring and decision-making.

## Phases of assignment
- Phase 1: Annex I habitat features and Annex II plant features (in situ) assigned to corresponding critical loads/levels.
- Phase 2: SPA bird features and Annex II non-plant features assigned using the same methodology as SPA features.
- Phase 3: A/SSSI habitat features only.

## Critical loads for nutrient nitrogen
- Based on empirical evidence (experiments, gradient studies) under UNECE LRTAP; assigned to EUNIS habitat classes for cross-Europe consistency.
- Habitat correspondence tables map EUNIS classes to Annex I features, A/SSSI features, or Annex II/SPA features.
- Sensitivity assessments determine which features may be affected by eutrophication from atmospheric deposition; most features are considered sensitive except a minority (e.g., estuaries, reefs, coastal lagoons).
- Justifications for habitat matches are recorded to ensure transparency and consistency.
- Uses Noordwijkerhout Expert Workshop (UNECE 2010) values, with notes on reliability and potential exceedance impacts.

## Critical loads for acidity
- Based on soil and habitat types across six Broad Habitats (e.g., acid grassland, calcareous grassland, dwarf shrub heath, bogs, montane, coniferous/broadleaved woodland).
- Habitat correspondence tables (NBN/JNCC) link Broad Habitats to Annex I/A/SSSI or Annex II/SPA features.
- Designated features assessed for sensitivity to acidification; coastal features and highly buffered calcareous features may be not sensitive.
- Annex I features and Annex II plant features matched to corresponding Broad Habitat critical loads; justification levels documented.
- Expert judgments from Natural England, SNH, CEH; some potential positive effects (e.g., increased food supply) considered where relevant.
- If a habitat is deemed insensitive, no acidity critical load is assigned.

## Exceptions and special cases in load allocation
- Some Annex I features may not have a suitable EUNIS match; may require further literature review or site-by-site assessment.
- In such cases, non-matches are indicated and alternative assessments may be undertaken.

## Assigning critical loads for SPA features and Annex II non-plant species
- Direct assignment to birds or non-plant species is generally unsuitable because direct effects from deposition are rare.
- Instead, evaluate the relationship between a species and its habitat: potential impacts on breeding, feeding, or roosting based on habitat responses to nitrogen or acidity.
- Affected species prompted by habitat sensitivity lead to assigning the most relevant nutrient nitrogen or acidity critical load based on the broad habitat, with supporting justification.
- Where the habitat is assessed as insensitive to either pollutant, no critical load is assigned.

## Process for species-specific considerations
- For each species, evaluate:
  1) Relevant BAP broad habitat (habitat used for breeding/feeding/roosting).
  2) Habitat sensitivity to eutrophication and/or acidification.
  3) Potential impacts on viability of breeding/feeding/roosting.
  4) Expert judgments on positive/negative effects; capture uncertainty where present.
  5) If negative impacts are likely, assign the most relevant nitrogen or acidity critical load based on the habitat and provide justification.

## Critical Levels
- Critical levels are not habitat-specific as loads; they cover broad vegetation types (e.g., forest, arable, semi-natural) and include specific values for sensitive lichens and bryophytes in ammonia contexts.
- Key values (annual mean):
  - NOx: 30 µg/m3 (receptor: all; reference: WHO/CLRTAP/AQ Directive)
  - SO2: 20 µg/m3 (receptor: forests/natural vegetation; annual mean; reference: WHO/CLRTAP/AQ Directive)
  - SO2: 10 µg/m3 (receptor: sensitive lichens; annual mean; reference: WHO)
  - Ammonia: 1 µg/m3 (receptor: lichens/bryophytes; annual mean; reference: CLRTAP)
  - Ammonia: 3 µg/m3 (receptor: other vegetation; annual mean; uncertainty 2–4 µg/m3; reference: CLRTAP)
- Where possible, linkages are established between habitats and species to provide site-relevant CLs for ammonia, NOx, and SO2, using National Vegetation Classifications (NVC) and site knowledge.

## Linkages and data mapping
- Link habitats to species where feasible to derive site-relevant critical loads for pollutants.
- Linkages rely on NVC and practical site knowledge to ensure relevance to designated features.

## Resource locators and data framework
- Primary reference: APIS (Animal and Plant Insurance Services) SRCL for critical loads and levels.
- Fieldwork/lab data: not required within this framework; focus is on data transfer, mapping, and justification.
- Quality control and calibration notes are minimal; emphasis on clear justifications and transparent mappings.

## Details of data structure
- Three datasets documenting critical load/level linkages:
  - APIS_SAC_feature_critical_load_level_linkages.csv
  - APIS_SPA_feature_critical_load_level_linkages.csv
  - APIS_SSSI_feature_critical_load_level_linkages.csv
- Key fields (summarized):
  - INTERESTCODE, INTERESTNAME, INTERESTLAYNAME, INTERESTTYPECODE/NAME
  - NVC_CODE and APIS_NAME (habitat naming)
  - BROAD_HABITATCODE and BROADHABITAT (BAP classification)
  - DEPTYPE (deposition type: F/M/G)
  - SENSITIVENDEP (nitrogen sensitivity) and NCLCODE/NCLCLASS (nitrogen critical load classification)
  - JUSTIFICATIONALLOCATIONNCL and EUNIS (mapping and class)
  - CLMIN_NUTN, CLMAX_NUTN, RECOMMENDED_VALUE (empirical nutrient N loads)
  - NTEXT (additional information)
  - SENSITIVEACIDITY and ACCODE/ACIDITYCLASS and JUSTIFYSPECIESSENSITIVITYA (acidity-related)
  - AMMONIA_CL_VALUE/AMMONIA_CL_TEXT and NOX/NITROGEN_DIOXIDE_CL_VALUE/TEXT (ammonia and NOx specifics)
  - SULPHUR_DIOXIDE_CL_VALUE/TEXT (SO2 specifics)
  - SPECIESSENSITIVEN/SPECIES_SENSITIVITY flags and related justification text fields
- These datasets provide the structured mapping required to apply the methodology to specific SAC/SP A/SSSI features, with explicit justification and sensitivity information.

## End notes
- The approach integrates international frameworks (UNECE LRTAP) with national habitat classifications and site-specific knowledge to derive defensible and auditable load/level assignments.
- Transparency is emphasized through documented justifications, explicit habitat-species linkages, and format-preserving data structures for monitoring and reporting.