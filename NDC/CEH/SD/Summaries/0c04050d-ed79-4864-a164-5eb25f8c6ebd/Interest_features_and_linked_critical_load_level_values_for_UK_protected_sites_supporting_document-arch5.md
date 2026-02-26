# Assigning Relevant Critical Loads/Levels to designated features of protected nature conservation sites

## Overview
- Describes the process of assigning critical loads and critical levels to designated features within protected nature conservation sites in the UK (SAC, SPA, SSSI), with England-specific SSSI phase.
- Three datasets/documentation describe the linkages between site features and empirical pollutant thresholds (nitrogen, acidity, ammonia, NOx, SO2).
- Emphasizes using empirical evidence, habitat classifications, and expert judgment to determine appropriate load/level assignments and their transparently justified rationale.

## Methodology and Phases
- Phase 1: Annex I habitat features and Annex II plant features are assigned; Annex II plant features treated as in situ part of habitat.
- Phase 2: Special Protection Area (SPA) bird features and Annex II non-plant features are assigned using the same methodological approach as SPA features.
- Phase 3: SSSI habitat features (England only) are assigned.
- Method combines habitat correspondence and empirical loads to ensure consistency across European habitat terminology (EUNIS) and national feature sets.

## Critical Loads for Nutrient Nitrogen
- Based on UNECE Long-Range Transboundary Air Pollution framework; empirical loads derived from experiments and gradient studies.
- Loads are mapped to EUNIS habitat classes to maintain cross-European consistency; habitat correspondence tables link EUNIS classes to interest features.
- Sensitivity judgments determine whether a feature is affected by eutrophication from atmospheric deposition; many features are linked to their most suitable EUNIS class with documented justifications for transparency.

## Critical Loads for Acidity
- Based on six Broad Habitats (e.g., acid grassland, calcareous grassland, dwarf shrub heath, bogs, montane, unmanaged woodland) per UK Biodiversity Action Plan.
- Assignments use NBN/JNCC habitat correspondence to relate Broad Habitats to Annex I/Annex II features.
- Designated features are assessed for acidity sensitivity; coastal features with high buffering may be not sensitive (e.g., estuaries, reefs); calcareous features can also be not sensitive due to buffering.
- Justifications for matchings and impacts of exceedance are recorded for transparency.

## Exceptions
- Not all Annex I features match a suitable EUNIS class; where mismatches occur, further scientific assessment is conducted and site-by-site evaluations may be indicated.
- Any non-matches are explicitly noted in the dataset.

## SPA Features and Annex II Non-Plant Species
- Direct effects of nitrogen and acidity on bird species are limited; instead, link species viability to the habitat’s condition.
- For each species, a series of questions guides the assignment:
  1) Identify relevant Broad Habitat for the species (breeding/feeding/roosting dependencies).
  2) Determine habitat sensitivity to eutrophication and/or acidification.
  3) Assess potential impacts on breeding/feeding/roosting viability.
  4) Apply expert judgment using best available science; note positive/negative potential effects and uncertainties.
  5) If negative effects are likely, assign the most relevant nutrient nitrogen or acidity critical load to the habitat in which the species occurs.
- Similar methodology and quality control apply to Annex II non-plant species.

## Critical Levels
- Not habitat-specific; target broad vegetation types (e.g., forest, arable, semi-natural) with specific values for sensitive lichens and bryophytes (ammonia context).
- Reported values (examples):
  - NOx: 30 µg/m3 (annual mean)
  - SO2: 20 µg/m3 (annual mean) for forests/natural vegetation; 10 µg/m3 (annual mean) for sensitive lichens
  - Ammonia: 1 µg/m3 (annual mean) for lichens/bryophytes; 3 µg/m3 (annual mean) for other vegetation (uncertainty range 2–4 µg/m3)
- Values reference WHO, CLRTAP, AQ Directive; linkages to habitat and species are informed by National Vegetation Classifications (NVC) and site knowledge.

## Linkages and Site-Relevant Context
- Where possible, link habitat-level critical loads/levels to site-relevant ammonia, NOx, and SO2 thresholds.
- Linkages are informed by whether bryophytes or lichens are integral to the designated feature habitat.

## Data Structure and Datasets
- Three CSV datasets contain critical loads/levels linkages across the UK’s SAC, SPA, and England-only SSSI networks:
  - APIS_SAC_sites_feature_critical_load_linkages.csv
  - APIS_SPA_sites_feature_critical_load_linkages.csv
  - APIS_SSSI_sites_feature_critical_load_linkages.csv
- Key columns include:
  - SITECODE, SITENAME, COUNTRY, DESIGNATION, INTERESTCODE, INTERESTNAME, INTERESTLAYNAME, INTERESTTYPECODE, INTERESTTYPE, NVC_CODE, APIS_NAME, BROAD_HABITATCODE, BROADHABITAT, DEPTYPE, SENSITIVENDEP, NCLCODE, NCLCLASS, JUSTIFICATIONALLOCATIONNCL, EUNIS, CLMIN_NUTN, CLMAX_NUTN, RECOMMENDED_VALUE, NTEXT, SENSITIVEACIDITY, ACCODE, ACIDITYCLASS, JUSTIFICATIONA, ATEXT, BRYOPHYTES, LICHENS, AMMONIA_CL_VALUE, AMMONIA_CL_TEXT, NITROGEN_DIOXIDE_CL_VALUE, NITROGEN_DIOXIDE_CL_TEXT, SULPHUR_DIOXIDE_CL_VALUE, SULPHUR_DIOXIDE_CL_TEXT, SPECIESSENSITIVEN, SPECIESSENSITIVITYN, JUSTIFYSPECIESSENSITIVITYN, SPECIES_SENSITIVE_NH3, JUSTIF_SPECIES_SENSITIVE_NH3, SPECIES_SENSITIVE_NOX, JUSTIF_SPECIES_SENSITIVE_NOX, SPECIES_SENSITIVE_SO2, JUSTIF_SPECIES_SENSITIVE_SO2, etc.
- Fields capturing deposition type, sensitivity, species/habitat linkages, and site-specific justifications provide a rich audit trail for governance and reuse.

## Data Accessibility and References
- Resource locator: APIS portal for critical loads and linkages.
- References used include Noordwijkerhout Expert Workshop (2010), WHO, CLRTAP, and national vegetation classifications; methodology supports transparency and reproducibility.

## Implications for Data Stewards
- Emphasizes governance of complex, multi-phase assessments across multiple designation types with transparent justifications.
- Requires careful metadata to document phase decisions, sensitivity judgments, and any site-by-site considerations.
- Highlights the need to maintain linkage mappings (habitat classes to EUNIS, NVC, etc.) and to manage updates as scientific understanding evolves.
- Ensures dataset interoperability by aligning with European habitat terminology and credible references, while accommodating national specifics (England-only SSSI phase).