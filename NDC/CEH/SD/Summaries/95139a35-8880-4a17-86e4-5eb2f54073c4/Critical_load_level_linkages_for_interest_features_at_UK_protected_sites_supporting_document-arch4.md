# Assigning Relevant Critical Loads/Levels to designated features of protected nature conservation sites

## Overview
- Objective: assign the most relevant critical loads and critical levels to designated features within protected nature conservation sites (e.g., SACs, SPAs, A/SSSIs).
- Approach is phased and feature-specific, linking atmospheric deposition effects to habitat and species interests.

## Phases of assignment
1. Annex I habitat features and Annex II plant species features (plants treated as in situ habitat; other Annex II species are considered separately).
2. Special Protection Area (SPA) bird features and Annex II non-plant species features using the same methodology as SPA features.
3. A/SSSI habitat features only.

## Critical loads for nutrient nitrogen
- Based on empirical evidence and coordinated under the UNECE Convention on Long-Range Transboundary Air Pollution.
- Empirical loads are assigned to habitat classes in the European Nature Information System (EUNIS) to maintain consistent habitat terminology across Europe.
- Habitat correspondence tables map EUNIS classes to interest features (Annex I, A/SSSI, Annex II/SPA features).
- Sensitivity assessments determine which features are affected by eutrophication; most features are sensitive except some coastal, estuarine, or highly buffered habitats.
- Linkage of Annex I features and Annex II plant features to suitable EUNIS classes; all justifications are recorded for transparency.
- Uses Noordwijkerhout Expert Workshop (2010) values; notes on reliability and potential impacts if exceeded.

## Critical loads for acidity
- Based on soil and habitat types across six Broad Habitats (e.g., acid grassland, calcareous grassland, dwarf shrub heath, bogs, montane, unmanaged woodlands).
- Habitats are matched to Annex I features, A/SSSI habitat features, or Annex II/SPA features using NBN/JNCC habitat correspondence tables.
- Designated features are assessed for sensitivity to acidification; many coastal features show high buffering capacity and are not sensitive, whereas others (e.g., calcareous features) may be protected by buffering.
- Justifications are documented to explain allocations and potential impacts of exceedance.

## Exceptions
- Annex I habitat features may not always map to a suitable EUNIS class; where this occurs, further evidence may yield a different sensible critical load, or site-by-site assessments are indicated.
- For SPA features and Annex II non-plant species, direct deposition effects on birds are rarely observed; instead, the relationship between habitat health and bird/non-plant species viability is used to infer potential impacts.
- Where a feature’s habitat is deemed insensitive to acidity or eutrophication, no critical load is assigned.

## Assigning critical loads for SPA features and Annex II non-plant species
- Direct effects of nitrogen and acidity on birds are uncommon; assessments rely on habitat integrity and its influence on breeding, feeding, or roosting suitability.
- For each species, the following questions guide the assessment:
  - What is the relevant Broad Habitat the species depends on?
  - Is that habitat sensitive to eutrophication or acidification?
  - If yes, what are the potential impacts on the species’ viability?
  - Expert judgments consider both positive (e.g., increased food supply) and negative effects; uncertainties are acknowledged.
  - If potential negative effects exist, the most relevant nitrogen or acidity critical load is assigned based on the habitat type, with similar justification and linkage as for Annex I features.
- Judgments are reviewed through Quality Control by relevant conservation bodies and CEH.

## Critical Levels
- Not habitat-specific like critical loads; instead, levels are set for broad vegetation types and include specific receptors (e.g., lichens, bryophytes).
- Example values:
  - NOx: Receptor = All; Time Period = Annual mean; Critical Level = 30 μg/m3; References include WHO and CLRTAP AQ Directive.
  - SO2: Receptors include Forests/Natural Vegetation (annual mean = 20 μg/m3) and Sensitive lichens (annual mean = 10 μg/m3); References include WHO and AQ Directive.
  - Ammonia: Receptors include Lichens/bryophytes (annual mean = 1 μg/m3) and Other vegetation (annual mean = 3 μg/m3, with 2–4 μg/m3 uncertainty range); References include CLRTAP.
- Linkages are established between habitats and species where possible, guided by National Vegetation Classifications (NVC) and site knowledge.

## Linkages and data sources
- Data are organized to connect habitat features with corresponding critical loads and levels for SAC, SPA, and A/SSSI features.
- Resource locator: http://www.apis.ac.uk/srcl
- Data and metadata support are designed to enable traceability from habitat type to assigned load/level and to document justifications and uncertainties.

## Details of data structure
- Three datasets capture critical loads and level linkages for designated interest features:
  - APIS_SAC_feature_critical_load_level_linkages.csv
  - APIS_SPA_feature_critical_load_level_linkages.csv
  - APIS_SSSI_feature_critical_load_level_linkages.csv
- Key fields include:
  - INTERESTCODE, INTERESTNAME, INTERESTLAYNAME, INTERESTTYPECODE, INTERESTTYPE
  - NVC_CODE, APIS_NAME, BROAD_HABITATCODE, BROADHABITAT
  - DEPTYPE (deposition type: F/M/G)
  - SENSITIVENDEP (nitrogen sensitivity)
  - NCLCODE, NCLCLASS, JUSTIFICATIONALLOCATIONNCL
  - EUNIS, CLMIN_NUTN, CLMAX_NUTN, RECOMMENDED_VALUE, NTEXT
  - SENSITIVEACIDITY, ACCODE, ACIDITYCLASS, JUSTIFYSA
  - BRYOPHYTES, LICHENS, AMMONIA_CL_VALUE, AMMONIA_CL_TEXT
  - NITROGEN_DIOXIDE_CL_VALUE, NITROGEN_DIOXIDE_CL_TEXT
  - SULPHUR_DIOXIDE_CL_VALUE, SULPHUR_DIOXIDE_CL_TEXT
  - SPECIES_SENSITIVE_NH3, JUSTIF_SPECIES_SENSITIVE_NH3, SPECIES_SENSITIVE_NH3_TEXT
  - SPECIES_SENSITIVE_NOX, JUSTIF_SPECIES_SENSITIVE_NOX, SPECIES_SENSITIVE_NOX_TEXT
  - SPECIES_SENSITIVE_SO2, JUSTIF_SPECIES_SENSITIVE_SO2, SPECIES_SENSITIVE_SO2_TEXT
  - Additional species sensitivity fields (NH3, NOX, NOX_TEXT, etc.)

## Practical implications for Data Leaders
- Ensures an end-to-end data pipeline from habitat classification (NVC/EUNIS) to empirical load values and site-specific justifications.
- Emphasizes transparency and documentation of reasoning and exceptions for governance and accountability.
- Highlights the need for maintaining metadata, data provenance, and clear data structures to support reuse across protected site networks (SAC/SPA/A/SSSI).
- Underlines challenges such as data gaps, mapping mismatches, and the necessity of expert judgement in complex allocations.