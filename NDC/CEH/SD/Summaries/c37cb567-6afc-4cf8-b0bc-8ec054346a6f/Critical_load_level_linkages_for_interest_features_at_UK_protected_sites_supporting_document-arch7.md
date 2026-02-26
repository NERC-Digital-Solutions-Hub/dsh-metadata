# Assigning Relevant Critical Loads/Levels to designated features of protected nature conservation sites

- Purpose: Define how to assign critical loads and critical levels to designated features of SACs, SPAs, and A/SSSIs, enabling GIS-based interpretation of potential impacts from atmospheric deposition.

## Phases of assignment
- Phase 1: Annex I habitat features and Annex II plant species features (with Annex II features combined as in situ plants part of habitat).
- Phase 2: SPA bird features and Annex II non-plant species features (using the same method as SPA features).
- Phase 3: A/SSSI habitat features only.

## Critical loads for nutrient nitrogen
- Basis: UNECE Convention on Long-Range Transboundary Air Pollution; empirical, experiment-based evidence and gradient studies.
- Habitat linkage: Empirical loads are assigned to habitat classes in EUNIS to ensure cross-European consistency; use habitat correspondence tables to map EUNIS classes to interest features (Annex I, A/SSSI, Annex II/SPA).
- Sensitivity assessment: Judgements on eutrophication sensitivity; most habitats are sensitive, with exceptions like estuaries, reefs, coastal lagoons (less sensitive due to buffering) and some calcareous features.
- Process: Link Annex I and Annex II plant features to the most suitable EUNIS class; document justifications for transparency.
- References: Noordwijkerhout Expert Workshop (2010) values and related justifications; note reliability and potential exceedance impacts.

## Critical loads for acidity
- Basis: Six Broad Habitats (acid grassland, calcareous grassland, dwarf shrub heath, bogs, montane, unmanaged coniferous/broadleaved woodland) as per UK Biodiversity Action Plan (1994); NBN/JNCC habitat correspondence tables used to map to features.
- Sensitivity assessment: Evaluated by experts; most features may be impacted where deposition is high or soils are poorly buffered; coastal features with high base cation buffering (e.g., estuaries, reefs) often not sensitive.
- Habitat linkage: Annex I and Annex II features matched to Broad Habitats; sensitivity assessments documented with justification.
- Exceptions: Some Annex I features may not map to a suitable EUNIS class; unresolved cases may require site-specific assessment.

## Exceptions
- Not all Annex I features have perfect EUNIS matches; where mismatches occur, further science-based investigation or site-by-site assessment may be needed; non-matches are indicated in the dataset.

## Assigning critical loads for SPA features and Annex II non-plant species
- Direct deposition effects on birds or non-plant species are rare/unlikely; instead, link potential impacts via habitat integrity.
- Methodology: Assess whether the habitat’s sensitivity to eutrophication or acidification could affect bird breeding, feeding, or roosting; apply the same approach as for other features.
- Decision flow: If the habitat is insensitive to acidity or eutrophication, no critical load is assigned for that feature.

## For each species: series of assessment questions
1. Identify the relevant BAP Broad Habitat the species depends on (breeding, feeding, roosting); may involve multiple habitats.
2. Determine if that habitat is sensitive to eutrophication or acidification.
3. Assess potential impacts on habitat viability and, consequently, on the species’ breeding/feeding/roosting.
4. Apply expert judgement, noting both potential negative and possible positive effects (e.g., enhanced food supply) and uncertainty.
5. If negative impacts are plausible, assign the most relevant nutrient nitrogen or acidity critical load based on the habitat.
6. Document justifications similarly to Annex I feature processes.

## Critical Levels (not habitat-specific like critical loads)
- NOx: Receptor = All; Time period = Annual mean; Level = 30 µg/m3 (WHO/CLRTAP/AQ Directive references).
- SO2: Receptor = Forests and natural vegetation; Time period = Annual mean; Level = 20 µg/m3; and for sensitive lichens: 10 µg/m3 (annual mean; WHO/CLRTAP/AQ Directive references).
- Ammonia: Receptor = Lichens and bryophytes (core ecosystem components); Time period = Annual mean; Level = 1 µg/m3; Receptor = Other vegetation; Level = 3 µg/m3 (uncertainty range 2–4 µg/m3); references from CLRTAP.
- Linkages: Where possible, link habitat features to critical levels (ammonia, NOx, SO2) using National Vegetation Classifications (NVC) and site knowledge.

## Linkages and data mapping
- Habitat-to-load/level linkages are established where feasible to reflect site-relevant exposures for ammonia, NOx, and SO2.
- NVC and site-level information support mapping between habitats and chemical thresholds.

## Resource locators
- APIS SRCL (Summary of Critical Loads): http://www.apis.ac.uk/srcl

## Details of data structure
- Datasets (3 CSV files):
  - APIS_SAC_feature_critical_load_level_linkages.csv
  - APIS_SPA_feature_critical_load_level_linkages.csv
  - APIS_SSSI_feature_critical_load_level_linkages.csv
- Key fields (highlights):
  - INTERESTCODE, INTERESTNAME, INTERESTLAYNAME, INTERESTTYPECODE, INTERESTTYPE, NVC_CODE, APIS_NAME, BROAD_HABITATCODE, BROADHABITAT
  - DEPTYPE (deposition type: Forest, Moorland, Grid Average)
  - SENSITIVENDEP (is feature sensitive to nutrient nitrogen?)
  - NCLCODE / NCLCLASS (critical load class)
  - JUSTIFICATIONALLOCATIONNCL (justification for N-load)
  - EUNIS, CLMIN_NUTN, CLMAX_NUTN, RECOMMENDED_VALUE (nutrient nitrogen loads)
  - NTEXT (further information)
  - SENSITIVEACIDITY, ACCODE, ACIDITYCLASS, JUSTIFICATIONA, ATEXT (acidity)
  - BRYOPHYTES, LICHENS (special interest indicators)
  - AMMONIA_CL_VALUE, AMMONIA_CL_TEXT (ammonia critical levels)
  - NITROGEN_DIOXIDE_CL_VALUE, NITROGEN_DIOXIDE_CL_TEXT (NO2 levels)
  - SULPHUR_DIOXIDE_CL_VALUE, SULPHUR_DIOXIDE_CL_TEXT (SO2 levels)
  - SPECIESSENSITIVEN, SPECIESSENSITIVITYN, JUSTIFYSPECIESSENSITIVITYN
  - SPECIESSENSITIVEA, SPECIESSENSITIVITYA, JUSTIFYSPECIESSENSITIVITYA
  - SPECIES_SENSITIVE_NH3, JUSTIF_SPECIES_SENSITIVE_NH3, etc. (species-specific sensitivities to NH3/NOx/SO2 and justifications)

## Data usage for GIS
- Purpose-built map products: visualize where critical loads/levels exceed thresholds for designated features.
- Use crosswalks between APIS, EUNIS, NVC, and site records to align features with load/level values.
- Document justifications and uncertainties for transparency; handle exceptions with site-by-site notes.
- Integrate with site boundaries (SAC/SPAs/A/SSSIs) to produce impact maps, sensitivity layers, and monitoring priorities.